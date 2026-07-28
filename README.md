<p align="center">
  <img src="logo.png" width="120" alt="Plain Words Logo">
</p>

<h1 align="center">大白话 · Plain Words</h1>

<p align="center">
  <b>让 AI 说人话的 Agent Skill（智能体技能）</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="MIT">
  <img src="https://img.shields.io/badge/Platform-TRAE%20%7C%20Claude%20Code%20%7C%20Codex%20%7C%20WorkBuddy-blue" alt="Platforms">
  <img src="https://img.shields.io/github/stars/Demon-Ryan/plain-words?style=social" alt="Stars">
</p>

---

## 这是什么？

这是一个 **Agent Skill（智能体技能）**。

把它放进你的项目，AI 就会自动把所有技术术语翻译成大白话。不管你完全不懂代码，还是看技术文档头大，只要说"说人话"，AI 就会用零基础也能看懂的话来回答你。

### 核心功能

- **完全不懂代码也能听懂** — 所有术语第一次出现时都带大白话解释
- **中英双语标注** — 格式：`中文术语（English Term，就是XXX）`
- **60+ 术语全覆盖** — 从 API、服务器、数据库，到沙盒、Token、Cookie
- **概念关系讲明白** — 服务器和 CDN 有什么区别？前端和后端怎么配合？直接告诉你
- **弹窗/权限不再慌** — "允许""阻止""加白名单"这些按钮，每个都告诉你点了会发生什么
- **命令行带注释** — 每条命令后面用括号说明这条命令是干嘛的
- **风险提前说** — 涉及删除、安装、修改配置的操作，先说清楚会不会有风险
- **两层设计，省上下文** — 基础规则始终生效（很少的 token），深度解释只在你"不懂"时才加载

> ## What is this?
>
> This is an **Agent Skill**.
>
> Put it in your project, and the AI will automatically translate all technical jargon into plain language. Whether you know nothing about coding or just get overwhelmed by tech docs, simply say "explain it to me like I'm five" and the AI will answer in terms anyone can understand.
>
> ### Key Features
>
> - **Understand everything even if you know zero coding** — Every technical term gets a plain-language explanation on first use
> - **Bilingual labels** — Format: `中文术语（English Term，就是XXX）`
> - **60+ terms covered** — From API, server, database to sandbox, Token, Cookie
> - **Concept relationships explained** — What's the difference between a server and a CDN? How do frontend and backend work together? All spelled out
> - **No more panic over pop-ups** — "Allow", "Block", "Whitelist" — every button explained in plain words
> - **Command annotations** — Every command followed by a bracket explaining what it does
> - **Risks disclosed upfront** — Before delete, install, or config changes, you'll know the risks
> - **Two-tier design, saves context** — Basic rules always on (minimal tokens), deep explanations only when you say "I don't get it"

---

## 效果对比

**没装这个 Skill 时，AI 是这样回答的：**

> 你需要在终端里执行 `npm install`，安装依赖后运行 `npm run dev` 启动开发服务器。确保你的环境变量配置正确，端口没有被占用。

**装了这个 Skill 后，AI 是这样回答的：**

> 1. 打开终端（Terminal，就是电脑上可以输入命令的文字窗口。Windows 按 Win+R 输入 `cmd` 回车；Mac 在启动台搜"终端"）
> 2. 输入 `npm install`（下载安装项目需要的依赖包），按回车
> 3. 等它下载完，你会看到命令行不再滚动，出现输入提示符
> 4. 输入 `npm run dev`（启动开发模式，改完代码页面会自动更新），按回车
> 5. 看到 `Local: http://localhost:3000` 这行字，说明成功了，打开浏览器访问这个地址

> ## Before & After
>
> **Without this Skill:**
>
> > Run `npm install` in the terminal, then start the dev server with `npm run dev`. Make sure your environment variables are configured correctly and the port is not in use.
>
> **With this Skill:**
>
> > 1. Open Terminal (the text window where you type commands. Windows: press Win+R, type `cmd`, press Enter; Mac: search "Terminal" in Launchpad)
> > 2. Type `npm install` (downloads and installs the dependency packages your project needs), press Enter
> > 3. Wait for it to finish — you'll see the command line stop scrolling and show a new input prompt
> > 4. Type `npm run dev` (starts development mode; the page auto-refreshes when you edit code), press Enter
> > 5. When you see `Local: http://localhost:3000`, it's working! Open this address in your browser

