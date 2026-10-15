# Security policy

[简体中文](SECURITY.zh-CN.md)

## Supported versions

Security fixes target the latest stable ARMHPC release series, currently 1.2.x. Older releases remain available; backports are assessed individually. A software release does not change board-specific hardware acceptance records.

## Report a vulnerability privately

Use **Security → Advisories → Report a vulnerability** in the affected repository:

- [armhpc-ota](https://github.com/ArmbianHPC/armhpc-ota/security/advisories/new)
- [armbian-hpc](https://github.com/ArmbianHPC/armbian-hpc/security/advisories/new)

Include the affected version, board/profile, impact and minimal reproduction. Send only the information needed to reproduce the issue. Never include real signing keys, SSH private keys, passwords, cluster tokens, full device backups or raw identity partitions. Do not post an unfixed exploit or credentials in a public issue.

One volunteer maintainer handles reports. We acknowledge, investigate and coordinate fixes as availability permits; no fixed response or resolution time is promised. Coordinated advisories identify affected and fixed versions after a correction is ready.

## Installation and signing

Fresh supplied images use the documented initial login `root` / `1`. Set your password with `passwd` after signing in; OTA preserves an existing device's login configuration. Check SSH host identity and signed package compatibility before device operations.

Release signing keys remain in the maintainer's controlled signing environment. Public PR workflows do not receive release keys, device credentials or access to real nodes. Report suspected signing-key exposure privately so a verified trust-key migration can be coordinated.
