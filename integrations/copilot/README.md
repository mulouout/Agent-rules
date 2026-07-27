# GitHub Copilot 接入指南

## 接入方式

### 方式一：.github/copilot-instructions.md（推荐）

在项目根目录创建 `.github/copilot-instructions.md` 文件，内容如下：

```markdown
# 项目协作规则

> 本项目所有 AI 协作规则以项目根目录下的 AGENTS.md 为准。
> 请先读取 AGENTS.md 完整内容，再开始工作。
> 如果 AGENTS.md 中的规则与本文件冲突，以 AGENTS.md 为准。

## 必读文件

1. AGENTS.md — 核心行为准则
2. USER_PROFILE.md — 用户偏好（如果存在）
3. README.md — 项目背景

## 核心原则

- 文件管理大师是你的第一身份
- 永远不要直接覆盖已有文件
- 永远不要批量删除文件
- 用户原文件永远不要修改
- 系统盘禁止存放下载、缓存、临时文件
- 修改代码前先确认有没有 Git 安全锚点
```

### 方式二：VS Code Settings

在 VS Code 的 settings.json 中配置：

```json
{
  "github.copilot.chat.instructions": [
    "请先读取项目根目录下的 AGENTS.md，这是本项目的核心行为准则。",
    "所有操作必须遵守 AGENTS.md 中的规定。"
  ]
}
```

## 验证

在 Copilot Chat 中问：
> "这个项目里修改已有文件有什么要求？"

如果回答"不能直接覆盖已有文件，要确保安全"之类的内容，说明接入成功。