---

## 支持哪些 Agent 平台？

本 Skill 基于标准的 **Agent Skill 规范**，可以在以下任何支持 Skill 机制的 AI 工具中使用：

| 平台 | 说明 |
|------|------|
| **TRAE** | 原生支持，可通过插件市场上传或手动放入 `.trae/skills/` 目录 |
| **Claude Code** | 支持 `.agents/skills/` 目录 |
| **Codex (by OpenAI)** | 支持 Skill 规范 |
| **WorkBuddy** | 支持 Skill 机制 |
| **其他兼容 Agent 规范的工具** | 只要支持读取 `SKILL.md` 的 Agent 都能用 |

**核心原理：** 这个 Skill 本质上就是一个 Markdown 文件（`SKILL.md`），里面写满了"遇到技术术语该怎么翻译"的规则。只要你的 AI 工具支持在对话前加载一段自定义指令，就能用这个 Skill。

> ## Which Agent Platforms Are Supported?
>
> This Skill follows the standard **Agent Skill specification** and works with any AI tool that supports the Skill mechanism:
>
> | Platform | Note |
> |----------|------|
> | **TRAE** | Native support, upload via plugin marketplace or place in `.trae/skills/` |
> | **Claude Code** | Supports `.agents/skills/` directory |
> | **Codex (by OpenAI)** | Supports Skill spec |
> | **WorkBuddy** | Supports Skill mechanism |
> | **Other Agent-compatible tools** | Any agent that can read `SKILL.md` |
>
> **Core principle:** This Skill is essentially a Markdown file (`SKILL.md`) filled with rules on "how to translate technical terms." As long as your AI tool supports loading custom instructions before a conversation, this Skill will work.

---

## 系统规则 + Skill 怎么配合用？

为了既照顾你的使用体验，又不浪费 AI 的上下文空间（AI 每次对话能记住的信息量是有限的），我们把"大白话"的能力拆成了两部分：

### 第一部分：系统规则（System Rules）— 每次对话都生效

这部分放在你的 **AI 工具系统设置** 里（不是放在项目文件夹里），内容很短，只有 8 条底线要求：

```
1. 【人话翻译】先用大白话解释清楚这是什么、用来干嘛的
2. 【步骤傻瓜化】一步一步来，说清楚点哪里、输入什么、看到什么算成功
3. 【命令大白话】给出的命令，用括号注释这条命令是干嘛的
4. 【风险说明】删除、安装等操作前，告诉用户会不会出问题
5. 【避坑提示】常见坑直接说出来
6. 【结果验收】每做完一步，告诉用户怎么验证成功了
7. 【术语表】遇到专业词汇，第一次出现时用括号解释
8. 【回复精简】少说没用的，除非用户要求解释
```

**这部分干嘛用的？** 它保证每次 AI 跟你说话时，都会自动遵守这些底线：术语要注释、命令要解释、步骤要傻瓜化。但因为内容很短，不占多少上下文。

### 第二部分：本 Skill — 你说"不懂"时才深度加载

这部分就是本仓库里的 `plain-language/SKILL.md` 文件，放在你的 **项目文件夹** 里。

**它干嘛用的？** 里面存了 60+ 个术语的完整翻译、几组概念的关系解释、弹窗按钮的大白话对照表。这些内容很长，但**只有你说"我不懂""说人话""这是什么意思"时，AI 才会加载它们**。平时不触发，几乎不占用上下文。

### 两部分的配合关系

| | 系统规则 | 本 Skill |
|--|---------|----------|
| **放在哪** | AI 工具的系统设置里 | 项目文件夹的 skills 目录里 |
| **什么时候生效** | 每次对话都生效 | 你说"不懂"时才触发 |
| **内容** | 8 条底线要求（很短） | 60+ 术语、概念关系、弹窗权限（很长） |
| **占用多少上下文** | 约 500 tokens | 约 1500~4000 tokens（按需加载） |

