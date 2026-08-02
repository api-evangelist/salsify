---
name: Bulk upsert Salsify products
description: Create or update many products in a Salsify organization in one call, using the idempotent-by-shape bulk upsert operation, then verify the result.
api: openapi/salsify-write-operations-openapi.json
operations:
  - bulk-upsert-products
  - bulk-read-products
  - read-product-record
---

# Bulk upsert Salsify products

Use this when you have a set of products and you do not know (or do not care) whether
they already exist in Salsify.

## Before you start

- You need the **organization ID** (`org_id`). It is the path segment immediately after
  `/orgs/` in the Salsify application URL. See
  https://developers.salsify.com/docs/organization-id
- You need a **user API key** in the `Authorization` header, or an OAuth 2.0 Bearer
  access token. See `authentication/salsify-authentication.yml`.
- API access is licence-gated: not every Salsify organization has it enabled.
- Base URL: `https://app.salsify.com/api/v1/orgs`

## Steps

1. **Upsert the batch** — call `bulk-upsert-products`
   (`PUT /{org_id}/products/_upsert`). The body carries the products keyed by their
   Salsify or external identifier plus the properties to set.
2. **Handle the response**
   - `422 Unprocessable Entity` means the payload was semantically invalid — a required
     property is missing, a value failed validation, or a referenced entity does not
     exist. Fix the offending records and resend; do not blind-retry.
   - `400 Bad Request` means the request itself was malformed.
   - `429 Too Many Requests` means the organization exceeded 10,000 requests/hour.
     Read `x-ratelimit-reset` and wait until the top of the hour.
3. **Verify** — call `bulk-read-products` (`GET /{org_id}/products`) with a `filter`
   expression scoped to the identifiers you just wrote, paging with `page` and
   `per_page`. For a single product use `read-product-record`
   (`GET /{org_id}/products/{salsify:id}`).

## Rules

- **Replay safety**: `bulk-upsert-products` converges on the same end state when
  replayed with the same body. Salsify publishes **no `Idempotency-Key` header**, so
  never assume replay protection on any other write operation — see
  `conventions/salsify-conventions.yml`.
- **Batch, do not loop.** Prefer one `bulk-upsert-products` call over N
  `add-a-product` / `update-product` calls; the 10,000/hour limit is per organization
  and is shared with every other integration in that org.
- **Very large loads belong in imports.** Above a few thousand products, use the import
  pipeline (`skills/salsify-run-json-import.md`) instead of the write API.
- Salsify system fields are namespaced `salsify:` (`salsify:id`, `salsify:parent_id`,
  `salsify:destroyed_at`). Everything else is a customer-defined property.
- Errors are plain JSON (some endpoints return `text/plain`); Salsify does **not** use
  RFC 9457 `application/problem+json`. See `errors/salsify-problem-types.yml`.
