---
name: reflex
description: Self-improvement loop — run at the end of every session or autonomous run to extract corrections, update Skills, and categorize learnings by confidence. Use when a session is wrapping up, when a task failed and should not fail the same way again, or when the user asks you to "learn from this" / "remember this".
---

# Reflex Skill

The Reflex Skill is the self-improvement loop described in `CLAUDE.md` §4. Run it
at the end of every session or autonomous run so that corrections persist and the
system "corrects once and never again."

## Procedure

### 1. Extract Corrections

Scan the conversation (and any run logs) for:

- **Human corrections** — places where the user redirected, rejected, or fixed
  your output.
- **Logic errors** — reasoning that produced a wrong result.
- **Task-level failures** — tests that failed, metrics that regressed, goals
  that were missed.

For each, write one line: *what happened* → *the corrected behavior*.

### 2. Update Skills

If a failure occurred that could recur:

1. Find the relevant Skill file under `.claude/skills/`.
2. If none exists, create a new one: `.claude/skills/<name>/SKILL.md` with YAML
   frontmatter (`name`, `description`).
3. Add the corrected behavior as a concrete, actionable rule — not a vague
   platitude. Make the change **surgical**: append or edit the smallest amount
   needed.

### 3. Confidence Categorization

Label each new learning:

- **High** — confirmed success (verified by a passing test or accepted output).
- **Medium** — a pattern that worked well but is not independently verified.
- **Low** — an observation to review later; do not act on it as fact yet.

Record High/Medium learnings in the appropriate Skill file. Keep Low learnings
in `.claude/skills/reflex/observations.md` for future review.

### 4. Journal to Git

Commit Skill updates with a message that names the correction, e.g.:

```
skills: correct <behavior> after <failure> [confidence: High]
```

The git history is the memory. If nothing changed, commit nothing.