**总结：** 系统规则是"每次对话都提醒 AI 要照顾小白"，Skill 是"用户明确说不懂时，给 AI 一份完整的术语词典"。一个打基础，一个做增强，互不冲突。

> ## How Do System Rules and the Skill Work Together?
>
> To balance user experience and AI context efficiency (the amount of information AI can remember per conversation is limited), we've split the "plain language" capability into two parts:
>
> ### Part 1: System Rules — Always On
>
> This part goes in your **AI tool's system settings** (not in the project folder). It's short — just 8 baseline rules:
>
> ```
> 1. [Plain Language] Explain what things are and what they do in plain words
> 2. [Step-by-Step] One thing per step; say what to click, what to type, what success looks like
> 3. [Command Annotations] Every command gets a bracket explaining what it does
> 4. [Risk Warning] Before delete/install operations, tell the user if something could go wrong
> 5. [Gotchas] Call out common pitfalls directly
> 6. [Verification] After each step, tell the user how to confirm success
> 7. [Glossary] First occurrence of any technical term gets a bracket explanation
> 8. [Keep It Short] Less fluff, unless the user asks for explanation
> ```
>
> **What does this part do?** It ensures every AI response follows these baselines. Because it's short, it barely uses any context.
>
> ### Part 2: This Skill — Deep Mode When You Say "I Don't Get It"
>
> This is the `plain-language/SKILL.md` file in this repo, placed in your **project folder**.
>
> **What does it do?** It stores 60+ term translations, concept relationship explanations, and pop-up button plain-language guides. It's long, but **only loads when you say "I don't get it" or "explain like I'm five."** When not triggered, it uses almost zero context.
>
> ### How They Work Together
>
> | | System Rules | This Skill |
> |--|-------------|------------|
> | **Where** | AI tool's system settings | Project folder's skills directory |
> | **When** | Every conversation | Only when you say "I don't get it" |
> | **Content** | 8 short baseline rules | 60+ terms, relationships, permissions (long) |
> | **Context used** | ~500 tokens | ~1500–4000 tokens (on-demand) |
>
> **Summary:** System rules are "remind the AI every time to be beginner-friendly." The Skill is "when the user clearly says they're lost, give the AI a full term dictionary." One sets the foundation, the other provides the firepower. No conflict.

---

## 使用方法

有三种安装方式，从简单到复杂排列。**推荐第一种，最省事。**

### 方式一：通过 TRAE 插件市场上传（最简单，推荐）

这个方法完全不需要找任何文件夹，直接在 TRAE 里上传就行。

1. 在本仓库下载 `plain-words-for-trae.zip` 文件
   - 这个压缩包打开后，直接就能看到 `SKILL.md`，符合 TRAE 的上传要求
2. 打开 TRAE → 找到"插件市场"（以前叫"技能"）
3. 找到"上传技能"按钮
4. 选择刚才下载的 `plain-words-for-trae.zip` 文件
5. TRAE 会自动识别里面的 `SKILL.md`，帮你填好技能名称和描述
6. 点"确认"，技能就安装好了

**为什么推荐这个方式？** 因为你不需要去找任何文件夹，也不需要手动创建目录。TRAE 会自动帮你处理。上传后，这个技能在所有项目里都能用。

### 方式二：手动放到项目文件夹（适合想自己管理的人）

如果你不想用插件市场，也可以手动放置文件。但请注意一个关键问题——

**⚠️ "你的项目"是什么意思？**

"你的项目"指的是 **你在 TRAE 里创建或打开的那个项目文件夹**（就是你写代码的那个文件夹），**不是** TRAE 软件的安装目录。TRAE 装在电脑哪里，跟这个完全没关系。

**操作步骤：**

1. 在 TRAE 里打开你要用的项目
2. 在 TRAE 左侧的文件浏览器里，找到你项目的根目录（最外层的那个文件夹）
3. 看看里面有没有一个叫 `.trae` 的文件夹
   - **如果有**：跳到第 5 步
   - **如果没有**：继续看第 4 步
