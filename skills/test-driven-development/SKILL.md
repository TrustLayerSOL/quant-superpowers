---
name: test-driven-development
description: Use when implementing behavior-changing features or bug fixes where an executable regression test can define the contract.
---

# Test-Driven Development

Use tests to prove the behavior boundary, not to create ceremony.

## Core loop

1. Write the smallest test that expresses the desired behavior or reproduces the
   bug.
2. Run it and confirm it fails for the expected reason.
3. Implement the smallest coherent change.
4. Run the focused test and nearby regression tests.
5. Refactor only while tests remain green.

For several tightly related Tier 1 cases, write a small failing batch before the
implementation. Keep each failure attributable to the intended missing
behavior.

## Exceptions

Do not force test-first work for prose, static configuration, generated
metadata, formatting-only changes, or mechanical refactors already covered by
strong tests. Validate those artifacts directly.

Do not write tests for private implementation details or mock the exact code you
intend to write. Test public behavior, observable state, important failure
paths, and boundary conditions.

If the test unexpectedly passes, determine whether the behavior already exists
or the test is ineffective before coding. If the implementation fails, inspect
the actual failure rather than weakening the assertion.

Finish with focused evidence. Run the broader suite only when the change has
broad impact or the completion claim depends on it.
