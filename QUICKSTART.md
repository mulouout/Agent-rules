# 快速上手指南

> 1 分钟让所有 AI 工具都遵守你的规则。

---

## ⏱️ 1 分钟快速接入

### 第 1 步：复制核心文件（10 秒）

将以下文件复制到你的项目根目录：

```
你的项目/
├── AGENTS.md                    ← 复制这个
├── USER_PROFILE_TEMPLATE.md     ← 复制这个
└── README.md                    ← 可选（如果你的项目已有 README）
```

只需要 `AGENTS.md` 就能工作，其他文件是辅助的。

### 第 2 步：用 AI 工具打开项目（5 秒）

用你常用的 AI 编程工具打开项目目录：
- TRAE → 打开工作区
- Cursor → 打开文件夹
- Copilot → 打开仓库
- 其他 → 打开项目目录

### 第 3 步：完成引导配置（~45 秒）

AI 会自动检测到这是首次使用，引导你填写：
1. 怎么称呼你？
2. 常用技术栈？
3. 偏好的沟通风格？
4. 特殊习惯或规则？

回答几个问题就完成了。

---

## 📋 接入清单

### ✅ 必须文件

| 文件 | 必须 | 作用 |
|------|------|------|
| `AGENTS.md` | ✅ 是 | 核心规则，AI 读到就自动接入 |

### ⚙️ 推荐文件

| 文件 | 必须 | 作用 |
|------|------|------|
| `USER_PROFILE_TEMPLATE.md` | ⭐ 推荐 | 填写你的偏好后改名为 `USER_PROFILE.md` |
| `README.md` | ⭐ 推荐 | 项目说明，AI 会读取了解项目背景 |

### 🔧 可选文件（进阶）

| 文件 | 必须 | 作用 |
|------|------|------|
| `.ai-rules/` | 🔧 可选 | AI 运行时配置目录 |
| `integrations/` | 🔧 可选 | 各工具的接入示例 |

---

## 🔌 各工具接入方式

### TRAE

将以下内容添加到项目的 `.trae/rules/` 目录下的规则文件中：

```markdown
本项目所有规则以项目根目录下的 AGENTS.md 为准。
请先读取 AGENTS.md，再读取 USER_PROFILE.md（如果存在）。
```

详细说明见 [integrations/trae/README.md](integrations/trae/README.md)。

### WorkBuddy

创建 `.workbuddy/SOUL.md`，内容：

```markdown
请先读取项目根目录下的 AGENTS.md，这是本项目的核心行为准则。
再读取 USER_PROFILE.md（如果存在）了解用户偏好。
```

详细说明见 [integrations/workbuddy/SOUL.md](integrations/workbuddy/SOUL.md)。

### CodeBuddy

创建 `.codebuddy/rules/collaboration.md`，内容：

```markdown
本项目所有 AI 协作规则以项目根目录下的 AGENTS.md 为准。
请先读取 AGENTS.md 完整内容，再开始工作。
```

详细说明见 [integrations/codebuddy/collaboration.md](integrations/codebuddy/collaboration.md)。

### Cursor

创建 `.cursorrules` 文件，内容：

```markdown
请先读取项目根目录下的 AGENTS.md，这是本项目的核心行为准则。
再读取 USER_PROFILE.md（如果存在）了解用户偏好。
所有操作必须遵守 AGENTS.md 中的规定。
```

详细说明见 [integrations/cursor/README.md](integrations/cursor/README.md)。

### GitHub Copilot

创建 `.github/copilot-instructions.md`，内容：

```markdown
请先读取项目根目录下的 AGENTS.md，这是本项目的核心行为准则。
所有操作必须遵守 AGENTS.md 中的规定。
```

详细说明见 [integrations/copilot/README.md](integrations/copilot/README.md)。

### 其他 AI 工具

任何能读取项目文件的 AI 工具，只要：
1. 能读到项目根目录的 `AGENTS.md`
2. 能遵守文件中的指令

就能自动接入本规则系统。

---

## 🧪 验证是否生效

接入完成后，你可以问 AI 以下问题来验证：

```
你知道在这个项目里，哪些文件不能用写入工具直接覆盖吗？
```

如果 AI 能正确回答（"已有文件只能用编辑工具修改，不能用写入工具覆盖"），说明规则已生效。

---

## 🎯 常见问题

### Q: 只有 AGENTS.md 够吗？

够。`AGENTS.md` 是核心，只要 AI 能读到它，规则就生效。其他文件都是增强体验的。

### Q: AI 不读取 AGENTS.md 怎么办？

不同的 AI 工具有不同的规则文件格式。查看 [integrations/](integrations/) 目录，找到你用的工具对应的接入方式。

### Q: 可以自定义规则吗？

当然可以！直接修改 `AGENTS.md`，所有 AI 工具都会自动遵循新规则。记得更新版本号。

### Q: 项目移动了位置怎么办？

不用担心。规则系统有路径变化检测机制，项目被移动后会自动重置敏感授权，确保安全。

### Q: 规则太多会影响 AI 效率吗？

规则系统有内置的精简机制。当规则超过 500 行时，会提示你精简合并。你也可以随时手动精简。

---

## 📚 下一步

- 想了解完整规则？读 [AGENTS.md](AGENTS.md)
- 想配置用户画像？复制 [USER_PROFILE_TEMPLATE.md](USER_PROFILE_TEMPLATE.md) 为 `USER_PROFILE.md` 并填写
- 想贡献规则？读 [README.md](README.md) 中的贡献指南

---

**版本**：v1.0
**最后更新**：2024-01-01