4. **没有 `.trae` 文件夹是正常的！** 大部分新项目都没有。你自己手动创建就行：
   - 在项目根目录上右键 → 新建文件夹 → 命名为 `.trae`（注意前面有个英文句号 `.`）
   - 在 `.trae` 里面再新建一个文件夹，命名为 `skills`
5. 把本仓库的 `plain-language/` 文件夹整个复制到 `skills/` 里面

最终结构长这样：

```
你在 TRAE 里打开的项目/        ← 这就是"你的项目"
└── .trae/                    ← 手动创建的隐藏文件夹
    └── skills/               ← 在 .trae 里面创建
        └── plain-language/   ← 从仓库复制过来的
            ├── SKILL.md
            └── references/
                ├── terms.md
                ├── concepts.md
                └── permissions.md
```

**常见问题：**

- **找不到 `.trae` 文件夹？** → 正常现象，大部分新项目都没有。自己新建一个就行（看第 4 步）
- **文件管理器看不到 `.trae`？** → 因为名字前面有 `.`，它是隐藏文件夹。Mac 按 `Cmd+Shift+.` 显示隐藏文件；Windows 在"查看"菜单里勾选"显示隐藏的文件"
- **这个文件夹跟 TRAE 软件安装目录有关系吗？** → **没有关系。** 这是每个项目自己的文件夹，跟 TRAE 软件装在哪完全无关
- **一定要放在项目文件夹吗？** → 是的。每个项目需要各自放一份。如果你有多个项目，每个项目都要放

### 方式三：其他 Agent 平台（Claude Code、Codex、WorkBuddy 等）

其他平台的原理和 TRAE 一样——把 Skill 文件放到指定目录里。但和 TRAE 一样，你可能会遇到"找不到目录"的问题。

| 平台 | 放在哪里 | 找不到目录怎么办 |
|------|---------|----------------|
| **Claude Code** | `你的项目/.agents/skills/plain-language/` | 自己手动创建 `.agents/skills/` 文件夹 |
| **Codex** | 查看其文档中"custom skills"的设置位置 | 如果不支持目录方式，把 `SKILL.md` 内容粘贴到自定义指令里 |
| **WorkBuddy** | 查看其文档中"skills"的设置位置 | 同上 |
| **其他工具** | 找到"自定义 Skill""系统提示词""Custom Instructions"的设置入口 | 把 `SKILL.md` 的内容粘贴进去 |

**所有平台的通用兜底方法：** 如果以上方法都不行，打开 `SKILL.md` 文件，把里面的内容全部复制，粘贴到你 AI 工具的"自定义指令"（Custom Instructions）或"系统提示词"（System Prompt）设置里，效果是一样的。

### 安装好之后怎么用

在 AI 对话里直接说下面任何一句话就行：

- "用大白话解释一下什么是 API"
- "说人话"
- "太专业了，我看不懂"
- "这是什么意思"
- "能不能通俗点"
- "能不能再简单点"

AI 就会自动加载这个 Skill，用大白话回答你。也可以手动输入 `/plain-language` 触发。

