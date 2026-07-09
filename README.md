# 面试辅导与陪跑教练

> v1.1 | 作者：观星哥
>
> AI 驱动的财务面试辅导 Skill。上传你的简历和目标岗位 JD，它会像一位面过几百人的财务老兵那样，先摸透这家公司到底做什么生意、这个岗位真正要解决什么问题，再逐项对照你的背景做匹配分析，告诉你面试官可能会在哪些点追着你问、在哪些点你能打出优势。最终输出一份包含话术策略、问答准备和面试前 Checklist 的完整报告。

## 兼容平台

本 Skill 同时兼容以下 AI 编码助手的 Skill 系统：

| 平台 | 全局安装路径 | 项目级安装路径 |
|---|---|---|
| **OpenCode** | `~/.config/opencode/skills/financial-interview-coach/` | `.opencode/skills/financial-interview-coach/` |
| **Claude Code** | `~/.claude/skills/financial-interview-coach/` | `.claude/skills/financial-interview-coach/` |
| **通用 Agent** | `~/.agents/skills/financial-interview-coach/` | `.agents/skills/financial-interview-coach/` |

> **注意**：目录名 `financial-interview-coach` 必须与 SKILL.md 中 `name` 字段一致，否则无法被发现。

## 前置条件

- 已安装 OpenCode / Claude Code / 其他兼容 Agent
- （可选）系统安装 `pdftotext` 工具，用于解析 PDF 格式的用户材料。macOS 可通过 Homebrew 安装：`brew install poppler`

## 安装

### 方式一：AI 自动安装（最快）

在 OpenCode、Claude Code 或 Codex 中直接说：

```
请帮我自动适配并安装如下 skill：
https://github.com/YFzh1995/Interview-Coach
```

AI 会自动识别当前平台和 Agent 类型，将 SKILL.md 安装到正确路径。

### 方式二：Git 克隆（可获得更新）

```bash
# macOS / Linux / Windows WSL：全局安装
mkdir -p ~/.config/opencode/skills
git clone https://github.com/YFzh1995/Interview-Coach.git ~/.config/opencode/skills/financial-interview-coach

# Claude Code 用户：改为 ~/.claude/skills/financial-interview-coach
```

Windows（非 WSL）对应的全局路径为 `%USERPROFILE%\.config\opencode\skills\`，在 PowerShell 或命令提示符中执行：

```powershell
mkdir %USERPROFILE%\.config\opencode\skills
git clone https://github.com/YFzh1995/Interview-Coach.git %USERPROFILE%\.config\opencode\skills\financial-interview-coach
```

### 方式三：手动下载

1. 从 [Releases](https://github.com/YFzh1995/Interview-Coach/releases) 下载 `SKILL.md`
2. 在目标路径创建目录（见上方兼容平台表格）
3. 将 `SKILL.md` 放入该目录

### 方式四：项目级安装

在项目根目录执行：

```bash
mkdir -p .opencode/skills/financial-interview-coach
# 然后将 SKILL.md 下载或复制到该目录
```

> 项目级安装适用于团队共享场景——将 `.opencode/skills/` 加入 Git 仓库，团队成员 clone 即用。

## 使用

在 OpenCode / Claude Code 中，向 AI 发送面试准备请求即可自动触发。例如：

```
帮我准备财务面试。目标公司：xxx，岗位：xxx，JD：xxx
[附上简历文件或文本]
```

Skill 加载后将按 Step 0 → Step 6 逐步引导分析，最终输出完整的面试准备报告。全程交互式，每步确认后再继续。

### 触发词

以下任一表达均可触发此 Skill：

- `@财务面试` / `@面试准备`
- `帮我准备财务面试`
- `面试辅导` / `陪跑教练`

## 更新

```bash
cd ~/.config/opencode/skills/financial-interview-coach
git pull origin main
```

## 反馈

在使用结束后，对 AI 说一句"**汇总本次分析**"或"**生成会话日志**"，AI 会将整场讨论整理为结构化日志文件。把日志文件发到微信 **guangxingge2025**（观星哥本人），星哥会根据反馈持续迭代这个 Skill。

## 许可

MIT
