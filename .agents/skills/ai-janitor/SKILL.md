# AI Janitor

Maintain `.agents/manifest.yaml` as the canonical index of this `.agents` workspace.

## Responsibility

Whenever files under `.agents/` are added, renamed, or removed, refresh `.agents/manifest.yaml`.

## Checklist

1. Ensure session-skill, context, memory, decision, policy, and skill paths are valid.
2. Ensure each skill directory includes `skill.yaml` and `SKILL.md`.
3. Remove stale entries and keep ordering stable for readable diffs.
4. Keep descriptions concise and practical.
