# Conventions (Quick Reference)

## 0) Core Rule

> "Do I need to DO this or KNOW this?"
> - Need to do → **Todoist**
> - Need to know / remember / reference → **Obsidian**

No checkboxes `- [ ]` in Obsidian project files. Tasks go to Todoist.

Rituals: `/morning` · `/dayend` · `/weekly-review`

---

## 1) PARA Structure

| Folder | What goes here |
|--------|---------------|
| `00_Inbox/` | Unprocessed captures |
| `01_Projects/` | Active work with a clear outcome |
| `02_Areas/` | Ongoing responsibilities |
| `03_Resources/` | Reference by topic |
| `04_Archive/` | Completed / inactive |

---

## 2) Project File Format

Each project in `01_Projects/` has an `_index.md` with:

```yaml
---
title: Project Name
status: active | parked | done
updated: YYYY-MM-DD
people: [person1, person2]   # links to 02_Areas/People/
---
```

---

## 3) Session Context Format

`_context/_session-context.md` — project statuses only, no tasks:

```
### Project Name
- updated: YYYY-MM-DD
- Status: active
- Notes: one line of context
```

---

## 4) Focus

`_focus.md` (vault root) — month / week / day focus blocks.
Updated in `/morning` (day) and `/weekly-review` (week).
Weekly focus tasks tagged with `focus` label in Todoist.

---

## 5) Daily Log

`_daily/YYYY-MM-DD.md` — created / updated by `/dayend`.
Template: `_daily/_template.md`.
