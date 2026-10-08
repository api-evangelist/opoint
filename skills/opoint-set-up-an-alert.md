---
generated: '2026-10-07'
method: generated
name: set-up-an-alert
description: Create an email alert over profiles and tags, preview its next send, activate it, and send it immediately or
  deactivate it.
api: openapi/opoint-openapi.yml
operations:
- alerts_create
- alerts_next_preview_create
- alerts_activate_create
- alerts_send_now_create
- alerts_deactivate_create
source: Grounded in openapi/opoint-openapi.yml and https://api-docs.opoint.com/references/api; operationIds verified in the
  contract.
---

# Create, preview and activate an alert

Create an email alert over profiles and tags, preview its next send, activate it, and send it immediately or deactivate it.

## Auth
- `Authorization: Token <static token>` header (or `?token=`). See `authentication/opoint-authentication.yml`.

## Idempotency
- None documented: no Idempotency-Key; de-duplicate writes yourself. See `conventions/opoint-conventions.yml`.

## Steps
1. **Create** — `alerts_create` (`POST /alerts/`).
2. **Preview** — `alerts_next_preview_create` (`POST /alerts/{id}/next/preview/`) to see what the next alert would contain before anything is sent.
3. **Activate** — `alerts_activate_create` (`POST /alerts/{id}/activate/`); `alerts_send_now_create` (`POST /alerts/{id}/send-now/`) sends immediately.
4. **Reverse** — `alerts_deactivate_create` (`POST /alerts/{id}/deactivate/`) stops it; there is no undo for a sent alert (see conventions/opoint-conventions.yml reversibility).

## Operations (from the contract)
- `alerts_create` — `POST /alerts/`; body schema `AlertCreate` with fields `id` (required), `url` (required), `subject`, `locale`, `schedule` (required), `profiles` (required), `recipients` (required), `smsRecipients`, `active`, `templateId` (required)
- `alerts_next_preview_create` — `POST /alerts/{id}/next/preview/`; parameters: `id` (path, required), `json` (query)
- `alerts_activate_create` — `POST /alerts/{id}/activate/`; parameters: `id` (path, required)
- `alerts_send_now_create` — `POST /alerts/{id}/send-now/`; parameters: `id` (path, required)
- `alerts_deactivate_create` — `POST /alerts/{id}/deactivate/`; parameters: `id` (path, required)

## Errors
- 401 when the token is missing or wrong, 403 when the token is valid but has no access (the docs show both on `GET /`); standard HTTP codes otherwise. See `errors/opoint-problem-types.yml`.
