# OpenCode Integration

This workspace is configured for OpenCode and Antigravity.

## Job search CLI tools

Portal search skills are installed under `.agents/skills/` and symlinked here at `.opencode/skills/`. Each skill contains a TypeScript CLI under `cli/` that runs with Bun.

Installed portals:
- freehire-search
- jobbank-search
- jobdanmark-search
- jobindex-search
- jobnet-search
- linkedin-search

## Prerequisites

- Bun 1.4+ is required. Installed to `~/.bun/bin/bun`. Add to PATH:
  ```bash
  export PATH="$HOME/.bun/bin:$PATH"
  ```
- All CLIs have been run through `bun install` in their `cli/` directories.

## Usage

The skills are portable Agent Skills with `SKILL.md` frontmatter. OpenCode/Antigravity can discover them via this `.opencode/skills` symlink.

Run a portal directly:
```bash
bun run .agents/skills/freehire-search/cli/src/cli.ts search -q "backend engineer" --region eu --format table
```

The canonical profile and workflow specifications remain in `.claude/` and `CLAUDE.md` as the single source of truth. The thin-pointer design keeps portal skills decoupled from the Claude-specific command files.
