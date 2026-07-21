---
name: using-superpowers
description: Use at the start of a task to route only clearly applicable skills and choose a proportional workflow.
---

# Skill Router

Apply user and repository instructions first. Then inspect the available skill
catalog and load only skills whose trigger clearly matches the request.

## Choose the smallest sufficient workflow

- Tier 0 — answer, explain, inspect, or make a trivial edit: act directly.
- Tier 1 — localized feature or bug with clear acceptance criteria: use one
  primary process skill, implement inline, and run focused verification.
- Tier 2 — multi-file or ambiguous change: clarify only material uncertainty,
  make a compact plan, then implement and verify.
- Tier 3 — destructive, security-sensitive, production, financial-execution, or
  architecture work: use the full relevant workflow and explicit gates.

Prefer one primary process skill. Add domain skills only when they contribute
specific knowledge. Do not stack brainstorming, planning, TDD, debugging, code
review, and verification by default.

## Context budget

- Read the relevant `SKILL.md` completely, but load only directly required
  references.
- Keep routine planning under five steps.
- Reuse existing artifacts and tests instead of restating them.
- Prefer focused tests during iteration; run broad suites only when the claimed
  completion requires them.

## Loop prevention

Do not repeat planning, auditing, or verification without new evidence. After
one failed attempt, inspect the concrete failure and change the approach. After
two failures with the same cause, stop retrying blindly and report the blocker
or pursue a materially different path.

If the user asks for direct or inline execution, do not delegate or insert
approval checkpoints unless a missing decision would materially change the
result.
