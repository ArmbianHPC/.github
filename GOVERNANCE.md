# Maintenance workflow

[简体中文](GOVERNANCE.zh-CN.md)

ARMHPC currently has one maintainer: [chens32](https://github.com/chens32). Contributors use forks and PRs. The maintainer handles triage, merges, releases and security reports.

## Changes

- Use a focused branch and PR for changes to `main`.
- Required checks must pass and review conversations must be resolved.
- Required approving reviews: **0**. Code Owner approval and approval by a different last pusher are not required.
- CODEOWNERS identifies responsibility; it does not require the sole maintainer to approve their own PR.
- No automatic dependency-PR merging. Review the diff and relevant results before merging.
- Main and release-tag updates/deletions are protected. Emergency rule changes remain possible for the owner and should be recorded in the affected PR or maintenance report.

## Releases

Use `vMAJOR.MINOR.PATCH` titles. English notes briefly describe changes and link a Simplified Chinese Markdown copy. Build from recorded commits and inputs, sign in the controlled signing environment, upload all expected files to a draft, verify names/sizes/SHA256, then publish.

- `armhpc-ota`: exactly Windows MSI, Linux host CLI tar.gz and signed maintenance tar.xz.
- `armbian-hpc`: one IMG.XZ and one system OTA TAR.XZ per included board.
- Put required sources, licenses, dependency inventory and build provenance inside the agreed packages or source documentation. Preserve old published payload bytes and task/package bindings; corrections to binary content use a new version.
- Record software checks and actual device results separately. Hardware acceptance fields change only with the corresponding evidence. Keep unresolved boot-component provenance visible in source records.

The [repository maintenance guides](https://github.com/ArmbianHPC/armhpc-ota/blob/main/docs/MAINTENANCE.md) document CI and signing boundaries. Future releases can use GitHub immutable releases once the complete package and source review is ready.

## Routine

Review new reports and dependency/security alerts weekly as availability permits; review access and source/download links monthly. Release corrections as needed. Response and release dates are not guaranteed.
