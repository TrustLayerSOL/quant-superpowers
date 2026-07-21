---
name: writing-plans
description: Use when a multi-step implementation needs a written plan before coding because scope, dependencies, or sequencing are material.
---

# Write an Implementation Plan

Produce an executable map, not a transcript of imagined keystrokes.

1. Inspect the relevant repository state, instructions, and tests.
2. State the objective, non-goals, constraints, and acceptance criteria.
3. Divide work into coherent tasks of roughly 15–60 minutes.
4. For each task, name the files or components, behavioral change, focused
   verification, and dependency on earlier work.
5. Put risky assumptions and irreversible actions before dependent work.
6. End with integration verification and handoff.

Keep routine plans under five steps. Use more detail only when independent
contributors or high-risk sequencing require it.

Prefer inline execution in the current task unless the user explicitly wants a
separate session, handoff, or subagent workflow. Avoid calendar estimates,
redundant reviews, speculative future phases, and one-step-per-line mechanical
plans.
