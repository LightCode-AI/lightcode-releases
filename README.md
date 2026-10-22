<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://lightcode.lcapi.online/lightcode/logo-white.svg">
  <img src="https://lightcode.lcapi.online/lightcode-logo-192.png" alt="Lightcode" width="80" height="80">
</picture>

# Lightcode

### 即开即用，立刻上手。

日常任务、编程开发，还是打造自己的 Agent，从这里开始。

**Light in. Code out.**

![Preview](https://img.shields.io/badge/Status-Preview-6799fe?style=flat-square)
![Windows x64](https://img.shields.io/badge/Platform-Windows_x64-181818?style=flat-square)
[![MIT License](https://img.shields.io/badge/License-MIT-181818?style=flat-square)](LICENSE)

[**下载 Windows 版 →**](https://github.com/LightCode-AI/lightcode-releases/releases/download/v0.2.1-alpha.5.20261022.2/Lightcode-0.2.1-alpha.5.20261022.2-win-x64-unsigned.exe)

[官网](https://lightcode.lcapi.online/lightcode) · [API 状态](https://status.lcapi.online/) · [版本与更新说明](https://github.com/LightCode-AI/lightcode-releases/releases) · [账号与订阅](https://lightcode.lcapi.online/lightcode/subscription) · [问题反馈](https://github.com/LightCode-AI/lightcode-releases/issues)

</div>

---

## 从想法到完成，让 Agent 接手

Lightcode 是基于 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) 定制的桌面 Agent。它可以读取和编辑文件、运行命令、拆分任务并跟进执行。通过 Lightcone AI 账号登录，即可使用订阅内的模型，无需自行配置 API Key。

| 能力 | 可以做什么 |
| :--- | :--- |
| **读写文件与编程** | 理解项目结构、查找代码、修改文件，并运行命令验证结果。 |
| **规划与协作** | 维护计划和待办，将子任务委派给其他 Agent。 |
| **模型选择** | 使用订阅支持的 Claude、GPT、Gemini 等模型，按模型能力选择思考强度。 |
| **技能与插件** | 沿用 DSH 的插件架构，按需扩展工具、技能与工作流。 |
| **权限与确认** | 根据当前权限策略执行操作，需要审批时先请求确认。 |

## 三步开始

1. **下载并安装**：从 [Releases](https://github.com/LightCode-AI/lightcode-releases/releases) 获取 Windows x64 安装包。
2. **登录并开通订阅**：在应用内点击登录，通过浏览器完成 Lightcone AI 授权；在[订阅页面](https://lightcode.lcapi.online/lightcode/subscription)开通 Lightcode 套餐。
3. **描述你的任务**：新建会话、选择订阅支持的模型，告诉 Lightcode 想完成什么。处理已有项目时，指定项目目录或相关文件。

> 可以这样开始：**“帮我理解这个项目，列出主要模块，再给出一个改进计划。”**

## 下载

| 平台 | 当前版本 | 安装包 |
| :--- | :--- | :--- |
| **Windows x64** | `0.2.1-alpha.5.20261022.2` · Preview | [下载 .exe · 约 274 MB](https://github.com/LightCode-AI/lightcode-releases/releases/download/v0.2.1-alpha.5.20261022.2/Lightcode-0.2.1-alpha.5.20261022.2-win-x64-unsigned.exe) |

Lightcode 目前处于预览阶段，功能持续迭代。当前安装包未进行代码签名，Windows 可能显示未知发布者提示。每个 Release 均附带版本说明和 SHA-256 校验文件。

> **建议更新到本版本。** 早期版本与 DeepSeek Harness 共用同一个 Electron 数据目录，两个应用无法同时运行；本版起 Lightcode 使用独立数据目录，可以同时启动。

### 最新变化

- **一键更新**：左下角账户栏右侧的更新按钮自动完成检查、下载、重启与安装，不再弹出原生确认框；新版本启动后显示一次更新完成页面，报告版本与更新说明。
- **多线路选择**：通用设置新增「API 线路」，可在中国大陆优化（默认）与 Cloudflare Anycast 之间切换。仅影响模型请求、用量查询与模型列表，登录不受影响，切换后无需重新登录。
- **侧边栏身份**：左下角显示昵称与头像，与个人资料一致；修改后立即生效。
- **可与 DeepSeek Harness 同时运行**：改用独立的应用数据目录，不再争抢单实例锁与缓存。

<details>
<summary>如何校验下载文件？</summary>

下载同一 Release 中的 `SHA256SUMS.txt`，在 PowerShell 中运行：

```powershell
Get-FileHash .\Lightcode-0.2.1-alpha.5.20261022.2-win-x64-unsigned.exe -Algorithm SHA256
```

将输出的 `Hash` 与校验文件中的值比较，两者应一致。当前版本的 SHA-256 为：

```
BB0A61831B28F6EB18CB5FD25B5D2349C2F818D3AEEEB92EA3784BB4D541352E
```

</details>

## 关于订阅

Lightcode 订阅使用 **5 小时 / 7 天** 两个独立的用量窗口，分别累计、分别重置。界面显示已用百分比、进度条和重置时间，不显示具体金额额度。任一窗口用尽后，需等待对应窗口恢复。

模型支持范围、消耗规则与套餐售价以[订阅页面](https://lightcode.lcapi.online/lightcode/subscription)为准。**Lightcode 订阅与 API 余额独立，不能互相抵扣。**

服务可用性与各渠道响应延迟可在 [status.lcapi.online](https://status.lcapi.online/) 查看，按分钟粒度公开最近 90 分钟的运行状况。

## 许可与致谢

感谢 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) 提供 Agent 框架。Lightcode 在其基础上定制，保留上游的 **Copyright © 2026 DeepSeek** 和 MIT 许可文本，详见 [LICENSE](LICENSE)。第三方组件适用各自的许可证，相关声明随安装包提供。

本仓库用于安装包分发，只保留 README、许可证和 Releases；应用源码在独立私有仓库中维护。

---

<div align="center">

**Lightcode · 即开即用，立刻上手。**

[下载桌面版](https://github.com/LightCode-AI/lightcode-releases/releases) · [访问官网](https://lightcode.lcapi.online/lightcode) · [API 状态](https://status.lcapi.online/)

</div>
