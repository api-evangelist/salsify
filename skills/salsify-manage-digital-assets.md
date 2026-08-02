---
name: Manage Salsify digital assets
description: Create, read, refresh, update and delete digital asset metadata in a Salsify organization, and subscribe to asset change webhooks.
api: openapi/salsify-write-operations-openapi.json
operations:
  - create-a-digital-asset-metadata
  - add-multiple-digital-assets
  - get-digital-asset
  - bulk-read-digital-assets
  - refresh-digital-assets
  - update-digital-asset-metadata
  - update-multiple-digital-assets
  - bulk-upsert-digital-assets
  - delete-multiple-digital-assets
---

# Manage Salsify digital assets

Digital assets are the images, videos and documents products reference on the digital
shelf. They carry their own metadata and their own change webhooks.

- Base URL: `https://app.salsify.com/api/v1/orgs`
- Auth: `Authorization` header with a user API key or OAuth 2.0 Bearer token.

## Steps

1. **Create** — `create-a-digital-asset-metadata`
   (`POST /{organization_id}/digital_assets`) for one asset, or
   `add-multiple-digital-assets` (`POST /{org_id}/digital_assets`) for a batch.
2. **Read** — `get-digital-asset` (`GET /{org_id}/digital_assets/{asset_id}`) for one,
   or `bulk-read-digital-assets` (`GET /{org_id}/digital_assets`) with `filter`, `page`
   and `per_page` for many.
3. **Refresh from source** — `refresh-digital-assets`
   (`POST /{org_id}/digital_assets/refresh`) when the underlying file changed at its
   origin URL and Salsify needs to re-fetch it.
4. **Update** — `update-digital-asset-metadata`
   (`PUT /{org_id}/digital_assets/{salsify:id}`) for one,
   `update-multiple-digital-assets` (`PUT /{org_id}/digital_assets`) for a batch, or
   `bulk-upsert-digital-assets` (`PUT /{organization_id}/digital_assets/_upsert`) when
   you do not know whether the assets exist.
5. **Delete** — `delete-multiple-digital-assets` (`DELETE /{org_id}/digital_assets`).
6. **Subscribe** — configure a digital-asset webhook in the Salsify app to receive
   `add` / `change` / `remove` notifications. See `asyncapi/salsify-webhooks.yml`.

## Rules

- Deletes are **soft** from the consumer's point of view: destroyed assets appear in
  webhooks and exports with `salsify:destroyed_at` set to the delete date. Check that
  field before treating a `remove` trigger as "the asset left my list".
- `bulk-upsert-digital-assets` is the only replay-safe write here. Salsify publishes no
  `Idempotency-Key` header.
- Webhook delivery is coalesced: two rapid metadata edits may arrive as one webhook, and
  an edit that returns an asset to its original state may fire none. Never treat webhook
  count as an event count.
- Ordering is guaranteed only per asset, never across assets.
- Verify every webhook's X.509 / SHA-256 signature and ignore requests that fail
  verification. See
  https://developers.salsify.com/reference/webhook-signature-verification-algorithm
