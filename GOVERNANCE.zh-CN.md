# 维护流程

[English](GOVERNANCE.md)

ARMHPC 目前由 [chens32](https://github.com/chens32) 一人维护。贡献者通过 Fork 和 PR 参与，维护者负责分类、合并、发行及安全报告。

## 变更

- 使用独立分支和 PR 修改 `main`。
- 必需检查通过，未解决的讨论处理完毕。
- 必需审批人数为 **0**，不要求 Code Owner 审批，也不要求最近推送由另一人批准。
- CODEOWNERS 标明负责范围，不要求唯一维护者审批自己的 PR。
- 依赖更新不自动合并，先审阅修改和相关检查结果。
- 主分支及发行 tag 的更新／删除受规则保护。Owner 可处理紧急规则调整，并在对应 PR 或维护报告记录原因。

## 发布

标题使用 `vMAJOR.MINOR.PATCH`。英文简述变更，链接简体中文 Markdown。记录源码提交及构建输入，在受控环境签名，先上传完整草稿，核对名称、大小及 SHA256 后发布。

- `armhpc-ota`：仅 Windows MSI、Linux 上位机 CLI tar.gz、签名 maintenance tar.xz。
- `armbian-hpc`：每个纳入发行的板卡提供一个 IMG.XZ 和一个系统 OTA TAR.XZ。
- 对应源码、许可证、依赖清单和构建来源放入约定包内或源码文档。保留旧发行载荷原字节及任务／包绑定；二进制修正使用新版本。
- 软件检查和实机结果分别记录，硬件验收字段随对应证据更新。尚未补齐的引导组件来源记录继续保留。

[仓库维护说明](https://github.com/ArmbianHPC/armhpc-ota/blob/main/docs/MAINTENANCE.zh-CN.md)介绍 CI 与签名边界。后续完整附件和来源核查就绪后可启用 GitHub 不可变发行。

## 日常

按可用时间每周查看新反馈、依赖和安全告警，每月复查权限及来源／下载链接，按修复需要发布，不承诺固定响应和发行日期。
