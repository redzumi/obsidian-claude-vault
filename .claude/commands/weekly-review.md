---
description: Weekly review ritual (Todoist Waiting For + project check-in + focus)
allowed-tools: [Read, Write, Edit, Bash, Task]
---

# Weekly Review

Trigger phrases: "weekly review", "let's do weekly review", "review the week".

## Steps (strict order)

1. **Todoist: Waiting For**
   - Use Todoist MCP to list tasks from the "Waiting For" project.
   - Highlight tasks stuck > 5 days.
   - Do not complete / update tasks unless user explicitly says so.

2. **Inbox processing**
   - Check `00_Inbox/` for unprocessed files.
   - For each item: suggest where it belongs in PARA or if it can be deleted.

3. **Project check-in**
   - Read `_context/_session-context.md`.
   - For each active project: ask for status update and next step.
   - Update `Status:` and `updated:` for mentioned projects.

4. **Focus of the week**
   - Read `_focus.md`.
   - Summarize last week: what from the focus was done, what wasn't.
   - Based on session-context + Todoist (p1/p2 + `focus` label), propose next week's focus:
     - 2-3 tasks across projects (Work / Personal / Side projects)
     - 1 intentional "not doing this week"
   - After confirmation — update the "Week" block in `_focus.md` with new dates and tasks.
   - Tag chosen tasks with `focus` label in Todoist.

5. **Create weekly review note** *(optional)*
   - Create a new file `_daily/YYYY-MM-DD-weekly-review.md` with a summary of decisions made.
