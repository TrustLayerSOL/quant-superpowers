---
name: systematic-debugging
description: Use for bugs, failing tests, and unexpected runtime behavior when the cause is not already proven.
---

# Systematic Debugging

Find the earliest incorrect state before changing code.

## Localized fast path

For a clear, reproducible fault:

1. Reproduce it once and capture the exact error or wrong value.
2. Trace the failing path to the first violated assumption.
3. Add or identify a regression check.
4. Apply one causal fix.
5. Re-run the reproduction and focused regressions.

## Broader investigation

When the failure is intermittent or crosses components:

1. Separate symptoms from confirmed facts.
2. Inspect logs, inputs, boundaries, state transitions, and recent changes.
3. Compare a working and failing case.
4. Form one falsifiable hypothesis.
5. Run the cheapest discriminating experiment.
6. Fix only after evidence identifies the cause.

Do not stack speculative patches, increase timeouts without evidence, or restart
services repeatedly as a substitute for diagnosis. After two attempts fail for
the same reason, revisit the model of the system or report the exact blocker.

Document the root cause, the changed invariant, and the verification evidence.
Keep unrelated cleanup out of the fix.