> ## Installation
>
> Three methods, from easiest to most manual. **Method 1 is recommended.**
>
> ### Method 1: Upload via TRAE Plugin Marketplace (Easiest, Recommended)
>
> This method requires no folder hunting — just upload directly in TRAE.
>
> 1. Download `plain-words-for-trae.zip` from this repo
>    - The zip has `SKILL.md` at the root level, meeting TRAE's upload requirement
> 2. Open TRAE → find "Plugin Marketplace" (formerly "Skills")
> 3. Find the "Upload Skill" button
> 4. Select the downloaded `plain-words-for-trae.zip`
> 5. TRAE will auto-detect `SKILL.md` and fill in the skill name and description
> 6. Click "Confirm" — done!
>
> > **Why recommend this?** No need to find or create any folders. TRAE handles everything. The skill works across all your projects after upload.
>
> ### Method 2: Manual Placement (For Those Who Want to Manage Files Themselves)
>
> **⚠️ What does "your project" mean?**
>
> "Your project" refers to **the project folder you created or opened in TRAE** — the folder where you write code. It is **NOT** the TRAE software installation directory.
>
> **Steps:**
>
> 1. Open your project in TRAE
> 2. In TRAE's file browser, find the project root folder (the outermost folder)
> 3. Check if there's a folder called `.trae`
>    - **If yes**: skip to step 5
>    - **If no**: continue to step 4
> 4. **Not having `.trae` is normal!** Most new projects don't have it. Just create it manually:
>    - Right-click the project root → New Folder → name it `.trae` (note the leading `.`)
>    - Inside `.trae`, create another folder named `skills`
> 5. Copy the entire `plain-language/` folder from this repo into `skills/`
>
> **Common issues:**
>
> - **Can't find `.trae`?** → Normal. Create it yourself (see step 4)
> - **File manager doesn't show `.trae`?** → It's a hidden folder (starts with `.`). Mac: press `Cmd+Shift+.`; Windows: enable "Show hidden files" in View menu
> - **Is this related to the TRAE installation folder?** → **No.** This is a per-project folder, completely unrelated to where TRAE is installed
> - **Does it have to be in the project folder?** → Yes. Each project needs its own copy. If you have multiple projects, each one needs it
>
> ### Method 3: Other Agent Platforms (Claude Code, Codex, WorkBuddy, etc.)
>
> Other platforms work the same way as TRAE — place Skill files in the designated directory. But like TRAE, you may encounter "can't find directory" issues.
>
> | Platform | Location | Can't find directory? |
> |----------|----------|----------------------|
> | **Claude Code** | `your-project/.agents/skills/plain-language/` | Create `.agents/skills/` manually |
> | **Codex** | Check docs for "custom skills" | Paste `SKILL.md` content into custom instructions |
> | **WorkBuddy** | Check docs for "skills" | Same as above |
> | **Other tools** | Find "Custom Instructions" or "System Prompt" setting | Paste `SKILL.md` content |
>
> **Universal fallback (all platforms):** If none of the above works, open `SKILL.md`, copy everything, and paste it into your AI tool's "Custom Instructions" or "System Prompt" setting. Same effect.
>
> ### How to Use After Installation
>
> Simply say any of the following in your AI chat:
>
> - "Explain what an API is in plain language"
> - "Say it in human words"
> - "Too technical, I don't understand"
> - "What does this mean?"
> - "Can you make it simpler?"
>
> The AI will automatically load this Skill and answer in plain language. You can also trigger it manually by typing `/plain-language`.

---

## 覆盖的术语

### 基础概念
API、SDK、框架（Framework）、库/插件（Library/Plugin）、组件（Component）、前端（Frontend）、后端（Backend）、全栈（Full Stack）、全栈开发流程

### 硬件与基础设施
服务器（Server）、云服务器（Cloud Server）、阿里云/腾讯云/AWS、CDN（内容分发网络）、七牛云/又拍云、虚拟机（Virtual Machine）、容器/Docker（Container）

### 网络相关
域名（Domain）、IP地址、DNS（域名系统）、网关（Gateway）、防火墙（Firewall）、代理（Proxy）、HTTPS、SSL证书、端口（Port）、带宽（Bandwidth）、延迟/响应时间（Latency）

### 开发与工具
终端/命令行/命令提示符（Terminal）、IDE / 编辑器、VS Code、环境（Environment）、开发环境（Dev Environment）、生产环境（Production Environment）、沙盒（Sandbox）、工作目录/项目目录（Working Directory）、根目录（Root Directory）、相对路径（Relative Path）、绝对路径（Absolute Path）、包管理器（Package Manager）、Git、GitHub/GitLab/Gitee、CI/CD（持续集成/持续部署）、Docker、日志（Log）、路由（Route）、中间件（Middleware）、Token、密钥/Secret Key、Cookie、Session

### 数据与存储
数据库（Database）、SQL（结构化查询语言）、JSON、接口（Interface/Endpoint）、部署（Deploy）、构建（Build）、编译（Compile）、依赖（Dependency）、node_modules、环境变量（Environment Variable）、缓存（Cache）、回调（Callback）、异步（Async）、同步（Sync）、开源（Open Source）、云函数/Serverless、Bug、Feature、回滚（Rollback）、灰度发布（Canary Release）、A/B测试

