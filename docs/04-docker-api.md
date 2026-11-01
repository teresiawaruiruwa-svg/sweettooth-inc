# Docker socket and API exposure

The final report describes `/var/run/docker.sock` as present inside the container with world-writable permissions. It also records an exposed Docker daemon API endpoint.

A Docker socket is an administrative interface to the daemon. Access may permit inspection and management of containers, images, and processes. Because the daemon has host-level authority, unrestricted socket access can undermine the intended container boundary.

The assignment notes describe SSH local port forwarding from the AttackBox to reach the Docker API. The final report describes a local TCP endpoint on port 9090. The source documents do not consistently describe one remote endpoint mapping, so this record avoids asserting a unified topology.

## Defensive controls
- Do not mount the Docker socket into ordinary application containers.
- Never make the socket world-writable.
- Restrict daemon access to trusted administrators and controlled identities.
- Avoid exposing Docker API over TCP where possible.
- If remote administration is required, use mutual TLS and strict authorization.
- Monitor daemon access and unexpected container activity.
