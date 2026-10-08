---
generated: '2026-10-07'
method: generated
name: search-the-archive
description: Run a one-off or historical search against the Opoint archive with the Opoint search syntax, and page through
  the results with the context cursor.
api: openapi/opoint-openapi.yml
operations:
- search_create
source: Grounded in openapi/opoint-openapi.yml and https://api-docs.opoint.com/references/api; operationIds verified in the
  contract.
---

# Search the Opoint news archive

Run a one-off or historical search against the Opoint archive with the Opoint search syntax, and page through the results with the context cursor.

## Auth
- `Authorization: Token <static token>` header (or `?token=`). See `authentication/opoint-authentication.yml`.

## Idempotency
- None documented: no Idempotency-Key; de-duplicate writes yourself. See `conventions/opoint-conventions.yml`.

## Steps
1. **Build the search body** — a `searchterm` (Opoint search syntax, e.g. `header:spotify`, filters such as `{"type":"lang","id":"no"}`) and `params`: `requestedarticles` (default 10), `oldest` (Unix timestamp), `main.header/summary/text` to select returned parts, `context: ""` on the first page.
2. **Search** — `search_create` (`POST /search/`, trailing slash required) with `Authorization: Token <token>` and `Content-Type: application/json`.
3. **Page** — when the response `context` is non-empty, resend the same search with that `context` to get the next batch; stop when it comes back empty.
4. **Do not poll this endpoint for new hits** — the FAQ says the Search API should not be used as a live feed; register a stored search instead (see opoint-poll-a-stored-search-feed).

## Operations (from the contract)
- `search_create` — `POST /search/`; parameters: `format` (query); body schema `Search` with fields `params`, `searchterm`, `expressions`, `use_raw_query`, `default_search`

## Errors
- 401 when the token is missing or wrong, 403 when the token is valid but has no access (the docs show both on `GET /`); standard HTTP codes otherwise. See `errors/opoint-problem-types.yml`.
