---
name: verification-before-completion
description: Use before claiming a change is complete, fixed, passing, or ready, and before commits or pull requests.
---

# Verify Before Claiming Completion

Match evidence to the exact claim.

1. State what must be true.
2. Select the cheapest fresh command or inspection that proves it.
3. Run it after the final change.
4. Read the exit status and relevant output.
5. Report the claim, evidence, and any remaining limitation.

Examples:

- A localized bug fix needs its reproduction plus focused regressions.
- A generated config needs schema or structural validation.
- A UI flow needs a real browser-path check when practical.
- A repository-ready claim needs the appropriate broader test, lint, or build
  suite.

Do not infer success from earlier runs, code inspection alone, or another
agent's report. Do not run the entire suite after every edit; reserve broad
verification for integration boundaries or broad claims.

If verification cannot run, say exactly why and narrow the completion claim.
