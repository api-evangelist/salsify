---
name: Export a Salsify catalog and collect the result
description: Start an asynchronous Salsify export run scoped to a list or filter, poll it to completion, and retrieve the generated file.
api: openapi/salsify-non-v1-endpoints-openapi.json
operations:
  - start-export-run
  - get-export-status
---

# Export a Salsify catalog and collect the result

Use this whenever you need more data than a paged `bulk-read-products` call should
carry — full catalog snapshots, channel feeds, or scheduled extracts.

- Base URL: `https://app.salsify.com/api/orgs` (non-v1 surface).
- Auth: `Authorization` header with a user API key or OAuth 2.0 Bearer token.
- Format reference: https://developers.salsify.com/docs/response-guidelines
  (JSON export file format) and https://developers.salsify.com/docs/export-overview

## Steps

1. **Start the export** — `start-export-run` (`POST /{org_id}/export_runs`). Scope it
   with a filter expression or a saved list. Filter syntax:
   https://developers.salsify.com/reference/salsify-filtering-language-syntax
2. **Poll** — `get-export-status` (`GET /{org_id}/export_runs/{export_id}`) until the
   run reports completion. Poll on a backoff; every poll counts against the
   10,000 requests/hour organization limit.
3. **Download** the generated file from the URL the status response returns.

## Rules

- Exports are asynchronous. There is no synchronous "give me the whole catalog" call.
- `400` from either operation means a malformed filter or an unknown export ID.
- Do not run an export in a tight loop; the export surface is the correct tool for
  volume, and polling it aggressively is what actually exhausts the rate limit.
- Prefer exports over paging `bulk-read-products` past a few pages.
