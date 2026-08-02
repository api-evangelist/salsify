---
name: Run a Salsify JSON import end to end
description: Upload a JSON or JSON Lines file to a Salsify mount point, create an import from it, start a run, and poll or receive a webhook for completion.
api: openapi/salsify-non-v1-endpoints-openapi.json
operations:
  - create-a-mount-point
  - creating-a-json-import-from-a-mount-point
  - updating-an-import-to-point-at-a-new-mount-point
  - starting-an-import-run
  - getting-the-status-of-an-import-run
---

# Run a Salsify JSON import end to end

This is the bulk-ingestion path. Use it instead of the product/record write API when
loading large volumes.

- Base URL for these operations: `https://app.salsify.com/api/orgs` (the **non-v1**
  surface — note there is no `/v1` segment).
- Auth: `Authorization` header with a user API key or OAuth 2.0 Bearer token.
- File formats: JSON import format and JSON Lines import format. See
  https://developers.salsify.com/docs/json-import-format and
  https://developers.salsify.com/docs/json-lines-import-format

## Steps

1. **Create a mount point** — `create-a-mount-point`
   (`POST /{org_id}/imports/upload_mounts`). The 201 response returns an S3 `url` and a
   `form_data` object containing the pre-signed policy, credential, algorithm, date and
   signature.
2. **Upload the file** — POST the file directly to the returned `url` as a multipart form
   using every field in `form_data` verbatim. This request goes to AWS S3, not to
   Salsify, and is not authenticated with your Salsify token.
3. **Create the import** — `creating-a-json-import-from-a-mount-point`
   (`POST /{org_id}/imports`) referencing the mount point key. For a recurring
   FTP-sourced import Salsify documents `creating-a-json-import-from-ftp` at
   https://developers.salsify.com/reference/creating-a-json-import-from-ftp — note that
   operation is documented but is NOT present in any published OpenAPI document, so treat
   its request shape as docs-only.
4. **Start the run** — `starting-an-import-run`
   (`POST /{org_id}/imports/{import_id}/runs`).
5. **Wait for completion** — either:
   - poll `getting-the-status-of-an-import-run`
     (`GET /{org_id}/imports/runs/{import_run_id}`), or
   - configure an **import webhook** in the Salsify app so Salsify posts the completion
     payload to you. See `asyncapi/salsify-webhooks.yml`.
6. **Read the outcome.** The import webhook payload carries `result`, `summary`,
   `errors`, `total_error_count`, `error_log_url`, `import_id` and `import_url`.
   Always fetch `error_log_url` when `total_error_count > 0` — the `errors` array is a
   summary and one message can represent many rows.

## Rules

- To repoint an existing import at a fresh upload, use
  `updating-an-import-to-point-at-a-new-mount-point` rather than creating a new import.
- A webhook added to an import **after** it was created only takes effect on the next
  run — re-run the import to persist the change.
- Imports are asynchronous. Never treat the 2xx from `starting-an-import-run` as
  "the data is loaded".
- `400` on `creating-a-json-import-from-a-mount-point` or `starting-an-import-run`
  usually means the mount point key is wrong or the file was never uploaded.
