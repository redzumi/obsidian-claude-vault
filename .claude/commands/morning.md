# /morning — Morning Briefing

Runs at the start of the day. Gives a full picture without unnecessary questions.

## Algorithm

### Step 1 — Load context
Read `_context/_session-context.md` and `_focus.md`.

### Step 2 — Get tasks from Todoist
Call Todoist MCP:
- All tasks due today or overdue (`today | overdue`)
- Tasks with priority p1/p2 and no due date
- Tasks with label `focus`

### Step 3 — Get events from Google Calendar
Call Google Calendar MCP: today's events.

### Step 4 — Stale project detector
Go through projects in session-context. If a project's `updated:` is older than 7 days — add to "Needs attention" section.

### Step 5 — Build briefing

Output in this order:

---

## ☀️ Good morning, [date]

### 📅 Calendar today
[list of events or "no events"]

### 🗓️ Monthly focus
[from _focus.md — 2-3 directions]

### 📌 Weekly focus
[from _focus.md — tasks with `focus` label or explicitly listed]

### ✅ Tasks today
[overdue and today's tasks from Todoist, grouped by project]

### 🔥 Priority backlog (p1/p2, no date)
[important tasks not tied to a date]

### ⚠️ Projects with no updates > 7 days
[list of projects with old updated: date]

### 🎯 Focus of the day — top 3
[3 specific tasks for today: based on weekly focus + deadlines + priorities]

---

## Briefing Rules

- Don't read extra files — only session-context + _focus.md + Todoist + Calendar
- Don't ask clarifying questions — just give the picture
- If Calendar MCP is unavailable — skip that block silently
- Focus of the day — max 3 tasks, chosen from weekly focus tasks + today's deadlines
- After briefing, offer to update `_focus.md` if weekly focus has changed
