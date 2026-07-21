# Quant Superpowers

Quant Superpowers is a quant-focused adaptation of [obra/superpowers](https://github.com/obra/superpowers) for OpenAI Codex. It keeps the composable planning, testing, debugging, verification, and delivery workflows while replacing the highest-frequency process skills with compact, proportional versions suited to quantitative research and trading-system engineering.

The goal is more useful autonomy with less ceremony: use the smallest safe workflow, prevent repeated planning and audit loops, control context and token use, and match verification effort to the claim being made.

## What changed

Eight high-frequency Superpowers workflows were rewritten:

- `using-superpowers`
- `brainstorming`
- `test-driven-development`
- `systematic-debugging`
- `executing-plans`
- `verification-before-completion`
- `writing-plans`
- `writing-skills`

The modified router introduces:

- proportional Tier 0–3 workflows;
- compact planning and context budgets;
- loop prevention after repeated failures;
- focused verification for focused claims;
- explicit escalation for destructive, production, financial-execution, or architectural work; and
- inline execution once scope is clear.

The remaining compatible Superpowers skills and their supporting scripts and references are retained so the workflow remains complete.

## Designed for

- quantitative and market research;
- leakage-safe replay and backtesting;
- trading-bot design and implementation;
- market-data capture and validation;
- strategy and feature engineering;
- systematic debugging;
- evidence-backed verification; and
- guarded progression toward execution.

## Install for OpenAI Codex

### 1. Clone the repository

```bash
git clone https://github.com/TrustLayerSOL/quant-superpowers.git ~/.codex/quant-superpowers
```

### 2. Make the skills globally available

Codex discovers user-level skills under `~/.agents/skills`. The following keeps the conventional `superpowers` discovery path while pointing it at Quant Superpowers:

```bash
mkdir -p ~/.agents/skills

if [ -L ~/.agents/skills/superpowers ]; then
  unlink ~/.agents/skills/superpowers
fi

ln -s ~/.codex/quant-superpowers/skills ~/.agents/skills/superpowers
```

If `~/.agents/skills/superpowers` is a real directory rather than a symlink, move or back it up manually before installing. Do not enable the original Superpowers bundle and Quant Superpowers simultaneously because both provide skills with the same names.

### 3. Restart Codex

Quit and reopen Codex so it discovers the skills. They will then be available across existing and future repositories for that user account.

### Verify

```bash
ls -la ~/.agents/skills/superpowers
ls ~/.codex/quant-superpowers/skills
```

## Update

```bash
git -C ~/.codex/quant-superpowers pull
```

Restart Codex if updated skills do not appear immediately.

## Uninstall

Remove only the discovery symlink:

```bash
if [ -L ~/.agents/skills/superpowers ]; then
  unlink ~/.agents/skills/superpowers
fi
```

The cloned repository remains at `~/.codex/quant-superpowers` unless you choose to remove it separately.

## Packaging

The repository stores the skills as normal source directories, with one `SKILL.md` per skill plus any required scripts and references. A committed ZIP is intentionally not included: GitHub provides source ZIP downloads automatically, while a Git clone preserves provenance and supports updates.

The Codex plugin manifest is located at `.codex-plugin/plugin.json`.

## Version provenance

The initial Quant Superpowers release preserves the locally validated workflow based on upstream Superpowers `v5.0.7` / commit `6efe32c`. It does not silently rebase the customized workflow onto a newer upstream release.

## Attribution and license

Quant Superpowers is a modified derivative of [obra/superpowers](https://github.com/obra/superpowers), created by Jesse Vincent and contributors. The upstream project is licensed under the MIT License.

The original copyright and MIT permission notice are retained in [LICENSE](LICENSE). See [ATTRIBUTION.md](ATTRIBUTION.md) for modification details.

Copyright © 2026 TrustLayerSOL for the Quant Superpowers modifications.
