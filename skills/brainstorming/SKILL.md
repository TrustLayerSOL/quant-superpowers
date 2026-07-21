---
name: brainstorming
description: Use before ambiguous or high-rework creative implementation when user intent, behavior, or architecture is not yet sufficiently defined.
---

# Brainstorming

Turn an underspecified idea into an implementable design without delaying clear
work.

## Skip this workflow

Do not brainstorm for explanations, research, content drafting, mechanical
edits, reproducible bug fixes, approved designs, or localized Tier 0–1 work.

## Workflow

1. Inspect current project context and existing constraints.
2. Identify only decisions that could materially change the implementation.
3. Ask one concise question at a time when those decisions cannot be inferred.
4. Offer two or three viable approaches only when a real tradeoff exists.
5. Recommend one approach with its cost, risk, and scope.
6. Present a compact design covering behavior, data flow, failure handling, and
   verification.
7. Obtain approval only before material or irreversible implementation.

For a small feature, the design may be one paragraph. For architecture work,
split it into short sections and confirm the direction once, not after every
section.

Do not create speculative requirements, schedule-shaped plans, or unrelated
future work. Once the design is adequate and approved, proceed directly to the
appropriate implementation workflow.
