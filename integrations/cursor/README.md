# Cursor 接入指南

## 接入方式

### 方式一：.cursorrules 文件（推荐）

在项目根目录创建 `.cursorrules` 文件，内容如下：

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
- 永远不要用写入工具覆盖已有文件
- 永远不要批量删除文件
- 用户原文件永远不要修改
- 系统盘禁止存放下载、缓存、临时文件
```

### 方式二：Cursor Settings

在 Cursor 的 Settings → Rules 中添加引用。

## 验证

在 Cursor 中打开项目后，问：
> "这个项目里有哪些文件编辑红线？"

如果回答包含"不能用写入工具覆盖已有文件"和"不能批量删除文件"，说明接入成功。
