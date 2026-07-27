# AI Collab Rules — 跨工具统一的 AI 编程协作规则系统

> **A unified AI coding collaboration rule system that works across all AI tools.**
> **一份规则，所有 AI 编程工具通用。下载即用，自动接入。**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-v1.0-green.svg)](#)
[![Languages](https://img.shields.io/badge/languages-中文%20%7C%20English-orange.svg)](#)

---

## ✨ 特性 | Features

**中文**：
- 🔄 **跨工具统一**：TRAE、WorkBuddy、CodeBuddy、Cursor、Copilot、Windsurf、Cline、Aider、Continue…… 一份规则，所有 AI 工具通用
- 🧬 **自我传播**：新 AI 工具读到 `AGENTS.md` 自动接入，无需手动配置
- 🤖 **自动引导**：首次使用时，AI 自动引导你填写个性化配置
- 🔒 **路径安全**：项目被复制/移动后自动重置敏感授权，防止信息泄露
- 📝 **实战驱动**：不是空架子，是踩坑踩出来的规则
- 🧹 **自管理**：版本同步、精简控制、时效管理，规则体系自己照顾自己

**English**:
- 🔄 **Cross-Tool Unified**: One rule set for TRAE, WorkBuddy, CodeBuddy, Cursor, Copilot, Windsurf, Cline, Aider, Continue, and more
- 🧬 **Self-Propagating**: New AI tools auto-join when they read `AGENTS.md` — no manual setup
- 🤖 **Auto-Guided**: On first use, AI guides you through personalized configuration
- 🔒 **Path-Safe**: Sensitive authorizations auto-reset when project is copied/moved
- 📝 **Battle-Tested**: Not theoretical — these rules were forged from real-world mistakes
- 🧹 **Self-Managing**: Version sync, bloat control, and staleness checks built-in

---

## 🚀 快速开始 | Quick Start

### 中文

3 步接入：

1. **下载**：将本项目的核心文件复制到你的项目根目录
2. **打开项目**：用你喜欢的 AI 编程工具打开项目
3. **完成引导**：AI 会自动引导你完成个性化配置

```bash
# 最简使用：只需要 3 个文件
AGENTS.md                    # 核心规则
USER_PROFILE_TEMPLATE.md     # 用户画像模板
README.md                    # 项目说明
```

详细步骤见 [QUICKSTART.md](QUICKSTART.md)。

### English

Get started in 3 steps:

1. **Download**: Copy the core files to your project root directory
2. **Open Project**: Open the project with your favorite AI coding tool
3. **Complete Setup**: AI will automatically guide you through configuration

```bash
# Minimal setup: only 3 files needed
AGENTS.md                    # Core rules
USER_PROFILE_TEMPLATE.md     # User profile template
README.md                    # Project description
```

See [QUICKSTART.md](QUICKSTART.md) for detailed instructions.

---

## 📁 文件结构 | File Structure

```
ai-collab-rules/
├── AGENTS.md                    # ⭐ 核心规则（真理源，带自我传播协议）| Core rules (source of truth)
├── USER_PROFILE_TEMPLATE.md     # 用户画像模板 | User profile template
├── README.md                    # 你正在读的文件 | You are here
├── QUICKSTART.md                # 快速上手指南 | Quick start guide
├── LICENSE                      # MIT 开源协议 | MIT license
├── .ai-rules/                   # AI 运行时配置 | AI runtime config
│   ├── path.lock.template       # 路径锁定文件模板 | Path lock template
│   └── README.md                # 目录说明 | Directory description
└── integrations/                # 各工具接入示例 | Tool integration examples
    ├── trae/README.md
    ├── workbuddy/SOUL.md
    ├── codebuddy/collaboration.md
    ├── cursor/README.md
    └── copilot/README.md
```

---

## 🎯 核心规则一览 | Core Rules Overview

### 文件管理铁律 | File Management Iron Rules

**中文**：
- 📂 **项目隔离**：每个项目一个独立大文件夹
- 🛡️ **系统盘保护**：下载、缓存、临时文件不准放系统盘
- 🔒 **原文件保护**：处理用户数据永远不修改原文件

**English**:
- 📂 **Project Isolation**: Each project gets its own dedicated folder
- 🛡️ **System Drive Protection**: No downloads, caches, or temp files on the system drive
- 🔒 **Original File Protection**: Never modify user's original data files

### 文件编辑红线 | File Editing Red Lines

**中文**：
- ❌ 永远不要用写入工具覆盖已有文件
- ❌ 永远不要批量删除文件
- ❌ 禁止递归删除命令（`rm -rf` 等）

**English**:
- ❌ NEVER overwrite existing files with write tools
- ❌ NEVER batch-delete files
- ❌ NEVER use recursive delete commands (`rm -rf`, etc.)

### 三层测试闭环 | Three-Layer Testing Loop

| 中文 | English |
|------|---------|
| 1. **单元验证**：改完立刻测 | 1. **Unit Test**: Test immediately after changes |
| 2. **边界陷阱**：主动找 bug | 2. **Edge Case**: Actively hunt for bugs |
| 3. **回归自检**：交付前最后一关 | 3. **Regression Check**: Final gate before delivery |

### 交付完全体验收 | Complete Delivery Checklist

**中文**：功能层 + 质量层 + 整洁层 + 安全层 = 完整交付

**English**: Functionality + Quality + Cleanliness + Security = Complete Delivery

---

## 🔧 支持的 AI 工具 | Supported AI Tools

| 工具 / Tool | 接入方式 / Integration | 状态 / Status |
|---|---------|------|
| TRAE | `.trae/rules/` 引用 AGENTS.md | ✅ |
| WorkBuddy | `.workbuddy/SOUL.md` 引用 | ✅ |
| CodeBuddy | `.codebuddy/rules/` 引用 | ✅ |
| Cursor | `.cursorrules` 引用 | ✅ |
| GitHub Copilot | `.github/copilot-instructions.md` | ✅ |
| 其他 AI 工具 / Other | 读取项目根目录 `AGENTS.md` | ✅ |

> 任何支持读取项目文件的 AI 工具，都能自动接入本规则系统。
>
> Any AI tool that can read project files can auto-join this rule system.

---

## 💡 为什么需要这个？ | Why Do You Need This?

### 中文

**痛点**：AI 编程工具越来越多，每个工具都要重新调教一遍规则——文件怎么放、代码怎么写、什么不能碰……太麻烦了。

**解决方案**：一套跨工具统一的规则系统。不管你用什么 AI 工具，打开项目就能：
1. 自动加载你的协作规则
2. 自动了解你的偏好
3. 自动遵守你的红线
4. 自动保持行为一致

**效果**：换工具 = 换个壳，行为习惯完全一致。

### English

**Pain Point**: AI coding tools are multiplying. Each tool needs its own rule configuration — how to organize files, how to write code, what not to touch... It's exhausting.

**Solution**: A unified, cross-tool rule system. No matter which AI tool you use, opening a project gives you:
1. Auto-loaded collaboration rules
2. Auto-detected user preferences
3. Auto-enforced red lines
4. Consistent behavior across all tools

**Result**: Switching tools = changing a shell, habits stay identical.

---

## 📚 规则体系 | Rule System

### 三层架构 | Three-Layer Architecture (Inspired by Aily)

| 中文 | English |
|------|---------|
| 1. **身份定位层**：我是谁？能干什么？ | 1. **Identity Layer**: Who am I? What can I do? |
| 2. **知识储备层**：我知道什么？从哪来？ | 2. **Knowledge Layer**: What do I know? Where from? |
| 3. **工具使用层**：我用什么干活？怎么用？ | 3. **Tool Layer**: What tools do I use? How? |

### 自我管理机制 | Self-Management Mechanisms

| 中文 | English |
|------|---------|
| 规则版本同步管理 | Rule version sync management |
| 规则膨胀自动精简 | Auto-simplification for rule bloat |
| 规则时效性定期复查 | Periodic staleness review |
| 路径变化安全检测 | Path-change security detection |

---

## 🤝 贡献 | Contributing

**中文**：

欢迎提交 Issue 和 Pull Request！

贡献原则：
- 优先添加实战中踩过的坑
- 规则要具体可执行，不要空泛口号
- 新增规则需标注日期和来源

**English**:

Issues and Pull Requests are welcome!

Contribution principles:
- Prioritize real-world pitfalls
- Rules must be specific and actionable, not vague slogans
- New rules should be dated and sourced

---

## 📄 许可证 | License

MIT License — 随便用，随便改，但请保留版权声明。
Use it freely, modify it freely, but keep the copyright notice.

---

## ⭐ 如果对你有帮助 | If This Helps You

**中文**：如果这个项目帮你节省了时间，点个 Star 支持一下吧！

**English**: If this project saved you time, please give it a Star!

---

**版本 / Version**：v1.0
**创建日期 / Created**：2024-01-01
**最后更新 / Last Updated**：2024-01-01
**许可证 / License**：MIT
**项目地址 / Repository**：https://github.com/mulouout/Agent-rules
