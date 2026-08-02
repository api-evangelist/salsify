---
name: Model Salsify records and properties
description: Define the property schema for a Salsify organization and load records against it, using the records surface rather than the product-only model.
api: openapi/salsify-write-operations-openapi.json
operations:
  - read-record-types
  - bulk-create-new-properties
  - read-property
  - update-property
  - bulk-upsert-properties
  - bulk-delete-properties
  - delete-property
  - create-record
  - bulk-create-records
  - bulk-upsert-records
  - read-record
  - bulk-read-records
---

# Model Salsify records and properties

Records are Salsify's generalized entity model: everything a product can do, plus
customer-defined record types. Do this before loading data, not after.

- Base URL: `https://app.salsify.com/api/v1/orgs`
- Auth: `Authorization` header with a user API key or OAuth 2.0 Bearer token.

## Steps

1. **Discover the record types** — `read-record-types`
   (`GET /{org_id}/record_types`). Every record belongs to one.
2. **Define the properties** — `bulk-create-new-properties`
   (`POST /{org_id}/properties`), or `bulk-upsert-properties`
   (`PUT /{organization_id}/properties/_upsert`) when re-running the schema load.
   Inspect an individual definition with `read-property`
   (`GET /{org_ID}/properties/{salsify:id}`) and amend with `update-property`.
3. **Load the records** — `create-record` (`POST /{org_id}/records/`) for one,
   `bulk-create-records` (`POST /{org_id}/records`) for a batch, or
   `bulk-upsert-records` (`PUT /{org_id}/records/_upsert`) for a re-runnable load.
   Filter records to a type on read with the `record_type` query parameter on
   `bulk-read-records`.
4. **Verify** — `read-record` (`GET /{org_id}/records/{salsify:id}`) or
   `bulk-read-records` (`GET /{org_id}/records`) with `filter`, `page`, `per_page`.

## Rules

- **Property IDs are load-bearing.** They appear in report headers, channel mappings and
  filter expressions. Deleting a property with `delete-property` or
  `bulk-delete-properties` breaks every downstream mapping that names it — treat those
  two operations as destructive and require explicit human confirmation.
- Load properties **before** records. A record whose payload names an undefined property
  fails with `422`.
- `bulk-upsert-properties` and `bulk-upsert-records` are the replay-safe operations;
  there is no `Idempotency-Key` contract on the create/update variants.
- `403` on `bulk-delete-records` means the authenticated user's Salsify permissions do
  not allow the deletion — not that the records are missing.
- Use a dedicated least-privilege integration user, as Salsify recommends, so a
  destructive schema call cannot be made with a human's full permissions.
