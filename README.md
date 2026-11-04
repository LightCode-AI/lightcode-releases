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

[**下载 Windows 版 →**](https://github.com/LightCode-AI/lightcode-releases/releases/download/v0.2.1-rc.5.20261105.1/Lightcode-0.2.1-rc.5.20261105.1-win-x64-unsigned.exe)

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
| **Windows x64** | `0.2.1-rc.5.20261105.1` · Preview | [下载 .exe · 约 285 MB](https://github.com/LightCode-AI/lightcode-releases/releases/download/v0.2.1-rc.5.20261105.1/Lightcode-0.2.1-rc.5.20261105.1-win-x64-unsigned.exe) |

Lightcode 目前处于预览阶段，功能持续迭代。当前安装包未进行代码签名，Windows 可能显示未知发布者提示。每个 Release 均附带版本说明和 SHA-256 校验文件。

> **建议更新到本版本。** 从 `0.2.1-rc.5.20261031.1` 起可直接在应用内检查更新；更早版本需要手动安装一次。

### 最新变化

- **生图工具修复**：加载 `image-generation` 技能后，`generate_image` 在当前会话内常驻，不再因首次生图或空闲被卸载。
- **多生图模型支持**：未指定模型时按目录顺序选择，图片模型配额耗尽或临时不可用时自动尝试下一个；也可通过模型 ID 或显示名指定。
- **按需生图**：在对话中加载 `image-generation` 技能后，模型可生成图片并保存到工作区 `generated-images/`，再由界面展示；图片不会以 base64 进入上下文。
- **更稳的上下文压缩**：压缩请求由后台指定的专用非图片模型执行，并使用该模型的输出上限；图片模型不会进入普通对话模型列表，也不会被误选为压缩模型。
- **模型管理**：后台可编辑 Model ID，重命名会迁移授权与套餐权益；模型行支持图片输出开关与压缩模型单选。
- **应用内更新**：安装包已带更新配置，可通过 `releases/latest/download/nightly.yml` 检查并升级到后续版本。

<details>
<summary>如何校验下载文件？</summary>

下载同一 Release 中的 `SHA256SUMS.txt`，在 PowerShell 中运行：

```powershell
Get-FileHash .\Lightcode-0.2.1-rc.5.20261105.1-win-x64-unsigned.exe -Algorithm SHA256
```

将输出的 `Hash` 与校验文件中的值比较，两者应一致。当前版本的 SHA-256 为：

```
9F6854A692FB85F8CD53C70B2285DA66AE5CACC2B6DA7C32C5A1E77BFDFB1CA2
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
