# 快速上手指南 | Quick Start Guide

> **1 分钟让所有 AI 工具都遵守你的规则。**
> **Get all your AI tools following your rules in 1 minute.**

---

## ⏱️ 1 分钟快速接入 | 1-Minute Quick Start

### 中文

#### 第 1 步：复制核心文件（10 秒）

将以下文件复制到你的项目根目录：

```
你的项目/
├── AGENTS.md                    ← 复制这个
├── USER_PROFILE_TEMPLATE.md     ← 复制这个
└── README.md                    ← 可选（如果你的项目已有 README）
```

只需要 `AGENTS.md` 就能工作，其他文件是辅助的。

#### 第 2 步：用 AI 工具打开项目（5 秒）

用你常用的 AI 编程工具打开项目目录：
- TRAE → 打开工作区
- Cursor → 打开文件夹
- Copilot → 打开仓库
- 其他 → 打开项目目录

#### 第 3 步：完成引导配置（~45 秒）

AI 会自动检测到这是首次使用，引导你填写：
1. 怎么称呼你？
2. 常用技术栈？
3. 偏好的沟通风格？
4. 特殊习惯或规则？

回答几个问题就完成了。

### English

#### Step 1: Copy Core Files (10 seconds)

Copy these files to your project root:

```
your-project/
├── AGENTS.md                    ← Copy this
├── USER_PROFILE_TEMPLATE.md     ← Copy this
└── README.md                    ← Optional (if you already have one)
```

Only `AGENTS.md` is required — the rest are optional enhancements.

#### Step 2: Open Project with AI Tool (5 seconds)

Open the project directory with your AI coding tool:
- TRAE → Open Workspace
- Cursor → Open Folder
- Copilot → Open Repository
- Others → Open project directory

#### Step 3: Complete Guided Setup (~45 seconds)

AI will auto-detect first-time use and guide you through:
1. What should I call you?
2. Your preferred tech stack?
3. Communication style?
4. Any special rules or habits?

Just answer a few questions and you're done.

---

## 📋 接入清单 | Setup Checklist

### ✅ 必须文件 | Required Files

| 文件 / File | 必须 / Required | 作用 / Purpose |
|------|------|------|
| `AGENTS.md` | ✅ 是 / Yes | 核心规则，AI 读到就自动接入 / Core rules, AI auto-joins on read |

### ⚙️ 推荐文件 | Recommended Files

| 文件 / File | 必须 / Required | 作用 / Purpose |
|------|------|------|
| `USER_PROFILE_TEMPLATE.md` | ⭐ 推荐 / Recommended | 填写后改名为 `USER_PROFILE.md` / Rename to `USER_PROFILE.md` after filling |
| `README.md` | ⭐ 推荐 / Recommended | 项目说明，AI 会读取了解项目背景 / AI reads this for project context |

### 🔧 可选文件（进阶）| Optional Files (Advanced)

| 文件 / File | 必须 / Required | 作用 / Purpose |
|------|------|------|
| `.ai-rules/` | 🔧 可选 / Optional | AI 运行时配置目录 / AI runtime config directory |
| `integrations/` | 🔧 可选 / Optional | 各工具的接入示例 / Tool integration examples |

---

## 🔌 各工具接入方式 | Tool Integration Methods

### TRAE

**中文**：将以下内容添加到项目的 `.trae/rules/` 目录下的规则文件中：

**English**: Add the following to a rule file in `.trae/rules/`:

```markdown
本项目所有规则以项目根目录下的 AGENTS.md 为准。
请先读取 AGENTS.md，再读取 USER_PROFILE.md（如果存在）。
All rules are defined in AGENTS.md at the project root.
Read AGENTS.md first, then USER_PROFILE.md if it exists.
```

详细说明见 / See: [integrations/trae/README.md](integrations/trae/README.md)

### WorkBuddy

创建 `.workbuddy/SOUL.md`，内容 / Create `.workbuddy/SOUL.md` with:

```markdown
请先读取项目根目录下的 AGENTS.md，这是本项目的核心行为准则。
Read AGENTS.md at the project root — it's the core behavior standard.
```

详细说明见 / See: [integrations/workbuddy/SOUL.md](integrations/workbuddy/SOUL.md)

### CodeBuddy

创建 `.codebuddy/rules/collaboration.md`，内容 / Create `.codebuddy/rules/collaboration.md` with:

