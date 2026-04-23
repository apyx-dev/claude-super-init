<div align="center">

# ⚡ Super Init

**One command. Your entire project. Ready for multi-agent AI.**

why configure many file when one command do trick

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude_Code-plugin-blueviolet)](https://docs.anthropic.com/en/docs/claude-code)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/apyx-dev/claude-super-init/pulls)

</div>

---

## The Problem

You open a new project with Claude Code. You want multi-agent workflows. Now you need to:

- 🔍 Analyze your tech stack manually
- 📝 Write agent files from scratch
- ⚙️ Configure MCP servers
- 🧠 Install token-saving tools
- 📂 Set up `CLAUDE.md` with project context

**That's 30-60 minutes of setup. Every. Single. Project.**

## The Fix

```
/super-init:init
```

That's it. One command. Everything configured. Agents generated. Tools installed. Done.

---

## 🎬 Before & After

<table>
<tr>
<td width="50%" valign="top">

### ❌ Without Super Init
```
# manually write 5 agent files...
# manually configure .mcp.json...
# manually install code-review-graph...
# manually write CLAUDE.md...
# manually figure out your stack...

⏱️ 45-60 min setup per project
🪫 generic agents, not project-aware
📦 no token optimization
```

</td>
<td width="50%" valign="top">

### ✅ With Super Init
```
/super-init:init

⏱️  ~5 min
🔋 agents know YOUR stack, YOUR code
📦 up to 49x token savings (graph)
📦 up to 75% fewer output tokens (caveman)
🎭 team lead + specialists, ready to go
```

</td>
</tr>
</table>

---

## 🚀 Install

**Option 1 — One-liner (shell):**

```bash
claude plugin install super-init@claude-super-init
```

**Option 2 — Inside Claude Code:**

```
/plugin marketplace add apyx-dev/claude-super-init
/plugin install super-init@claude-super-init
```

**Option 3 — Via marketplace (shell):**

```bash
claude marketplace add github:apyx-dev/claude-super-init
claude plugin install super-init
```

Then run:

```
/super-init:init
```

---

## 🧠 What Happens When You Run It

Super Init runs **7 phases** automatically:

| Phase | What | Why |
|:-----:|------|-----|
| 1️⃣ | **Project Analysis** | Scans your entire codebase — languages, frameworks, patterns, conventions |
| 2️⃣ | **Code-Review-Graph** | Installs a code knowledge graph for **49x token savings** on context |
| 3️⃣ | **Caveman Plugin** | Enables compressed communication for **~75% output token savings** |
| 4️⃣ | **MCP Servers** | Configures Playwright (QA automation) + graph tools in `.mcp.json` |
| 5️⃣ | **CLAUDE.md** | Generates project rules & conventions (<800 tokens, loaded everywhere) |
| 6️⃣ | **Agent Generation** | Creates team lead + up to 4 specialist agents with real project data |
| 7️⃣ | **Summary** | Shows what was installed, skipped, and how to start |

> 💡 **Non-destructive** — merges with existing configs, never overwrites your settings.

---

## 🎭 Generated Agents

Your project gets a **team** — not generic templates, but agents built from your actual code:

| Agent | Trigger | Role | Model |
|:-----:|---------|------|:-----:|
| 🔵 `lead.md` | Always | Orchestrator — decomposes tasks, delegates, reviews | Opus |
| 🔴 `backend.md` | Backend framework detected | APIs, services, database logic | Sonnet |
| 🟣 `frontend.md` | Frontend framework detected | Components, pages, styling | Sonnet |
| 🟠 `mobile.md` | React Native / Flutter / native | Mobile app development | Sonnet |
| 🟢 `qa.md` | Test framework detected | E2E testing with Playwright | Sonnet |
| 🟡 `devops.md` | Docker / Terraform / K8s / CI | Infrastructure & deployment | Sonnet |
| 🔵 `ai.md` | ANY AI/ML framework | LLM integrations, pipelines | Sonnet |
| 🟤 `data.md` | dbt / Airflow / SQL-heavy | ETL, data warehousing | Sonnet |
| ⚪ `{name}.md` | Service doesn't fit standard roles | Custom agent from universal template | Sonnet |

### What makes these agents different?

Every generated agent contains **your project's actual**:

- ✅ Stack versions and dependencies
- ✅ Directory layout and architecture
- ✅ Coding patterns (discovered by reading your source files)
- ✅ Build, lint, and test commands
- ✅ File ownership boundaries (no agent steps on another's files)

---

## 📊 Token Savings Stack

Super Init doesn't just set up agents — it makes them **dramatically cheaper to run**:

| Tool | Savings | How |
|------|:-------:|-----|
| **code-review-graph** | **up to 49x** | Smart context extraction — agents read only what matters |
| **caveman** | **~75%** | Compressed output — same substance, fewer tokens |
| **CLAUDE.md** | — | <800 tokens, loaded once, prevents redundant context |
| **File ownership** | — | Agents only touch their files, no wasted exploration |

> Combined, a task that would burn **100K tokens** might use **~5-10K**. Real savings. Real money.

---

## 🔧 Options

Full control over what runs:

| Command | What Runs |
|---------|-----------|
| `/super-init:init` | Everything |
| `/super-init:init --no-graph` | Skip code-review-graph |
| `/super-init:init --no-caveman` | Skip caveman plugin |
| `/super-init:init --no-agents` | Skip agent generation |
| `/super-init:init --no-mcp` | Skip MCP server configuration |
| `/super-init:init --agents-only` | Only analyze + generate agents |
| `/super-init:init --graph-only` | Only install code-review-graph |
| `/super-init:init --caveman-only` | Only install caveman |
| `/super-init:init --mcp-only` | Only configure MCP servers |
| `/super-init:init --rebuild` | Overwrite existing agents + rebuild graph |

Combine freely: `/super-init:init --no-graph --no-caveman` runs agents only.

---

## 🔍 Tech Detection

Super Init recognizes **30+ languages**, **25+ frameworks**, and a wide range of tooling:

<details>
<summary><b>Full detection matrix</b> (click to expand)</summary>


**Languages:** TypeScript, JavaScript, Python, Go, Rust, Java, Kotlin, Swift, Ruby, PHP, C#, Dart, Vue, Svelte

**Frontend:** React, Vue, Angular, Svelte, Next.js, Nuxt, Astro, Gatsby, Remix, Solid

**Backend:** Express, Koa, Fastify, NestJS, Hono, Django, Flask, FastAPI, Laravel, Symfony, Gin, Chi, Fiber, Actix, Axum, Rocket, Ktor, Vapor

**Mobile:** React Native, Expo, Flutter, Capacitor, Ionic, native iOS/Android

**Infrastructure:** Docker, GitHub Actions, GitLab CI, Jenkins, Terraform, Kubernetes, Serverless, Vercel, Netlify, Fly.io

**Databases:** Prisma, Drizzle, Mongoose, TypeORM, Sequelize, SQLAlchemy

**Testing:** Jest, Vitest, Playwright, Cypress

**Package Managers:** npm, yarn, pnpm, bun, pip, poetry, uv, cargo, go modules, bundler, composer, pub

**Monorepos:** pnpm workspaces, Yarn workspaces, Lerna, Nx, Turborepo

</details>

---

## 🏗️ Design Principles

| Principle | What it means |
|-----------|---------------|
| **Read-first** | Analyzes actual code patterns, doesn't guess |
| **Graceful degradation** | Python missing? Graph skipped. Caveman missing? Instructions shown. Nothing blocks. |
| **Non-destructive** | Merges configs, never overwrites |
| **Project-specific** | Real data in every agent, not boilerplate |
| **Bounded teams** | Max 1 lead + 4 specialists — more agents = more coordination overhead |

---

## 📋 Requirements

| Requirement | Status |
|-------------|--------|
| Claude Code CLI | **Required** |
| Python 3.10+ | Optional (for code-review-graph) |
| Git repository | Recommended |

---

## 🤝 Contributing

PRs welcome. If you add support for a new framework or language detection, include test cases.

---

## 📜 License

MIT — use it, fork it, ship it.

---

<div align="center">

**Built by [Apyx Development Studio](https://apyx.dev)**

*Stop configuring. Start building.*

⚡

</div>
