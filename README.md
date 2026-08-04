# World Time API

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

APIs.json profile for World Time API — a free REST API providing current time, timezone information, UTC offset, DST status, and Unix epoch time for any timezone or IP address.

The original service (worldtimeapi.org) has been sunset. This profile covers its drop-in compatible successor at [timeapi.world](https://timeapi.world/), which is source-available, built on Cloudflare Workers, and supports 537 IANA timezones with p99 latency under 40ms.

## Key Endpoints

| Method | Path | Description |
|--------|------|-------------|
| GET | /api/timezone | List all supported timezones |
| GET | /api/timezone/{area}/{location} | Current time for a specific timezone |
| GET | /api/ip | Current time for the calling IP address |
| GET | /api/ip/{ip} | Current time for a given IPv4/IPv6 address |
| GET | /api/geo | Geolocation for the calling IP |
| GET | /api/geo/{ip} | Geolocation for a given IP address |

## Response Fields (DateTime)

- `datetime` — ISO 8601 current date and time
- `timezone` — IANA timezone identifier (e.g., `America/New_York`)
- `utc_offset` — UTC offset in ±HH:MM format
- `unixtime` — Seconds since Unix epoch
- `dst` — Boolean DST active status
- `dst_from` / `dst_until` — DST boundary timestamps
- `day_of_week`, `day_of_year`, `week_number` — Calendar info
- `client_ip` — Requesting client IP address

## Plans

| Plan | Price | Requests/month | Overage |
|------|-------|---------------|---------|
| Free | $0 | 20,000 | None (rejected) |
| Starter | $5 | 50,000 | $0.0003/req |
| Standard | $10 | 100,000 | $0.0002/req |
| Pro | $20 | 200,000 | $0.0001/req |
| Enterprise | Custom | 1M+ | Custom |

## Links

- Website: https://timeapi.world/
- Documentation: https://timeapi.world/
- Pricing: https://timeapi.world/pricing
- FAQ: https://timeapi.world/faq
- GitHub: https://github.com/sleeyax/world-time-api

## Maintainer

Kin Lane — kin@apievangelist.com
