# 安全策略

[English](SECURITY.md)

## 维护版本

安全修复面向最新稳定 ARMHPC 系列，目前为 1.2.x。旧版继续提供下载，是否回移修复逐项评估。软件发行不会改变各板卡实际的硬件验收记录。

## 私密报告漏洞

在对应仓库选择 **Security → Advisories → Report a vulnerability**：

- [armhpc-ota](https://github.com/ArmbianHPC/armhpc-ota/security/advisories/new)
- [armbian-hpc](https://github.com/ArmbianHPC/armbian-hpc/security/advisories/new)

说明受影响版本、板卡／配置、影响及最小复现步骤。只提供复现需要的资料，不包含真实签名私钥、SSH 私钥、密码、集群 token、完整设备备份或原始身份分区。未修复漏洞的利用细节和凭据不放入公开 Issue。

目前由一名志愿维护者处理报告，根据可用时间确认、调查并协调修复，不承诺固定响应或解决时限。修复准备就绪后，通过协调发布的安全公告说明受影响版本及修复版本。

## 安装与签名

全新镜像的公开初始登录为 `root` / `1`，登录后通过 `passwd` 设置自己的密码；已有设备 OTA 升级保留原登录配置。执行设备操作前核对 SSH 主机身份及签名包兼容性。

发行签名私钥保存在维护者受控的签名环境。公开 PR 工作流不接触发行私钥、设备凭据或实际节点。疑似签名私钥泄露请私密报告，以便协调可信密钥迁移。
