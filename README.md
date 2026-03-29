# Obsidian + Claude Code Vault

A personal knowledge management system combining **Obsidian** (PARA structure) with **Claude Code** (daily operating layer) and **Todoist** (GTD task management).

## Philosophy

One rule to remember:

> **"Do I need to DO this or KNOW this?"**
> - Need to do → **Todoist**
> - Need to know / remember / reference → **Obsidian**

Three layers:
- **KNOW** — Obsidian (PARA: Projects / Areas / Resources / Archive)
- **DO** — Todoist (GTD: Next Actions / Projects / Waiting For / Someday)
- **OPERATE** — Claude Code (daily rituals, context, AI assistance)

## Requirements

- [Obsidian](https://obsidian.md) — for the vault
- [Claude Code](https://claude.ai/code) — CLI for AI assistance
- [Todoist](https://todoist.com) — task manager (optional but recommended)
- Todoist MCP server — for Claude ↔ Todoist integration ([setup guide](https://github.com/abhiz123/todoist-mcp-server))

## Structure

```
vault/
├── 00_Inbox/          # Capture everything here first
├── 01_Projects/       # Active projects with clear outcomes
├── 02_Areas/          # Ongoing responsibilities (Health, Work, Finance…)
├── 03_Resources/      # Reference material by topic
├── 04_Archive/        # Completed / inactive items
├── _daily/            # Daily log files (YYYY-MM-DD.md)
├── _context/          # Claude operating context (session, conventions, paths)
├── _focus.md          # Weekly / monthly / daily focus — lives at root
├── _init.md           # Single entry point for Claude — read this first
├── CLAUDE.md          # Claude Code project instructions
└── .claude/
    └── commands/      # Slash command skills
        ├── morning.md
        ├── dayend.md
        └── weekly-review.md
```

## Daily Rituals

| Command | When | What it does |
|---------|------|-------------|
| `/morning` | Start of day | Briefing: Calendar + Todoist + focus + stale projects |
| `/dayend` | End of day | Captures closed tasks, updates session-context |
| `/weekly-review` | Sunday | Full sync: Todoist + projects + next week's focus |

## Setup

1. **Clone and open in Obsidian**
   ```bash
   git clone https://github.com/yourname/obsidian-claude-vault
   ```
   Open the folder as an Obsidian vault.

2. **Install Claude Code**
   ```bash
   npm install -g @anthropic-ai/claude-code
   ```

3. **Configure `CLAUDE.md`**
   Edit `CLAUDE.md` to point to your actual context files. The file is already wired — just verify paths.

4. **Set up Todoist MCP** *(optional)*
   Follow the [todoist-mcp-server](https://github.com/abhiz123/todoist-mcp-server) setup guide. Add your API token to Claude Code's MCP config.
   Create projects in Todoist matching your workflow:
   - `Next Actions / Work`
   - `Next Actions / Personal`
   - `Projects`
   - `Waiting For`
   - `Someday / Maybe`
   Add a label `focus` (orange) for weekly focus tasks.

5. **Personalize `_context/_personal-context.md`**
   Add your integrations, tools, and any Claude-specific rules.

6. **Set your first focus**
   Open `_focus.md` and fill in your monthly and weekly focus blocks.

7. **Run `/morning`**
   ```
   /morning
   ```

## Context Loading (token-lean)

Claude only loads what's needed:

- **L0** (always): `_init.md`
- **L1** (by task): `_context/_session-context.md`, `_context/_personal-context.md`, `_context/_conventions-quick.md`
- **L2** (specific): `_context/_conventions.md`, `_context/_paths.md`, `_context/_commands.md`, `_context/_glossary.md`

## Focus System

`_focus.md` at vault root contains three blocks:
- **Month** — 2-3 directions across life areas
- **Week** — 3-5 specific tasks (mirrored as `focus` label in Todoist)
- **Day** — max 3 tasks, suggested by `/morning` each morning

`/weekly-review` helps you close the week and set next week's focus. `/morning` reads the file and suggests today's top 3.

## License

MIT
