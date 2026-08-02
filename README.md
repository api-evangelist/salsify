# Salsify

Salsify is a product experience management (PXM) and supplier experience management (SXM)
platform used by brands, distributors and retailers to centralize product content, digital
assets and syndication to the digital shelf.

- Website: https://www.salsify.com/
- Developer hub: https://developers.salsify.com/
- API reference: https://developers.salsify.com/reference
- Status: https://status.salsify.com/

## API surface

| Surface | Base | Notes |
|---|---|---|
| REST | `https://app.salsify.com/api/v1/orgs` | Products, records, properties, digital assets, list membership |
| REST (non-v1) | `https://app.salsify.com/api/orgs` | Imports, upload mounts, export runs |
| GraphQL | `https://api.salsify.com/graphql` | Early access; accounts, organizations, configuration manifests. Introspection auth-gated |
| MCP | `https://app.salsify.com/mcp` | First-party remote MCP server; OAuth 2.1, `tools/list` auth-gated |
| Webhooks | configured in-app | Product change, digital asset change, import completion, channel notifications |

Three OpenAPI 3.1.0 documents (43 operations total) were harvested from the Salsify
developer hub and saved verbatim to `openapi/`.

## Artifacts

`openapi/` `graphql/` `mcp/` `well-known/` `llms/` `packages/` `overlays/` `conformance/`
`errors/` `lifecycle/` `scopes/` `authentication/` `security/` `conventions/` `changelog/`
`data-model/` `rate-limits/` `asyncapi/` `skills/` `agentic-access/`

## Not present

- **No A2A Agent Card.** `app.salsify.com` and `api.salsify.com` answer HTTP 200 with an
  HTML cookie-consent page for every unknown `/.well-known/*` path; `www.salsify.com` and
  `developers.salsify.com` return 404. No card was written.
- **No AsyncAPI.** Salsify has a real webhook surface but publishes no AsyncAPI document;
  the webhook catalog is captured in `asyncapi/salsify-webhooks.yml`.
- **No RFC 9116 `security.txt`**, no idempotency-key contract, no first-party CLI, no
  published sandbox, and no first-party general-purpose REST SDK.
