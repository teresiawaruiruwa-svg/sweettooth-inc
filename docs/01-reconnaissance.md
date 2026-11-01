# Reconnaissance and service discovery

The report records a full TCP port scan with service/version detection and default scripts, generalized here as:

```bash
nmap -sC -sV -p- <LAB_TARGET>
```

## Services recorded

| Port | Service / role |
|---|---|
| 22 | SSH |
| 8086 | InfluxDB HTTP API |
| 8088 / 9090 | Docker-related service/API exposure noted during assessment |
| 2222 | Alternate SSH |

The service identified on TCP/8086 was InfluxDB 1.3.0. This directed the next stage toward the HTTP query API and stored measurements.

The source documents contain differing historical target addresses and service details. This record does not assert one fixed network topology.
