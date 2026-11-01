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

## Evidence and publication status
Nine screenshots are present in `evidence/screenshots/`. The task 4 screenshot documents Docker daemon access and container-root execution. The task 5 screenshot documents mounting the host root filesystem and reading a host-side file.

**Important:** the current task 4 and task 5 screenshots expose lab flag values and historical target details. Keep original evidence privately and replace public copies with redacted versions before presenting this repository as sanitized. Never publish flags, credentials, target IPs, tokens, or unredacted source reports.

## Evidence qualification
The accompanying assignment notes say the final host-mount sequence was not captured in the original working session. The uploaded task 5 screenshot now provides direct visual evidence of the mount and host-side file read. The host filesystem access is therefore classified as screenshot-observed, while the original notes discrepancy is retained in `docs/06-host-breakout-evidence.md`.

This is an independent learning record, not an official TryHackMe publication.