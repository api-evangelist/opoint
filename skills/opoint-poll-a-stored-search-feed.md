---
generated: '2026-10-07'
method: generated
name: poll-a-stored-search-feed
description: Register a search that Opoint matches against newly crawled articles, then pull the near-real-time feed forward
  in time with the from/next_from cursor.
api: openapi/opoint-openapi.yml
operations:
- storedsearch_create
- storedsearch_list
- storedsearch_feed_retrieve
source: Grounded in openapi/opoint-openapi.yml and https://api-docs.opoint.com/references/api; operationIds verified in the
  contract.
---

# Register a stored search and poll its feed

Register a search that Opoint matches against newly crawled articles, then pull the near-real-time feed forward in time with the from/next_from cursor.

## Auth
- `Authorization: Token <static token>` header (or `?token=`). See `authentication/opoint-authentication.yml`.

## Idempotency
- None documented: no Idempotency-Key; de-duplicate writes yourself. See `conventions/opoint-conventions.yml`.

## Steps
1. **Register the search** — `storedsearch_create` (`POST /storedsearch/`) with `search` (a search string; syntax is not validated here, so test it in M360 first) and optionally `access_group`, `get_old_articles`. Note the returned stored search id.
2. **Confirm it** — `storedsearch_list` (`GET /storedsearch/`, `limit` default 500, `offset`).
3. **Pull the feed** — `storedsearch_feed_retrieve` (`GET /storedsearch/feed/`) with `from` (Unix timestamp, required) and `interval` (120-1800 seconds, default 900); optional `format`, `num_art`, `topics`, `matches`, `equalgroup`, and the licensed `readership` / `textrazor`.
4. **Advance** — read `next_from` from the response and pass it as `from` on the next call, sleeping between calls; every document carries `stored_search_id` because all stored searches share one feed.

## Operations (from the contract)
- `storedsearch_create` — `POST /storedsearch/`; body schema `StoredSearchDetail` with fields `id` (required), `search` (required), `last_new_article` (required), `access_group`, `max_age`, `get_old_articles`, `use_syndicates`
- `storedsearch_list` — `GET /storedsearch/`; parameters: `limit` (query), `offset` (query)
- `storedsearch_feed_retrieve` — `GET /storedsearch/feed/`; parameters: `equalgroup` (query), `format` (query), `from` (query, required), `id` (query), `interval` (query), `matches` (query), `num_art` (query), `readership` (query), `textrazor` (query), `to` (query), `topics` (query)

## Errors
- 401 when the token is missing or wrong, 403 when the token is valid but has no access (the docs show both on `GET /`); standard HTTP codes otherwise. See `errors/opoint-problem-types.yml`.
