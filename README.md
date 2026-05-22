# AI Template Bootstrap

This repository contains a reusable `.ai` bootstrap structure for new projects.

## Included structure

```text
.ai/
  manifest.yaml
  prompts/
    start-session.md
    end-session.md
  context/
    architecture.md
    conventions.md
    glossary.md
  memory/
    active-focus.md
    log.md
  decisions/
    YYYYMMDD-placeholder.md
  failures/
    YYYYMMDD-topic.md
  skills/
    <skill-name>/
      skill.yaml
      skill.md
  policies/
    coding-style.md
```

## Quick start

1. Copy `.ai/` into a target project.
2. Fill out `context/*` with project-specific details.
3. Use `prompts/start-session.md` at the beginning of work sessions.
4. Use `prompts/end-session.md` before ending a session.
5. Record important decisions in `.ai/decisions/YYYYMMDD-topic.md`.
6. Record important failures in `.ai/failures/YYYYMMDD-topic.md`.
