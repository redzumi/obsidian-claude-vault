# /dayend — End of Day

A 3-5 minute closing ritual. Captures the day, updates context.

## Algorithm

### Step 1 — Three questions (ask sequentially, wait for each answer)

**Question 1:** What did you close / finish today?
*(tasks completed, decisions made, things shipped)*

**Question 2:** Any project status changes?
*(new blockers, priorities shifted, something parked or activated)*

**Question 3:** Anything to add to Todoist for tomorrow or this week?

---

### Step 2 — Update session-context

Based on answers to questions 1 and 2:
- Update `Status:` and `updated:` for changed projects in `_context/_session-context.md`
- Don't touch projects that weren't mentioned

### Step 3 — Add tasks to Todoist

Based on answer to question 3:
- Add tasks via Todoist MCP (check for duplicates first)
- Default project: Next Actions / Personal or Next Actions / Work depending on context

### Step 4 — Create / update daily log

Create or update `_daily/YYYY-MM-DD.md` using `_daily/_template.md`:
- **Done** — from question 1
- **Tomorrow** — from question 3
- **Notes** — any extra thoughts mentioned

---

## Rules

- Keep it short — 3-5 minutes max
- Don't ask for more than what's in the 3 questions
- Don't update projects not mentioned in answers
- If user says "nothing" to a question — skip that step
