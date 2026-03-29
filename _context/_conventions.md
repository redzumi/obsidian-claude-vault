# Conventions (Full Specification)

> Quick reference → `_context/_conventions-quick.md`
> This file: full spec, read only when needed for structure / formatting tasks.

---

## 0) Core Rule

> "Do I need to DO this or KNOW this?"
> - Need to do → **Todoist**
> - Need to know / remember / reference → **Obsidian**

No `- [ ]` checkboxes in Obsidian project files. All actionable tasks go to Todoist.

---

## 1) PARA Structure

| Folder | What goes here | Examples |
|--------|---------------|---------|
| `00_Inbox/` | Unprocessed captures — process weekly | voice memos, links, raw notes |
| `01_Projects/` | Has a clear outcome + deadline | "Launch website", "Q1 report" |
| `02_Areas/` | Ongoing responsibilities, no end date | Health, Finance, Work, Learning |
| `03_Resources/` | Reference by topic, not tied to outcome | AI tools, book notes, recipes |
| `04_Archive/` | Completed, inactive, or superseded | old projects, deprecated files |

### Project lifecycle
- New project → `01_Projects/project-name/_index.md`
- Project completes / parks → move folder to `04_Archive/`
- Reference material from project → move relevant parts to `03_Resources/`

---

## 2) File Naming

- Folders: `kebab-case`
- Notes: `YYYY-MM-DD-title.md` for dated content, `_index.md` for project roots
- Prefix `_` for system files (`_init.md`, `_focus.md`, `_index.md`)

---

## 3) Frontmatter Template

### 01_Projects

```yaml
---
title: Project Name
status: active | parked | done
updated: YYYY-MM-DD
people: [person1, person2]
---
```

### 02_Areas

```yaml
---
title: Area Name
updated: YYYY-MM-DD
---
```

---

## 4) Session Context Format

`_context/_session-context.md` — statuses only, no tasks:

```
### Project Name
- updated: YYYY-MM-DD
- Status: active | parked | done
- Notes: one-line context or next step
```

Rule: if `updated:` is older than 7 days → flag as stale in `/morning`.

---

## 5) People

Contacts live in `02_Areas/People/`. Each person has a file.
Reference people from project files via `people:` frontmatter field.

---

## 6) Inbox Processing

Process `00_Inbox/` at least once a week (during `/weekly-review`).
For each item: file it to PARA → or delete → never leave tasks in Obsidian.

---

## 7) Focus System

`_focus.md` (vault root):
- **Month block** — 2-3 directions across life areas
- **Week block** — 3-5 specific tasks, mirrored as `focus` label in Todoist
- **Day block** — max 3 tasks, suggested by `/morning`

Updated: day block → `/morning`, week block → `/weekly-review`.
