# 17TRACK

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
