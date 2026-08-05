# Movable Ink

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Movable Ink is a New York-headquartered marketing technology company that turns customer data into
personalized content across email, mobile and web. Its two products are **Studio** (composite images
and interactive content generated at open time) and **Da Vinci** (an AI decisioning layer that picks
what each customer sees).

- Website: https://movableink.com/
- Mobile SDK docs: https://sdk-mobile.movableink.com/
- GitHub: https://github.com/movableink
- Status: https://status.movableink.com/
- Trust Center: https://trust.movableink.com/

## API surface

| Surface | What it is | Contract |
|---|---|---|
| Customer Data API | Write-only behavioral-event collector, `POST https://collector.movableink-dmz.com/behavioral/{endpoint_key}`, HTTP Basic auth with credentials issued by the Movable Ink Solutions team | none published |
| Platform Identity | Auth0/OIDC tenant at `auth.movableink.com` fronting `app.movableink.com` | OIDC discovery + RFC 8414 metadata + JWKS (all public) |
| Mobile SDKs | iOS, Android, React Native, Cordova, Flutter, Expo | published to CocoaPods, Maven Central, npm and pub.dev |
| Studio toolchain | `movable` CLI, `cropduster`, `@movable/studio-utilities` | published to npm |

**No OpenAPI, AsyncAPI, GraphQL SDL, Postman collection, MCP server or A2A agent card was found** on
any Movable Ink host. Movable Ink's own API reference lives on `support.movableink.com`, which
requires an active tenant — the Zendesk help-center API returns `401` and anonymous browser requests
get a Cloudflare interstitial (`403`). What is public is `https://movableink.com/llms.txt`, the OIDC
discovery documents, the status page, and the Trust Center.

