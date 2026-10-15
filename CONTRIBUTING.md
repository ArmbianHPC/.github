# Contributing to ARMHPC

[简体中文](CONTRIBUTING.zh-CN.md)

## Choose the repository

- `armhpc-ota`: controller UI/CLI, SSH/serial transport, signatures, upgrade state and maintenance.
- `armbian-hpc`: image composition, boot/storage integration, drivers, device commands and recovery.
- `.github`: organization profile and shared community guidance.

Use [Discussions](https://github.com/ArmbianHPC/armbian-hpc/discussions) for usage questions and design discussions. Report reproducible defects through the issue forms. Use the [security policy](SECURITY.md) for vulnerabilities.

## Submit a change

1. Open an issue or discussion for a substantial behavior or board change.
2. Fork the repository, create a focused branch and preserve existing work.
3. Follow the repository's build instructions. Explain the checks you ran and their limits; documentation-only changes can state that.
4. Keep English and Simplified Chinese user documentation consistent.
5. Open a PR describing the change, reason, compatibility and verification.

Keep public commands, `protocol: 1`, persistent task IDs and signed package bindings compatible unless an explicitly documented versioned migration is supplied. Changes to disk writing, boot selection, signatures, identity, network rollback or credentials need focused verification and a recovery path. Separate automated/simulated results from observations on a named board revision.

Do not submit private keys, passwords, cluster tokens, device backups, raw identity partitions, vendor MiniLoaders or firmware without established source/redistribution records. Redact diagnostic logs. Preserve original author, source and license notices; original contributions use the license declared by the affected file/repository.

The sole maintainer can merge their own PR after required checks pass and conversations are resolved. An additional approving reviewer and Code Owner approval are not required. See [governance](GOVERNANCE.md).
