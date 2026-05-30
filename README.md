# AI Template Bootstrap

This repository contains a reusable `.agents` bootstrap structure for new projects. See [.agents/README.md](.agents/README.md).

## Included structure

```text
.agents/
  manifest.yaml
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
      SKILL.md
  policies/
    coding-style.md
```

## Quick start

1. Copy `.agents/` into a target project.
2. Fill out `context/*` with project-specific details.
3. Use `skills/start-session/SKILL.md` at the beginning of work sessions.
4. Use `skills/end-session/SKILL.md` before ending a session.
5. Record important decisions in `.agents/decisions/YYYYMMDD-topic.md`.
6. Record important failures in `.agents/failures/YYYYMMDD-topic.md`.
