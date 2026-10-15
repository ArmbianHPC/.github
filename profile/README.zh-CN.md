# ARMHPC

[English](README.md)

面向 ARM 设备的模块化 Linux 固件与签名 OTA 管理项目。

ARMHPC 通过板卡配置组合通用设备管理组件。框架支持 ARM64／ARM32 组合配置，目前提供的 OECT、OESP 镜像为 ARM64。

## 项目

| 仓库 | 用途 | 下载 |
| --- | --- | --- |
| [armbian-hpc](https://github.com/ArmbianHPC/armbian-hpc) | 固件组合、板卡接入、Rescue A/B、SATA 安装与恢复。 | [镜像和系统 OTA](https://github.com/ArmbianHPC/armbian-hpc/releases/latest) |
| [armhpc-ota](https://github.com/ArmbianHPC/armhpc-ota) | 签名升级引擎及 Windows／Linux 上位机，通过 SSH/SFTP 或受支持的 USB 串口连接设备。 | [MSI、Linux CLI 和维护包](https://github.com/ArmbianHPC/armhpc-ota/releases/latest) |

## 开始使用

1. 阅读[设备兼容说明](https://github.com/ArmbianHPC/armbian-hpc/blob/main/docs/DEVICES.zh-CN.md)，选择对应镜像或 OTA 包。
2. 按设备说明完成安装并准备恢复入口。全新镜像使用 `root` / `1`，登录后执行 `passwd`。已有设备通过 OTA 升级保留原登录配置。
3. 使用上位机查询设备，安装匹配的签名维护包或系统包。

固件文件名包含版本、板卡、系统代号、内核、文件系统和编译日期。上位机软件与设备固件分别下载；操作前阅读[已知问题](https://github.com/ArmbianHPC/armbian-hpc/blob/main/docs/KNOWN-ISSUES.zh-CN.md)。

## 反馈与贡献

- [使用咨询和建议](https://github.com/ArmbianHPC/armbian-hpc/discussions)
- [上位机与升级引擎问题](https://github.com/ArmbianHPC/armhpc-ota/issues/new/choose)
- [固件与板卡问题](https://github.com/ArmbianHPC/armbian-hpc/issues/new/choose)
- [贡献说明](https://github.com/ArmbianHPC/.github/blob/main/CONTRIBUTING.zh-CN.md)
- [私密安全报告](https://github.com/ArmbianHPC/.github/blob/main/SECURITY.zh-CN.md)

目前由 [chens32](https://github.com/chens32) 维护。文档默认使用英文，并提供简体中文副本；欢迎使用任一语言提交贡献与硬件运行记录。

## 来源与许可证

原创代码与第三方组件采用各仓库记录的许可证。板卡固件输入及再分发记录见框架的[来源文档](https://github.com/ArmbianHPC/armbian-hpc/blob/main/docs/SOURCES.md)。ARMHPC 独立维护，并保留上游作者与来源声明。
