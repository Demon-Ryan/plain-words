<p align="center">
  <img src="./logo.png" width="100" alt="Plain Words">
</p>

<p align="center"><b>大白话 · Plain Words</b></p>

<p align="center">让 AI 说人话的 Agent Skill</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="MIT">
  <img src="https://img.shields.io/badge/Platform-TRAE%20%7C%20Claude%20Code%20%7C%20Codex%20%7C%20WorkBuddy-blue" alt="Platforms">
  <img src="https://img.shields.io/github/stars/Demon-Ryan/plain-words?style=social" alt="Stars">
</p>

<p align="center"><sub>An Agent Skill that translates AI's technical answers into plain language.</sub></p>

---

## 这是什么？

把它放进你的项目，AI 就会自动把所有技术术语翻译成大白话。只要说"说人话"，AI 就会用零基础也能看懂的话来回答你。

> ## What is this?
>
> Put it in your project, and the AI will automatically translate all technical jargon into plain language. Say "explain like I'm five" and the AI answers in terms anyone can understand.

---

## 效果对比

**没装时：**

> 在终端执行 `npm install`，然后运行 `npm run dev` 启动开发服务器。确保环境变量配置正确。

**装了后：**

> 1. 打开终端（Terminal，就是电脑上输入命令的文字窗口）
> 2. 输入 `npm install`（下载项目需要的依赖包），按回车
> 3. 等命令行不再滚动，说明下载完了
> 4. 输入 `npm run dev`（启动开发模式），按回车
> 5. 看到 `Local: http://localhost:3000`，说明成功了

> ## Before & After
>
> **Without:** Run `npm install` in the terminal, then start the dev server with `npm run dev`.
>
> **With:** 1. Open Terminal (the text window for commands) 2. Type `npm install` (downloads dependencies), press Enter 3. Wait until scrolling stops 4. Type `npm run dev` (starts dev mode), press Enter 5. See `Local: http://localhost:3000` — it's working!

---

## 安装

### 方式一：TRAE 插件市场（推荐，最简单）

1. 下载本仓库的 `plain-words-for-trae.zip`
2. 打开 TRAE → 插件市场 → 上传技能
3. 选择下载的 zip 文件，点确认即可

### 方式二：手动放置

把 `plain-language/` 文件夹复制到你项目的 `.trae/skills/` 目录里。没有 `.trae` 文件夹就自己建一个（注意前面有个 `.`）。

### 方式三：其他平台（Claude Code、Codex 等）

把 `plain-language/` 放到对应平台的 skills 目录。找不到目录？打开 `SKILL.md`，把内容复制粘贴到自定义指令（Custom Instructions）里，效果一样。

> ## Installation
>
> **Method 1 (Recommended):** Download `plain-words-for-trae.zip` → TRAE → Plugin Marketplace → Upload Skill → Select zip → Confirm.
>
> **Method 2:** Copy `plain-language/` folder into your project's `.trae/skills/` directory. Create `.trae/` if it doesn't exist (note the leading dot).
>
> **Method 3 (Other platforms):** Place `plain-language/` in the platform's skills directory. Or copy `SKILL.md` content into Custom Instructions — same effect.

---

## 用法

安装后在对话里说任意一句即可触发：

`"说人话"` · `"看不懂"` · `"太专业了"` · `"简单说一下"` · `"这是什么意思"`

> ## Usage
>
> After installation, say any of: `"explain like I'm five"` · `"too technical"` · `"what does this mean"` · `"simplify"`

---

## 两层设计

| | 始终生效 | 深度模式 |
|--|---------|---------|
| **触发** | 每次对话 | 你说"不懂"时 |
| **内容** | 术语括号标注、命令注释、风险提示 | 加载完整术语表（60+）、概念关联、弹窗权限解释 |
| **Token** | ~1500 | 额外 ~2300 |

基础规则每次都生效，深度模式按需加载，不浪费上下文。

> ## Two-Tier Design
>
> | | Always On | Deep Mode |
> |--|-----------|-----------|
> | **Trigger** | Every chat | When you say "I don't get it" |
> | **Content** | Term annotations, command notes | Full glossary (60+), concept maps, permission guides |
> | **Tokens** | ~1500 | +2300 |

---

## 覆盖的术语

**基础：** API、SDK、框架、前端/后端、全栈开发流程

**基础设施：** 服务器、云服务器、CDN、Docker、虚拟机

**网络：** 域名、IP、DNS、HTTPS、SSL、端口、带宽

**开发工具：** 终端、IDE、环境变量、沙盒、Git、CI/CD、Token、Cookie、Session

**数据存储：** 数据库、SQL、JSON、缓存、依赖、构建、部署、回滚、灰度发布

**弹窗权限：** 允许/阻止/取消/白名单 + 8 种常见权限的风险说明

> ## Terms Covered
>
> **Basics:** API, SDK, Framework, Frontend/Backend, Full-Stack Flow
>
> **Infra:** Server, Cloud Server, CDN, Docker, VM
>
> **Network:** Domain, IP, DNS, HTTPS, SSL, Port, Bandwidth
>
> **Dev Tools:** Terminal, IDE, Env Variables, Sandbox, Git, CI/CD, Token, Cookie
>
> **Data:** Database, SQL, JSON, Cache, Dependency, Build, Deploy, Rollback
>
> **Permissions:** Allow/Block/Cancel/Whitelist + 8 permission types with risk descriptions

---

## 系统规则配合

为了省上下文，"大白话"能力拆成两部分：

- **系统规则**（放在 AI 工具设置里）：8 条底线，每次对话生效，约 500 tokens
- **本 Skill**（放在项目里）：60+ 术语完整翻译，你说"不懂"时才加载

一个打底，一个增强，互不冲突。系统规则内容见仓库 [system-rules.md](./system-rules.md)。

> ## System Rules + Skill
>
> Split into two parts: **System Rules** (8 baseline rules in AI settings, ~500 tokens) always on; **This Skill** (full glossary) loads on-demand. One sets the foundation, one provides the firepower.

---

## 贡献

术语库越全越好用，欢迎完善！

1. Fork → 修改 `terms.md`（加术语）或 `SKILL.md`（改规则）→ 提 PR
2. 新术语优先说"它是干嘛的"和"怎么用"，不要用生活比喻
3. 格式：`中文（English，就是XXX）`

> ## Contributing
>
> 1. Fork → Edit `terms.md` or `SKILL.md` → Submit PR
> 2. Explain "what it does" and "how to use" first. Avoid metaphors.
> 3. Format: `中文（English，就是XXX）`

---

## License

MIT — 随便用、随便改、随便分享。

> MIT License — Use, modify, share freely.

---

<p align="center">
  <sub>觉得有用？点个 ⭐ Star 让更多人发现它</sub>
</p>