### 弹窗与权限
确认/允许/阻止/取消/忽略/始终允许/仅此次允许/加白名单/移出白名单，以及 8 种常见权限的风险说明

> 觉得缺了什么术语？欢迎提 Issue 或发 PR！

> ## Terms Covered
>
> ### Basic Concepts
> API, SDK, Framework, Library/Plugin, Component, Frontend, Backend, Full Stack, Full-Stack Development Flow
>
> ### Hardware & Infrastructure
> Server, Cloud Server, Alibaba Cloud/Tencent Cloud/AWS, CDN, Qiniu Cloud/UpYun, Virtual Machine, Container/Docker
>
> ### Networking
> Domain, IP Address, DNS, Gateway, Firewall, Proxy, HTTPS, SSL Certificate, Port, Bandwidth, Latency
>
> ### Development & Tools
> Terminal, IDE, VS Code, Environment, Dev Environment, Production Environment, Sandbox, Working Directory, Root Directory, Relative Path, Absolute Path, Package Manager, Git, GitHub/GitLab/Gitee, CI/CD, Docker, Log, Route, Middleware, Token, Secret Key, Cookie, Session
>
> ### Data & Storage
> Database, SQL, JSON, Interface/Endpoint, Deploy, Build, Compile, Dependency, node_modules, Environment Variable, Cache, Callback, Async, Sync, Open Source, Serverless, Bug, Feature, Rollback, Canary Release, A/B Testing
>
> ### Pop-ups & Permissions
> Confirm/Allow/Block/Cancel/Ignore/Always Allow/Allow Once/Add to Whitelist/Remove from Whitelist, plus 8 common permission types with risk descriptions
>
> Think we're missing a term? Open an Issue or send a PR!

---

## 两层设计

| | 始终生效 | 深度模式 |
|--|---------|----------|
| **触发条件** | 每次对话都生效 | 你说"不懂"时才触发 |
| **做什么** | 术语括号简短标注、命令注释、风险提示、验证方法 | 加载完整术语表、概念关联、弹窗权限解释 |
| **占多少 token** | 很少（约 1500 tokens） | 额外加载约 2300 tokens |

这样平时不触发深度模式时，几乎不额外占用上下文。

> ## Two-Tier Design
>
> | | Always On | Deep Mode |
> |--|-----------|----------|
> | **Trigger** | Every conversation | When you say "I don't get it" |
> | **What it does** | Short term annotations, command notes, risk warnings | Full glossary, concept maps, permission guides |
> | **Token usage** | Minimal (~1500 tokens) | Extra ~2300 tokens |
>
> This way, when deep mode isn't triggered, almost no extra context is used.

---

## 贡献

这个 Skill 的术语库越全越好用，欢迎大家一起完善！

1. Fork 这个仓库
2. 修改 `plain-language/references/terms.md`（加术语）或 `SKILL.md`（改规则）
3. 提交 Pull Request

### 贡献规范

- 新增术语时，解释优先说"它是干嘛的"和"怎么用"，不要用生活比喻
- 术语第一次出现格式：`中文（English，就是XXX）`
- 保持精简，用户问什么翻译什么，不要过度解释

> ## Contributing
>
> The more complete the term glossary, the better this Skill works. Contributions welcome!
>
> 1. Fork this repo
> 2. Edit `plain-language/references/terms.md` (add terms) or `SKILL.md` (change rules)
> 3. Submit a Pull Request
>
> ### Guidelines
> - When adding a term, explain "what it does" and "how it's used" first. Avoid life metaphors.
> - First appearance format: `中文（English，就是XXX）`
> - Stay concise. Translate what the user asked for, nothing extra.

---

## License

MIT License — 随便用、随便改、随便分享。

> ## License
> MIT License — Use freely, modify freely, share freely.

---

<p align="center">
  <img src="logo.png" width="48" alt="Logo">
  <br>
  如果觉得有用，点一下 ⭐ Star 让更多人发现它！
</p>