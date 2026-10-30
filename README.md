# Forithmus

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

Forithmus builds foundation models for medical imaging (Zurich, Switzerland; pre-seed backed by Point Nine and e2vc). Its developer-facing product is the Forithmus Research Hub, a Challenge Platform where research teams host and enter medical-imaging benchmarks by submitting Docker containers or prediction files, with leaderboards, credits and compute tiers, collections, forums, and groups. The public REST API is served at https://research.forithmus.com/api and described by an OpenAPI 3.1.0 specification (172 paths, 213 operations across 24 tags: auth/2FA, challenges, phases, collections, submissions, leaderboard, credits, payments, forum, groups, and more). Authentication is Bearer JWT via email/password or Google OAuth, with a browser device flow used by the first-party `forithmus` CLI. Forithmus also publishes open model/dataset repositories (MR-RATE, VLM3D, FORA) on GitHub.

**Areas:** Medical Imaging · Radiology · Machine Learning · Foundation Models · Healthcare AI · Challenge Platform · Benchmarks · Research · Developer Tools

## Forithmus on APIs.io

Everything profiled for Forithmus is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/forithmus/](https://apis.io/providers/forithmus/)** — or go straight to one of the APIs or properties below.

### APIs (25)

- [Forithmus Admin API](https://apis.io/apis/forithmus/forithmus-admin-api/) — The admin API from Forithmus — 15 operation(s) for admin.
- [Forithmus Auth API](https://apis.io/apis/forithmus/forithmus-auth-api/) — The auth API from Forithmus — 13 operation(s) for auth.
- [Forithmus Challenges API](https://apis.io/apis/forithmus/forithmus-challenges-api/) — The challenges API from Forithmus — 7 operation(s) for challenges.
- [Forithmus Collections API](https://apis.io/apis/forithmus/forithmus-collections-api/) — The collections API from Forithmus — 15 operation(s) for collections.
- [Forithmus Credits API](https://apis.io/apis/forithmus/forithmus-credits-api/) — The credits API from Forithmus — 16 operation(s) for credits.
- [Forithmus Data Upload API](https://apis.io/apis/forithmus/forithmus-data-upload-api/) — The data-upload API from Forithmus — 8 operation(s) for data-upload.
- [Forithmus Forum API](https://apis.io/apis/forithmus/forithmus-forum-api/) — The forum API from Forithmus — 7 operation(s) for forum.
- [Forithmus Groups API](https://apis.io/apis/forithmus/forithmus-groups-api/) — The groups API from Forithmus — 10 operation(s) for groups.
- [Forithmus Health API](https://apis.io/apis/forithmus/forithmus-health-api/) — The Health API from Forithmus — 2 operation(s) for health.
- [Forithmus Images API](https://apis.io/apis/forithmus/forithmus-images-api/) — The images API from Forithmus — 1 operation(s) for images.
- [Forithmus Leaderboard API](https://apis.io/apis/forithmus/forithmus-leaderboard-api/) — The leaderboard API from Forithmus — 2 operation(s) for leaderboard.
- [Forithmus Members API](https://apis.io/apis/forithmus/forithmus-members-api/) — The members API from Forithmus — 7 operation(s) for members.
- [Forithmus Messages API](https://apis.io/apis/forithmus/forithmus-messages-api/) — The messages API from Forithmus — 5 operation(s) for messages.
- [Forithmus Notifications API](https://apis.io/apis/forithmus/forithmus-notifications-api/) — The notifications API from Forithmus — 3 operation(s) for notifications.
- [Forithmus Pages API](https://apis.io/apis/forithmus/forithmus-pages-api/) — The pages API from Forithmus — 3 operation(s) for pages.
- [Forithmus Payments API](https://apis.io/apis/forithmus/forithmus-payments-api/) — The payments API from Forithmus — 6 operation(s) for payments.
- [Forithmus Phases API](https://apis.io/apis/forithmus/forithmus-phases-api/) — The phases API from Forithmus — 6 operation(s) for phases.
- [Forithmus Resources API](https://apis.io/apis/forithmus/forithmus-resources-api/) — The resources API from Forithmus — 5 operation(s) for resources.
- [Forithmus Roles API](https://apis.io/apis/forithmus/forithmus-roles-api/) — The roles API from Forithmus — 6 operation(s) for roles.
- [Forithmus Search API](https://apis.io/apis/forithmus/forithmus-search-api/) — The search API from Forithmus — 1 operation(s) for search.
- [Forithmus Submissions API](https://apis.io/apis/forithmus/forithmus-submissions-api/) — The submissions API from Forithmus — 18 operation(s) for submissions.
- [Forithmus Timeline API](https://apis.io/apis/forithmus/forithmus-timeline-api/) — The timeline API from Forithmus — 2 operation(s) for timeline.
- [Forithmus Uploads API](https://apis.io/apis/forithmus/forithmus-uploads-api/) — The uploads API from Forithmus — 1 operation(s) for uploads.
- [Forithmus Users API](https://apis.io/apis/forithmus/forithmus-users-api/) — The users API from Forithmus — 8 operation(s) for users.
- [Forithmus 2 FA API](https://apis.io/apis/forithmus/forithmus-2-fa-api/) — The 2 FA API from Forithmus — 5 operation(s) for 2 fa.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [forithmus](https://apis.io/servers/forithmus/forithmus/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Forithmus Agentic Access](https://apis.io/agentic-access/forithmus/forithmus-agentic-access/)

#### Collections (25)

Postman and Open Collection request collections.

- [Forithmus Challenge Platform 2fa API](https://apis.io/collections/forithmus/open-forithmus-2fa-api/)
- [Forithmus Challenge Platform 2fa admin API](https://apis.io/collections/forithmus/open-forithmus-admin-api/)
- [Forithmus Challenge Platform 2fa auth API](https://apis.io/collections/forithmus/open-forithmus-auth-api/)
- [Forithmus Challenge Platform 2fa challenges API](https://apis.io/collections/forithmus/open-forithmus-challenges-api/)
- [Forithmus Challenge Platform 2fa collections API](https://apis.io/collections/forithmus/open-forithmus-collections-api/)
- [Forithmus Challenge Platform 2fa credits API](https://apis.io/collections/forithmus/open-forithmus-credits-api/)
- [Forithmus Challenge Platform 2fa data-upload API](https://apis.io/collections/forithmus/open-forithmus-data-upload-api/)
- [Forithmus Challenge Platform 2fa forum API](https://apis.io/collections/forithmus/open-forithmus-forum-api/)
- [Forithmus Challenge Platform 2fa groups API](https://apis.io/collections/forithmus/open-forithmus-groups-api/)
- [Forithmus Challenge Platform 2fa Health API](https://apis.io/collections/forithmus/open-forithmus-health-api/)
- [Forithmus Challenge Platform 2fa images API](https://apis.io/collections/forithmus/open-forithmus-images-api/)
- [Forithmus Challenge Platform 2fa leaderboard API](https://apis.io/collections/forithmus/open-forithmus-leaderboard-api/)
- [Forithmus Challenge Platform 2fa members API](https://apis.io/collections/forithmus/open-forithmus-members-api/)
- [Forithmus Challenge Platform 2fa messages API](https://apis.io/collections/forithmus/open-forithmus-messages-api/)
- [Forithmus Challenge Platform 2fa notifications API](https://apis.io/collections/forithmus/open-forithmus-notifications-api/)
- [Forithmus Challenge Platform 2fa pages API](https://apis.io/collections/forithmus/open-forithmus-pages-api/)
- [Forithmus Challenge Platform 2fa payments API](https://apis.io/collections/forithmus/open-forithmus-payments-api/)
- [Forithmus Challenge Platform 2fa phases API](https://apis.io/collections/forithmus/open-forithmus-phases-api/)
- [Forithmus Challenge Platform 2fa resources API](https://apis.io/collections/forithmus/open-forithmus-resources-api/)
- [Forithmus Challenge Platform 2fa roles API](https://apis.io/collections/forithmus/open-forithmus-roles-api/)
- [Forithmus Challenge Platform 2fa search API](https://apis.io/collections/forithmus/open-forithmus-search-api/)
- [Forithmus Challenge Platform 2fa submissions API](https://apis.io/collections/forithmus/open-forithmus-submissions-api/)
- [Forithmus Challenge Platform 2fa timeline API](https://apis.io/collections/forithmus/open-forithmus-timeline-api/)
- [Forithmus Challenge Platform 2fa uploads API](https://apis.io/collections/forithmus/open-forithmus-uploads-api/)
- [Forithmus Challenge Platform 2fa users API](https://apis.io/collections/forithmus/open-forithmus-users-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Forithmus Openapi Overlay](https://apis.io/overlays/forithmus/forithmus-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Forithmus Authentication](https://apis.io/security/forithmus/forithmus-authentication/)
- [Forithmus Domain Security](https://apis.io/security/forithmus/forithmus-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://forithmus.com)
- [Documentation](https://research.forithmus.com/getting-started)
- [Getting started](https://research.forithmus.com/getting-started)
- [Sign up](https://research.forithmus.com)
- [Blog](https://forithmus.com/news/)
- [GitHub](https://github.com/forithmus)

## API Evangelist rating

**Kin Score 26.9** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 42.4 |
| Contract governance | 4.5 |
| Operational transparency | 2.6 |
| Developer ergonomics | 28.0 |
| Access clarity | 0.0 |

**Agent readiness 25.6** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 12.5** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/forithmus/](https://apis.io/providers/forithmus/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Forithmus: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/forithmus/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
