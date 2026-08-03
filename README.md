# 17TRACK

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

Package tracking REST API supporting 3,300+ global carriers for real-time shipment tracking, status updates, and delivery notifications.

## Overview

17TRACK provides a unified tracking API that aggregates shipment data from over 3,300 carriers worldwide. The API uses a webhook push mechanism to automatically deliver tracking updates to your endpoint, covering 9 main status categories and 27 sub-statuses.

## API Base URL

```
https://api.17track.net/track/v1
```

## Authentication

All requests require an API key passed as an HTTP header:

```
17token: YOUR_API_KEY
```

Obtain your API key from the Management Console under Settings > Security > Access Key.

## Key Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /register | Register tracking numbers |
| POST | /gettrackinfo | Get detailed tracking information |
| POST | /gettracklist | Get filtered tracking list |
| POST | /stoptrack | Stop tracking for completed shipments |
| POST | /retrack | Reactivate stopped tracking |
| POST | /deletetrack | Remove tracking numbers |
| POST | /changecarrier | Update carrier assignment |
| POST | /changeinfo | Update tracking metadata |
| POST | /push | Manually trigger webhook push |

## Rate Limits

- 3 requests per second per API key
- Maximum 40 tracking numbers per request
- HTTP 429 returned when rate limit exceeded

## Pricing

Plans are quota-based with annual validity (12-month periods):

| Plan | Quota | Price (CNY) |
|------|-------|-------------|
| Free Trial | 100 | Free |
| Basic | 10,000 | ¥299/year |
| Advanced | 50,000 | ¥1,299/year |
| Pro | 500,000 | ¥7,299/year |
| Flagship | 1,000,000 | ¥9,999/year |
| Custom | Custom | Contact sales |

## Resources

- [Developer Portal](https://www.17track.net/en/api)
- [API Documentation](https://asset.17track.net/api/document/v1_en/index.html)
- [Help Center](https://help.17track.net)
- [Carrier List](https://res.17track.net/asset/carrier/info/apicarrier.all.json)
- [API Support](mailto:apisupport@17track.net)
