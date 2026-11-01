# Troubleshooting and lessons

- **Non-standard SSH port:** use discovered service information rather than assuming defaults.
- **Docker API mismatch:** matching client API version to the supported server version restored communication. Distinguish compatibility errors from network or authorization failures.
- **cURL option support:** the notes describe a Unix-socket option unavailable in the installed cURL version. Check local tool capabilities first.
- **SSH tunnel placement:** tunnel attempts were made from the wrong environment. Understand which machine owns each end of a tunnel.
- **Unnecessary package installation:** Docker was already present; an installation attempt failed due to a package conflict. Check installed tools before changing the environment.
- **Evidence gap:** the notes distinguish container privilege escalation from final host breakout, for which no execution transcript was captured.

Maintain contemporaneous logs. Do not report suggested commands as executed.
