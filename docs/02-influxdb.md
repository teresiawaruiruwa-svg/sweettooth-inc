# InfluxDB exploration

The report describes GET requests to the InfluxDB `/query` endpoint using cURL, database/query parameters, and JSON responses. Original target URLs and authentication material are omitted.

## Findings recorded in the report

| Exercise | Reported result |
|---|---|
| Water tank temperature at specified UTC timestamp | 22.5 |
| Highest mixer motor RPM | 4875 |
| System username found in database information | Redacted |
| Database account information | Redacted |

The water tank exercise queried the `water_tank` measurement in the `tanks` database at Unix timestamp `1621346400` (2021-05-18 14:00:00 UTC). The mixer exercise used an aggregation over `mixer_stats` in the `mixer` database to identify maximum RPM.

The report includes JSON output for these results (pages 3–4). Add redacted screenshots. Do not publish usernames, credentials, or full secret-bearing cURL commands.

The assessment demonstrated that operational telemetry can expose information useful for access to other systems.
