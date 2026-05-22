# .ai Workspace Guide

This file documents prompts, skills, and core artifacts under `.ai` for this bootstrap template.

## Prompts

- `prompts/start-session.md`: session bootstrap prompt that loads project context, memory, policy, and decision notes.
- `prompts/end-session.md`: session close-out prompt that updates memory artifacts, optional decision/failure notes, and refreshes `manifest.yaml`.

## Skills

- `skills/memento/skill.md`: maintains session-to-session memory continuity.
- `skills/theory-of-mind/skill.md`: seeds context and memory from historical threads/logs.
- `skills/ai-janitor/skill.md`: keeps `.ai/manifest.yaml` synchronized with `.ai` structure changes.
- `skills/docs/skill.md`: updates root `README.md` only when non-`.ai` files changed.

## Core Files

- `manifest.yaml`: canonical index of `.ai` structure and skill metadata.
- `context/architecture.md`: architecture summary, boundaries, and system-level concerns.
- `context/conventions.md`: engineering and collaboration conventions.
- `context/glossary.md`: project terminology and acronyms.
- `memory/active-focus.md`: current objective, in-flight tasks, and immediate next actions.
- `memory/log.md`: long-term chronological memory log; decision/failure links are optional and only added when directly related.
- `decisions/YYYYMMDD-placeholder.md`: starter template for dated ADR-style decisions.
- `failures/YYYYMMDD-placeholder.md`: starter template for dated failure notes.
- `policies/coding-style.md`: coding and documentation policy baseline.

## Dependency Graph

### Start-session flow

```mermaid
graph LR
  start["prompts/start-session.md"] --> memento["skills/memento/skill.md"]
  start --> architecture["context/architecture.md"]
  start --> conventions["context/conventions.md"]
  start --> glossary["context/glossary.md"]
  start --> active["memory/active-focus.md"]
  start --> log["memory/log.md"]
  start --> policy["policies/coding-style.md"]
  start --> decisionsDir["decisions/*.md"]
```

### End-session flow

```mermaid
graph LR
  endSession["prompts/end-session.md"] --> memento["skills/memento/skill.md"]
  endSession --> janitor["skills/ai-janitor/skill.md"]
  endSession --> docs["skills/docs/skill.md"]

  memento --> active["memory/active-focus.md"]
  memento --> log["memory/log.md"]
  memento --> decisionsDir["decisions/*.md"]
  memento --> failuresDir["failures/*.md"]

  janitor --> manifest["manifest.yaml"]
  docs --> projectReadme["../README.md"]
```
