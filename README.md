# Super Init

One-command project initialization for Claude Code. Analyzes your codebase and sets up everything for multi-agent workflows.

## What it does

1. **Installs code-review-graph** - builds a code knowledge graph that reduces token usage by up to 49x
2. **Installs caveman plugin** - ultra-compressed communication for ~75% token savings
3. **Configures MCP servers** - sets up `.mcp.json` + `.claude/settings.local.json` with needed MCP servers (Playwright for QA, code-review-graph for smart context)
4. **Generates `.claude/agents/`** - team lead + role-specific agents tailored to your actual tech stack

## Install

```bash
claude plugin install super-init@claude-super-init
```

Or add the marketplace:

```bash
claude marketplace add github:apyx-dev/claude-super-init
claude plugin install super-init
```

## Usage

Navigate to any project and run:

```
/super-init
```

### Options

| Command | What runs |
|---------|-----------|
| `/super-init` | Everything (graph + caveman + agents) |
| `/super-init --no-graph` | Skip code-review-graph |
| `/super-init --no-caveman` | Skip caveman plugin |
| `/super-init --no-agents` | Skip agent generation |
| `/super-init --no-mcp` | Skip MCP server configuration |
| `/super-init --agents-only` | Only analyze + generate agents |
| `/super-init --graph-only` | Only install code-review-graph |
| `/super-init --caveman-only` | Only install caveman |
| `/super-init --mcp-only` | Only configure MCP servers |
| `/super-init --rebuild` | Overwrite existing agents + rebuild graph |

Combine flags: `/super-init --no-graph --no-caveman` = agents only.

## Generated Agents

| Agent | When Generated | Purpose |
|-------|---------------|---------|
| `lead.md` | Always | Team orchestrator - decomposes tasks, delegates to specialists |
| `backend.md` | Backend framework or server code detected | API/service development |
| `frontend.md` | Frontend framework or UI code detected | Components, pages, styling |
| `mobile.md` | React Native, Flutter, or native mobile code | Mobile app development |
| `devops.md` | Docker, CI/CD, or infrastructure configs | Infrastructure and deployment |
| `qa.md` | Test framework detected | Browser-based E2E testing |

Each agent is populated with your project's actual:
- Stack versions and dependencies
- Directory layout
- Architecture patterns (discovered by reading source files)
- Coding conventions
- Build/lint/test commands

## Supported Tech Detection

**Languages:** TypeScript, JavaScript, Python, Go, Rust, Java, Kotlin, Swift, Ruby, PHP, C#, Dart, Vue, Svelte

**Frontend:** React, Vue, Angular, Svelte, Next.js, Nuxt, Astro, Gatsby, Remix, Solid

**Backend:** Express, Koa, Fastify, NestJS, Hono, Django, Flask, FastAPI, Laravel, Symfony, Gin, Chi, Fiber, Actix, Axum, Rocket, Ktor, Vapor

**Mobile:** React Native, Expo, Flutter, Capacitor, Ionic, native iOS/Android

**Infrastructure:** Docker, GitHub Actions, GitLab CI, Jenkins, Terraform, Kubernetes, Serverless, Vercel, Netlify, Fly.io

**Databases:** Prisma, Drizzle, Mongoose, TypeORM, Sequelize, SQLAlchemy

**Testing:** Jest, Vitest, Playwright, Cypress

**Package Managers:** npm, yarn, pnpm, bun, pip, poetry, uv, cargo, go modules, bundler, composer, pub

## Requirements

- Claude Code CLI
- Python 3.10+ (for code-review-graph - optional, skipped if unavailable)
- Git repository (recommended)

## License

MIT
