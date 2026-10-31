# Opoint

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Opoint is a Copenhagen-based real-time global news data provider in the Infomedia group. It crawls news from more than 250,000 online sources in 135 languages, and sells that data to media-monitoring, compliance (adverse media, AML/KYC, due diligence), financial-services and business-intelligence buyers. Developers reach it through the Opoint REST API on api.opoint.com (archive Search, StoredSearch near-real-time feeds, Alerts, Profiles, Tags, Tracking of press releases, Analytics, Trends), the SafeFeed pull feed on feed.opoint.com, and a suggestion server on suggest.api.opoint.com that translates names and URLs into filter ids, with enrichment such as topics and entities, readership estimates and sentiment. An OpenAPI 3.1 contract is served at api.opoint.com/schema/ and a Python client library is published on PyPI.

**Areas:** Company · News · News Data · Media Monitoring · Search · Feed · Adverse Media · Compliance · Financial Services · Content Tracking · Denmark

## Opoint on APIs.io

Everything profiled for Opoint is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/opoint/](https://apis.io/providers/opoint/)** — or go straight to one of the APIs or properties below.

### APIs (26)

- [Opoint Suggestion Server API](https://apis.io/apis/opoint/opoint-suggestion-server-api/) — A search engine for filters that translates site names, URLs, countries, languages and other filter names in natural language into the ids the Opoint search…
- [Opoint SafeFeed API](https://apis.io/apis/opoint/opoint-safefeed-api/) — Pull feed of real-time global news data at feed.opoint.com/safefeed.php, advanced with a lastid cursor taken from the opoint_search_start element of each…
- [Opoint Agreements API](https://apis.io/apis/opoint/opoint-agreements-api/) — The agreements API from Opoint — 4 operation(s) for agreements.
- [Opoint Alert Info API](https://apis.io/apis/opoint/opoint-alert-info-api/) — The alert_info API from Opoint — 1 operation(s) for alert_info.
- [Opoint Alerts API](https://apis.io/apis/opoint/opoint-alerts-api/) — The alerts API from Opoint — 15 operation(s) for alerts.
- [Opoint Analytics API](https://apis.io/apis/opoint/opoint-analytics-api/) — The analytics API from Opoint — 21 operation(s) for analytics.
- [Opoint Auth API](https://apis.io/apis/opoint/opoint-auth-api/) — The auth API from Opoint — 5 operation(s) for auth.
- [Opoint Customers API](https://apis.io/apis/opoint/opoint-customers-api/) — The customers API from Opoint — 6 operation(s) for customers.
- [Opoint Folders API](https://apis.io/apis/opoint/opoint-folders-api/) — The folders API from Opoint — 4 operation(s) for folders.
- [Opoint Invite API](https://apis.io/apis/opoint/opoint-invite-api/) — The invite API from Opoint — 6 operation(s) for invite.
- [Opoint Licenses API](https://apis.io/apis/opoint/opoint-licenses-api/) — The licenses API from Opoint — 1 operation(s) for licenses.
- [Opoint Mailstatus API](https://apis.io/apis/opoint/opoint-mailstatus-api/) — The mailstatus API from Opoint — 10 operation(s) for mailstatus.
- [Opoint Notifications API](https://apis.io/apis/opoint/opoint-notifications-api/) — The notifications API from Opoint — 3 operation(s) for notifications.
- [Opoint Profiles API](https://apis.io/apis/opoint/opoint-profiles-api/) — The profiles API from Opoint — 16 operation(s) for profiles.
- [Opoint Reports API](https://apis.io/apis/opoint/opoint-reports-api/) — The reports API from Opoint — 2 operation(s) for reports.
- [Opoint Safefeeds API](https://apis.io/apis/opoint/opoint-safefeeds-api/) — The safefeeds API from Opoint — 6 operation(s) for safefeeds.
- [Opoint Search API](https://apis.io/apis/opoint/opoint-search-api/) — The search API from Opoint — 6 operation(s) for search.
- [Opoint Sites API](https://apis.io/apis/opoint/opoint-sites-api/) — The sites API from Opoint — 18 operation(s) for sites.
- [Opoint stored search API](https://apis.io/apis/opoint/opoint-stored-search-api/) — The stored search API from Opoint — 4 operation(s) for stored search.
- [Opoint Support API](https://apis.io/apis/opoint/opoint-support-api/) — The support API from Opoint — 1 operation(s) for support.
- [Opoint Tags API](https://apis.io/apis/opoint/opoint-tags-api/) — The tags API from Opoint — 10 operation(s) for tags.
- [Opoint Templates API](https://apis.io/apis/opoint/opoint-templates-api/) — The templates API from Opoint — 3 operation(s) for templates.
- [Opoint Tracking API](https://apis.io/apis/opoint/opoint-tracking-api/) — The tracking API from Opoint — 4 operation(s) for tracking.
- [Opoint Trends API](https://apis.io/apis/opoint/opoint-trends-api/) — The trends API from Opoint — 5 operation(s) for trends.
- [Opoint Users API](https://apis.io/apis/opoint/opoint-users-api/) — The users API from Opoint — 5 operation(s) for users.
- [Opoint Watchqueries API](https://apis.io/apis/opoint/opoint-watchqueries-api/) — The watchqueries API from Opoint — 2 operation(s) for watchqueries.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [mcp-oauth-server (WordPress MCP Adapter default server on opoint.com)](https://apis.io/servers/opoint/mcp-oauth-server-wordpress-mcp-adapter-default-server-on-opoint-com/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Opoint Agentic Access](https://apis.io/agentic-access/opoint/opoint-agentic-access/)

#### JSON Schema (6)

The data models the API reads and writes.

- [Agreement](https://apis.io/schemas/opoint/opoint-agreement/)
- [AgreementList](https://apis.io/schemas/opoint/opoint-agreement-list/)
- [AlertDetail](https://apis.io/schemas/opoint/opoint-alert-detail/)
- [PatchedSiteRequest](https://apis.io/schemas/opoint/opoint-patched-site-request/)
- [ProfileDetail](https://apis.io/schemas/opoint/opoint-profile-detail/)
- [SiteRequest](https://apis.io/schemas/opoint/opoint-site-request/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Opoint Context](https://apis.io/jsonld/opoint/opoint-context/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Opoint Openapi Overlay](https://apis.io/overlays/opoint/opoint-openapi-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Opoint API Rules](https://apis.io/rules/opoint/opoint-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Opoint Authentication](https://apis.io/security/opoint/opoint-authentication/)
- [Opoint Domain Security](https://apis.io/security/opoint/opoint-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Opoint Plans Pricing](https://apis.io/plans/opoint/opoint-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Opoint Rate Limits](https://apis.io/rate-limits/opoint/opoint-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.opoint.com)
- [Documentation](https://api-docs.opoint.com/)
- [Getting started](https://api-docs.opoint.com/guides/getting-started-with-searching)
- [API reference](https://api-docs.opoint.com/references/api)
- [Support](https://support.opoint.com/)
- [Blog](https://opoint.com/resources/articles)
- [Privacy policy](https://opoint.com/privacy-policy)
- [Status](https://status.opoint.com/)

## API Evangelist rating

**Kin Score 44.2** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 63.4 |
| Contract governance | 22.0 |
| Operational transparency | 15.8 |
| Developer ergonomics | 56.5 |
| Access clarity | 23.7 |

**Agent readiness 46.0** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | platform (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly (partial credit) |

**Regulatory alignment 20.6** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/opoint/](https://apis.io/providers/opoint/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Opoint: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/opoint/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
