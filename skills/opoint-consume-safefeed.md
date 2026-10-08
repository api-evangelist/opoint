---
generated: '2026-10-07'
method: generated
name: consume-safefeed
description: Inspect a SafeFeed, read its feed and last ids, and check its stats and logs through the api.opoint.com safefeeds
  operations.
api: openapi/opoint-openapi.yml
operations:
- safefeeds_list
- safefeeds_retrieve
- safefeeds_feed_retrieve
- safefeeds_lastids_list
- safefeeds_stats_retrieve
source: Grounded in openapi/opoint-openapi.yml and https://api-docs.opoint.com/references/api; operationIds verified in the
  contract.
---

# Consume a SafeFeed through the API

Inspect a SafeFeed, read its feed and last ids, and check its stats and logs through the api.opoint.com safefeeds operations.

## Auth
- `Authorization: Token <static token>` header (or `?token=`). See `authentication/opoint-authentication.yml`.

## Idempotency
- None documented: no Idempotency-Key; de-duplicate writes yourself. See `conventions/opoint-conventions.yml`.

## Steps
1. **List feeds** — `safefeeds_list` (`GET /safefeeds/`) then `safefeeds_retrieve` (`GET /safefeeds/{id}/`).
2. **Read the feed** — `safefeeds_feed_retrieve` (`GET /safefeeds/{id}/feed/`); the direct pull surface documented at https://api-docs.opoint.com/references/safefeed is `feed.opoint.com/safefeed.php?key=<key>&lastid=?` advanced with the `opoint_search_start` id of each response, `num_art` 1-5000.
3. **Track the cursor** — `safefeeds_lastids_list` (`GET /safefeeds/{id}/lastids/`) and `safefeeds_stats_retrieve` (`GET /safefeeds/{id}/stats/`).
4. **Prefer the official client** — the `opoint` PyPI package's `SafefeedClient` (asyncio or requests) manages lastid, batch size and request interval; see packages/opoint-packages.yml.

## Operations (from the contract)
- `safefeeds_list` — `GET /safefeeds/`
- `safefeeds_retrieve` — `GET /safefeeds/{id}/`; parameters: `id` (path, required)
- `safefeeds_feed_retrieve` — `GET /safefeeds/{id}/feed/`; parameters: `doc_format` (query), `format` (query), `id` (path, required), `lastid` (query), `num_art` (query)
- `safefeeds_lastids_list` — `GET /safefeeds/{id}/lastids/`; parameters: `id` (path, required)
- `safefeeds_stats_retrieve` — `GET /safefeeds/{id}/stats/`; parameters: `end_time` (query), `id` (path, required), `start_time` (query)

## Errors
- 401 when the token is missing or wrong, 403 when the token is valid but has no access (the docs show both on `GET /`); standard HTTP codes otherwise. See `errors/opoint-problem-types.yml`.
