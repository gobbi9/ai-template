# Conventions

## Code conventions
- Naming:
- File organization:
- Error handling:
- Testing expectations:

## Workflow conventions
- Branch/commit style:
- Pull request checklist:
- Release notes expectations:

## AI collaboration conventions
- Keep edits minimal and scoped.
- Update `.ai/memory/active-focus.md` and append to `.ai/memory/log.md` at the end of meaningful sessions.
- Capture material decisions in `.ai/decisions/YYYYMMDD-topic.md` only when directly related.
- Capture notable failed approaches in `.ai/failures/YYYYMMDD-topic.md` only when they actually occurred.
- Never invent a decision or failure entry to satisfy process/checklist requirements.
- In `.ai/memory/log.md`, include Decision(s)/Failure(s) lines only when directly related to the session.
- Prefer root-cause fixes over quick patches.

## Diagram conventions
- Prefer GitHub-safe Mermaid syntax and simple node IDs.
- Avoid reserved/conflicting identifiers in node IDs (for example `end`; in this project also avoid `ebd`).
- If a diagram fails to render in GitHub, record the failure and lesson in `.ai/failures/`.