```markdown
本项目所有 AI 协作规则以项目根目录下的 AGENTS.md 为准。
All AI collaboration rules are defined in AGENTS.md at the project root.
```

详细说明见 / See: [integrations/codebuddy/collaboration.md](integrations/codebuddy/collaboration.md)

### Cursor

创建 `.cursorrules` 文件，内容 / Create `.cursorrules` with:

```markdown
请先读取项目根目录下的 AGENTS.md，这是本项目的核心行为准则。
Read AGENTS.md at the project root — it's the core behavior standard.
All operations must comply with AGENTS.md.
```

详细说明见 / See: [integrations/cursor/README.md](integrations/cursor/README.md)

### GitHub Copilot

创建 `.github/copilot-instructions.md`，内容 / Create `.github/copilot-instructions.md` with:

```markdown
请先读取项目根目录下的 AGENTS.md，这是本项目的核心行为准则。
Read AGENTS.md at the project root — it's the core behavior standard.
```

详细说明见 / See: [integrations/copilot/README.md](integrations/copilot/README.md)

### 其他 AI 工具 | Other AI Tools

**中文**：任何能读取项目文件的 AI 工具，只要能读到项目根目录的 `AGENTS.md` 并遵守其中的指令，就能自动接入。

**English**: Any AI tool that can read project files and follow instructions in `AGENTS.md` at the project root will auto-join.

---

## 🧪 验证是否生效 | Verify It Works

### 中文

接入完成后，你可以问 AI 以下问题来验证：

```
你知道在这个项目里，哪些文件不能用写入工具直接覆盖吗？
```

如果 AI 能正确回答（"已有文件只能用编辑工具修改，不能用写入工具覆盖"），说明规则已生效。

### English

After setup, ask the AI this question to verify:

```
Do you know which files in this project cannot be directly overwritten with write tools?
```

If the AI correctly answers ("Existing files can only be modified with edit tools, not overwritten with write tools"), the rules are working.

---

## 🎯 常见问题 | FAQ

### Q: 只有 AGENTS.md 够吗？ | Is AGENTS.md alone enough?

**中文**：够。`AGENTS.md` 是核心，只要 AI 能读到它，规则就生效。其他文件都是增强体验的。

**English**: Yes. `AGENTS.md` is the core — as long as the AI can read it, the rules take effect. Other files are enhancements.

### Q: AI 不读取 AGENTS.md 怎么办？ | What if the AI doesn't read AGENTS.md?

**中文**：不同的 AI 工具有不同的规则文件格式。查看 [integrations/](integrations/) 目录，找到你用的工具对应的接入方式。

**English**: Different AI tools have different rule file formats. Check the [integrations/](integrations/) directory for your tool's integration method.

### Q: 可以自定义规则吗？ | Can I customize the rules?

**中文**：当然可以！直接修改 `AGENTS.md`，所有 AI 工具都会自动遵循新规则。记得更新版本号。

**English**: Absolutely! Just modify `AGENTS.md` and all AI tools will follow the new rules. Remember to update the version number.

### Q: 项目移动了位置怎么办？ | What if I move the project?

**中文**：不用担心。规则系统有路径变化检测机制，项目被移动后会自动重置敏感授权，确保安全。

**English**: Don't worry. The rule system has path-change detection — sensitive authorizations auto-reset when the project is moved.

### Q: 规则太多会影响 AI 效率吗？ | Will too many rules affect AI efficiency?

**中文**：规则系统有内置的精简机制。当规则超过 500 行时，会提示你精简合并。你也可以随时手动精简。

**English**: The system has a built-in simplification mechanism. When rules exceed 500 lines, it prompts you to consolidate. You can also manually simplify at any time.

---

## 📚 下一步 | Next Steps

| 中文 | English |
|------|---------|
| 想了解完整规则？读 [AGENTS.md](AGENTS.md) | Want the full rules? Read [AGENTS.md](AGENTS.md) |
| 想配置用户画像？复制 [USER_PROFILE_TEMPLATE.md](USER_PROFILE_TEMPLATE.md) | Want to configure your profile? Copy [USER_PROFILE_TEMPLATE.md](USER_PROFILE_TEMPLATE.md) |
| 想贡献规则？读 [README.md](README.md) 中的贡献指南 | Want to contribute? Read the Contributing section in [README.md](README.md) |

---

**版本 / Version**：v1.0
**最后更新 / Last Updated**：2024-01-01
