# Installing Quant Superpowers for Codex

Enable Quant Superpowers globally through Codex native skill discovery.

## Prerequisites

- Git
- OpenAI Codex

## Install

1. Clone the repository:

```bash
git clone https://github.com/TrustLayerSOL/quant-superpowers.git ~/.codex/quant-superpowers
```

2. Point the global Superpowers discovery path at the clone:

```bash
mkdir -p ~/.agents/skills

if [ -L ~/.agents/skills/superpowers ]; then
  unlink ~/.agents/skills/superpowers
fi

ln -s ~/.codex/quant-superpowers/skills ~/.agents/skills/superpowers
```

If `~/.agents/skills/superpowers` is a real directory instead of a symlink, move or back it up manually. Do not install Quant Superpowers alongside the original Superpowers bundle because they contain skills with the same names.

3. Restart Codex.

## Verify

```bash
ls -la ~/.agents/skills/superpowers
```

The path should be a symlink to `~/.codex/quant-superpowers/skills`.

## Update

```bash
git -C ~/.codex/quant-superpowers pull
```

Restart Codex if the updated skills do not appear immediately.

## Uninstall

```bash
if [ -L ~/.agents/skills/superpowers ]; then
  unlink ~/.agents/skills/superpowers
fi
```
