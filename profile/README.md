# ARMHPC

[简体中文](README.zh-CN.md)

Modular Linux firmware and signed OTA management for ARM devices.

ARMHPC combines reusable device-management components with explicit board profiles. The framework supports ARM64 and ARM32 composition; the currently supplied OECT and OESP images are ARM64.

## Projects

| Repository | Purpose | Downloads |
| --- | --- | --- |
| [armbian-hpc](https://github.com/ArmbianHPC/armbian-hpc) | Firmware composition, board integration, Rescue A/B, SATA installation and recovery. | [Images and system OTA](https://github.com/ArmbianHPC/armbian-hpc/releases/latest) |
| [armhpc-ota](https://github.com/ArmbianHPC/armhpc-ota) | Signed upgrade engine and Windows/Linux controllers using SSH/SFTP or supported USB serial interfaces. | [MSI, Linux CLI and maintenance](https://github.com/ArmbianHPC/armhpc-ota/releases/latest) |

## Start here

1. Read the [device compatibility guide](https://github.com/ArmbianHPC/armbian-hpc/blob/main/docs/DEVICES.md) and select the matching image or OTA package.
2. Follow the device's installation and recovery instructions. Fresh supplied images use `root` / `1`; run `passwd` after signing in. OTA retains an existing device's login configuration.
3. Use the controller to query the device and install the matching signed maintenance or system package.

Firmware filenames identify version, board, distribution, kernel, filesystem and build date. Software and firmware have separate download packages. Read [known issues](https://github.com/ArmbianHPC/armbian-hpc/blob/main/docs/KNOWN-ISSUES.md) before changing a device.

## Get help and contribute

- [Questions and ideas](https://github.com/ArmbianHPC/armbian-hpc/discussions)
- [Controller and upgrade-engine issues](https://github.com/ArmbianHPC/armhpc-ota/issues/new/choose)
- [Firmware and board issues](https://github.com/ArmbianHPC/armbian-hpc/issues/new/choose)
- [Contribution guide](https://github.com/ArmbianHPC/.github/blob/main/CONTRIBUTING.md)
- [Private security reporting](https://github.com/ArmbianHPC/.github/blob/main/SECURITY.md)

The project is maintained by [chens32](https://github.com/chens32). English is the default documentation language, with Simplified Chinese copies. Contributions and hardware reports in either language are welcome.

## Sources and licenses

Original code and third-party components retain the licenses documented in each repository. Board-specific firmware inputs and redistribution records are listed in the framework's [source documentation](https://github.com/ArmbianHPC/armbian-hpc/blob/main/docs/SOURCES.md). ARMHPC is independently maintained and preserves upstream author and source attribution.
