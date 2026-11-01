# Container privilege escalation

The practical report records that the Docker CLI initially failed because client and daemon API versions did not match. The error indicated API version 1.38 was not supported by a client whose minimum supported version was 1.40. The assignment notes state that setting the Docker client's API version to match the server restored communication.

This was an interoperability issue; the underlying security concern was access to the Docker daemon from a low-privileged context.

The report records discovery of `influxdb:1.3.0` and `sweettoothinc:latest` images, followed by execution in the application container as root. It states that the container-root flag was retrieved; the flag is omitted.

A user able to control the Docker daemon may start or enter containers with permissions beyond those of the original account. The report includes a screenshot of the compatibility adjustment, image listing, container execution, and root identity (page 6). Add a redacted copy when available.
