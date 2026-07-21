---
name: writing-skills
description: Use when creating, editing, or validating reusable Codex skills and their bundled resources.
---

# Write Effective Skills

Keep the loaded instruction small and move optional depth into directly linked
references.

## Workflow

1. Define the trigger precisely in the frontmatter description.
2. Identify non-obvious reusable procedure, domain rules, scripts, references,
   and assets.
3. Scaffold new skills with the supported initializer.
4. Write imperative instructions with one clear workflow, proportional
   branches, and explicit stop conditions.
5. Avoid generic advice, duplicated platform rules, long rationalizations, and
   examples that do not change execution.
6. Validate frontmatter, naming, metadata, links, and any bundled scripts.
7. Forward-test only complex discipline-enforcing skills or changes whose
   failure would be costly. Use lightweight scenarios for wording and routing
   changes.

Target fewer than 500 lines and preferably fewer than 500 words for frequently
loaded skills. Put schemas, examples, and deep domain material in `references/`
and instruct the agent exactly when to read them.

For `agents/openai.yaml`, quote strings, keep the UI description concise, and
make the default prompt explicitly mention `$skill-name`.

Do not use subagents merely to satisfy a process checklist. Do not repeat
validation after unchanged output. Finish with the exact validator evidence and
the skill paths created or changed.
