# AI Janitor

Maintain `.ai/manifest.yaml` as the canonical index of this `.ai` workspace.

## Responsibility

Whenever files under `.ai/` are added, renamed, or removed, refresh `.ai/manifest.yaml`.

## Checklist

1. Ensure prompt, context, memory, decision, policy, and skill paths are valid.
2. Ensure each skill directory includes `skill.yaml` and `skill.md`.
3. Remove stale entries and keep ordering stable for readable diffs.
4. Keep descriptions concise and practical.
