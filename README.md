# World Time API

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
