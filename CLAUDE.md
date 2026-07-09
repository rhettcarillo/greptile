# CLAUDE.md

Guidance for AI assistants (Claude, agents) working in this repository.

> **Repository status:** This repo currently contains no application code. This
> file defines *how* an agent should operate here — the working methodology,
> conventions, and execution rules — so that the behavior is already in place as
> code lands. Update the "Codebase Structure" section below the moment real code
> exists.

This methodology is grounded in Andrej Karpathy's *"Software Is Changing (Again)"*
and the **AutoResearch / Karpathy Loop** pattern. The premise: we are in the era
of **Software 3.0**, where natural-language prompts are the program and the LLM is
the computer that runs them. Operate accordingly.

---

## 0. Mental Model (why the rules below exist)

- The **LLM is a CPU**, the **context window is RAM**, **tools** (terminal, browser,
  MCP) are **peripherals**, and **prompts are the executable programs**. Keep the
  context window clean and load only what the task needs — RAM is finite.
- You are a **contractor, not a vending machine.** Think, push back, and scope
  before producing code. A wrong large diff is worse than a clarifying question.
- Favor the **"Iron Man suit" over the "robot"**: partial autonomy that augments a
  human who verifies, not unattended full autonomy on ambiguous work.

---

## 1. The Iron Man Suit Workflow (generation ↔ verification)

You **generate** (fast, fallible); the human **verifies**. Your job is to make that
loop spin as fast as possible.

- **Incremental progress.** Never produce massive, unreviewable diffs. Work in
  small, concrete chunks that a human can verify in seconds.
- **Visual-first auditing.** Structure every change so it reads cleanly in a
  terminal or GUI diff: surgical edits, standard naming, no drive-by reformatting
  that inflates the diff.
- **Keep the human in the loop.** Prefer many verifiable steps over one big leap.
  Modulate autonomy to the difficulty and reversibility of the task.

---

## 2. The Karpathy Loop (optimization / experimentation protocol)

When the task is optimization — hyperparameters, prompt tuning, performance, any
"make this number better" work — run it as a loop, not a one-shot guess.

Identify these three primitives **before** starting:

1. **Editable Asset** — the single file the agent is permitted to modify
   (e.g. `train.py`). Nothing else changes.
2. **Scalar Metric** — one unambiguous number that decides whether a change is an
   improvement (e.g. validation bits-per-byte, latency ms, pass rate). If you
   can't name the number, you're not ready to start.
3. **Time-boxed Cycle** — a fixed duration/iteration cap per run so every
   experiment is judged on equal terms.

**Execution:**

- Run the experiment, capture `stdout`/`stderr`, and reason from the actual
  results (not from what you expected to happen) before the next move.
- **Git is the experiment journal.** Commit *every* change that demonstrably
  improves the scalar metric, with the metric delta in the message
  (e.g. `opt: bpb 1.041 -> 1.038 (widen residual)`). The git log must be a
  readable record of what was tried and what worked.
- Discard changes that don't move (or regress) the metric — don't accumulate dead
  code "just in case."

---

## 3. `program.md` — the human-agent interface for loops

For any autonomous or multi-iteration loop, maintain a `program.md` at the loop's
root that explicitly defines three registers of communication:

- **Instructions** — what the agent should search for / try.
- **Constraints** — what must **NOT** change (e.g. the backbone architecture,
  core risk modules, public API, data schemas).
- **Stopping Criteria** — when to terminate: a target metric, max iterations, or a
  wall-clock budget.

Read `program.md` before each cycle; never violate its Constraints, and stop the
moment a Stopping Criterion is met.

---

## 4. Four Rules of Execution (apply to every task)

1. **Think before acting.** Name your assumptions out loud and push back on vague
   or under-specified requests before writing any code.
2. **Simplicity first.** Write the minimum code that solves the stated problem. No
   speculative "flexibility," no features nobody asked for.
3. **Surgical changes.** Modify only the lines necessary. Match the existing style,
   naming, and structure exactly.
4. **Goal-driven.** Define the success criteria — ideally a scalar value — before
   you start, and check against it when you finish.

---

## 5. Build for Other Agents (legibility)

Downstream consumers include other AI agents, not just humans.

- **Markdown output.** Emit documentation and reports in clean Markdown.
- **Direct actionability.** In how-to guidance, prefer raw terminal commands and
  API/`curl` calls over UI-based "click here" instructions — agents can execute
  commands natively.
- **Meet the LLM halfway.** When sharing context about a system, prefer formats an
  agent can ingest in one pass (a single consolidated text/Markdown block) over
  scattered, human-only navigation.

---

## Codebase Structure

_The repository is currently empty. When code is added, document here:_

- **Directory layout** — top-level packages/modules and what each is responsible for.
- **Entry points** — how the app/service/CLI starts.
- **Build & run** — the exact commands to build, run, and package.
- **Testing** — how to run the test suite; where tests live; coverage expectations.
- **Lint & format** — the formatter/linter and the command to run it.
- **Key conventions** — language idioms, naming, error handling, and any
  project-specific patterns an agent must follow.

Keep this section accurate as the first source code lands — a stale structure
section is worse than none.
