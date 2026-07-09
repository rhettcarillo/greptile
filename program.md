# program.md — Autonomous Loop Strategy

This file stores the instructions, constraints, and stopping criteria for
autonomous optimization loops. Update it before starting any Karpathy Loop
(see `CLAUDE.md` §3).

## Objective

<!-- What are you optimizing? State it in one sentence. -->

## Editable Asset

<!-- The single file or configuration you are permitted to modify. -->

## Scalar Metric

<!-- The single, unambiguous number that decides whether a change is an
     improvement. Must be computable without human judgment. -->

- **Definition:**
- **Direction:** <!-- maximize | minimize -->
- **Command to compute:**

## Constraints

<!-- Hard limits: files you must NOT touch, time/compute budgets, style rules. -->

## Cycle Configuration

- **Cycle duration (time-box):**
- **Baseline metric value:**
- **Current best metric value:**

## Stopping Criteria

<!-- When does the loop end? e.g. "metric plateaus for N cycles",
     "metric reaches target X", "budget exhausted". -->

## Journal

Every change that demonstrably improves the metric is committed to Git. The git
history is the experiment journal — see `git log` for the record of what worked.
