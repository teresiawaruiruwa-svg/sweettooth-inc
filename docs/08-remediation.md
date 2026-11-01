# Findings and remediation

## Findings

| ID | Finding | Impact |
|---|---|---|
| F-01 | InfluxDB HTTP API exposed | Increased database attack surface |
| F-02 | Stored information useful for system access | Credential disclosure and lateral-movement risk |
| F-03 | SSH on non-standard port | Remote access path; port change is not a security control |
| F-04 | World-writable Docker socket | Low-privileged context could control daemon |
| F-05 | Docker API insufficiently restricted | Administrative container operations exposed |
| F-06 | Root inside application container | Container boundary weakened |
| F-07 | Host filesystem exposure reported | Potential host compromise; direct evidence incomplete in notes |

## Controls
- Do not mount Docker socket into ordinary application containers; never use world-writable permissions.
- Restrict daemon access; disable unauthenticated TCP exposure. If remote administration is needed, require mutual TLS and authorization.
- Run containers as non-root, drop unnecessary capabilities, use seccomp/MAC profiles, avoid privileged containers and broad host mounts, and prefer read-only filesystems.
- Restrict database interfaces to trusted networks, enforce least privilege, avoid storing reusable system credentials in telemetry, rotate exposed secrets, and keep software supported.
- Monitor unexpected Docker API connections, socket permission changes, new host mounts, anomalous database access, and unusual container lifecycle activity.

The critical failure was exposing a privileged Docker management interface to a low-privileged environment without adequate access controls.
