# Sweettooth Inc. — Database, Docker and Container Security Assessment

A technical portfolio case study documenting an authorized TryHackMe Sweettooth Inc. lab assessment.

> Authorized training-lab work only. Do not test systems without explicit permission.

## Coverage
- TCP service discovery and InfluxDB 1.3.0 identification
- InfluxDB HTTP query API and time-series exploration
- Credential exposure through stored operational data
- SSH access and container execution-context identification
- World-writable Docker socket and exposed Docker API
- Docker client/server API compatibility troubleshooting
- Container root and host filesystem boundary analysis
- Findings, remediation, and evidence qualification

## Documentation
- [Overview and scope](docs/00-overview.md)
- [Reconnaissance](docs/01-reconnaissance.md)
- [InfluxDB exploration](docs/02-influxdb.md)
- [Initial access and container context](docs/03-initial-access.md)
- [Docker socket and API](docs/04-docker-api.md)
- [Container privilege escalation](docs/05-container-privilege.md)
- [Host breakout and evidence](docs/06-host-breakout-evidence.md)
- [Troubleshooting](docs/07-troubleshooting.md)
- [Findings and remediation](docs/08-remediation.md)
- [Timeline](notes/timeline.md)
- [Evidence register](notes/evidence-register.md)

Add sanitized screenshots to `evidence/screenshots/`. Never commit flags, credentials, target IPs, tokens, or unredacted source reports.

## Evidence qualification
The final report states that host filesystem access and retrieval of the host flag were achieved. The accompanying assignment notes say the final host-mount sequence was not captured as executed in that session. This repository labels host breakout as **reported in the final report, but not independently verified by the accompanying session notes**. Do not present it as screenshot-verified unless original evidence is added.

This is an independent learning record, not an official TryHackMe publication.
