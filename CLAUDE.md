# Super Init

Claude Code plugin that sets up multi-agent workflows in one command. Analyzes project, installs tools, generates tailored agents.

## Structure

- `skills/init/SKILL.md` — main skill prompt (all init logic lives here)
- `skills/init/references/agent-*.md` — agent templates with `{{PLACEHOLDER}}` syntax
- `scripts/analyze-project.sh` — tech stack detection script
- `.claude-plugin/plugin.json` — plugin manifest

## Rules

- Agent templates use `{{PLACEHOLDER}}` syntax — never hardcode project-specific values
- `analyze-project.sh` must handle missing tools gracefully (no hard exits)
- All phases run sequentially (1-7), never parallel
- Max 1 lead + 4 specialist agents per project
- Never overwrite existing `CLAUDE.md` or agents without user confirmation
- MCP server entries only added when underlying tool is available

## Commands

- `bash scripts/analyze-project.sh <path>` — run tech detection standalone

## Contributing

See `CONTRIBUTING.md`. PRs need before/after examples.
