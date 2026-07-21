---
name: executing-plans
description: Use when an approved written implementation plan exists and the task is to carry it through to verified completion.
---

# Execute an Approved Plan

Treat the plan as the contract for outcomes, not an immutable sequence of
commands.

1. Read the plan and current repository state.
2. Flag only contradictions, unsafe steps, or missing decisions that materially
   block execution.
3. Work through coherent batches while preserving user changes.
4. Use subagents only when the user allows delegation and independent work will
   materially reduce elapsed time.
5. Run focused verification after each risky boundary and full verification
   once before the final completion claim.
6. Report deviations, evidence, remaining limitations, and the next logical
   step.

Do not pause for routine checkpoints when the user requested direct progress.
Do not re-plan completed work or repeat a failed command without new evidence.
