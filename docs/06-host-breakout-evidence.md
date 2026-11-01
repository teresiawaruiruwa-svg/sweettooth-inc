# Host breakout: outcome and evidence qualification

## Observed outcome
The repository includes direct screenshot evidence for both container-root access and host filesystem access:
- `evidence/screenshots/task 4 flag.PNG` shows Docker daemon access, entry into the `sweettoothinc` container, and `uid=0(root)` inside that container.
- `evidence/screenshots/task 5 flag.PNG` shows block-device identification, mounting `/dev/xvda1` at `/mnt/mountme`, listing the mounted root filesystem, and reading `/mnt/mountme/root/root.txt`.

The second screenshot supports host filesystem access; this is stronger evidence than a report-only claim. The flag values are intentionally not reproduced in this document.

## Reconciling the source notes
The final assessment report describes host filesystem mounting and retrieval of the host root flag (page 6). The assignment working notes state that the host-mount and final host-flag commands were not captured as executed in that session (page 8). However, the repository now contains `task 5 flag.PNG`, which visibly records the mount and host-side file read. The evidence register should therefore classify the host filesystem access as **screenshot-observed**, while retaining the discrepancy in the original notes as provenance context.

## Publication warning
The current `task 4 flag.PNG` and `task 5 flag.PNG` images visibly contain lab flag values and historical target details. They are useful as private verification evidence but are **not safe for a public portfolio repository in their current form**. Replace them with redacted copies before treating the public evidence set as sanitized. Do not recreate evidence and present it as contemporaneous.

Container root and host root are distinct contexts. The task 4 screenshot establishes container root; the task 5 screenshot establishes access to the mounted host root filesystem.