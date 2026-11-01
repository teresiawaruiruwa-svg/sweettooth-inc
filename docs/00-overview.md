# Overview and scope

Sweettooth Inc. follows a chain from network reconnaissance and InfluxDB exploration to initial access, container enumeration, Docker daemon exposure, and analysis of container/host security boundaries.

```text
Network reconnaissance -> InfluxDB HTTP API -> Stored account information -> SSH access
-> Low-privileged container shell -> Docker socket/API exposure -> Docker control
-> Container root -> Host filesystem boundary assessment
```

## Learning objectives
1. Identify network services and versions.
2. Explore a time-series database through its HTTP API.
3. Understand how stored operational data can expose credentials.
4. Distinguish a container shell from a host shell.
5. Recognize the significance of Docker socket access.
6. Diagnose Docker client/server API compatibility problems.
7. Explain why Docker daemon control can undermine container isolation.
8. Recommend database and container security controls.

Evidence labels: **Observed** means visible in captured output; **Reported** means stated in the final report; **Inferred** means supported but not directly proven; **Not verified** means source material lacks sufficient evidence.
