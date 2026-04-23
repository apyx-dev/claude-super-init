# Contributing

Improvements to agent templates, tech detection, and the init skill are welcome — open a PR with before/after examples showing the change.

## How

1. Fork repo
2. Edit the relevant file:
   - **Agent templates:** `skills/init/references/agent-*.md`
   - **Init skill logic:** `skills/init/SKILL.md`
   - **Tech detection:** `scripts/analyze-project.sh`
3. Open PR with:
   - **Before:** what super-init does now
   - **After:** what super-init does with your change
   - One sentence why change better

## What to contribute

- New framework/language detection in `analyze-project.sh`
- Better agent template prompts (with before/after examples)
- New agent types for unserved domains
- Bug fixes in detection or generation logic

See [issues labeled `good first issue`](../../issues?q=label%3A%22good+first+issue%22) for starter tasks.

## Guidelines

- Small focused change > big rewrite
- Test with a real project before submitting
- Agent templates must use `{{PLACEHOLDER}}` syntax for project-specific data
- Detection scripts must handle missing tools gracefully (no hard failures)
