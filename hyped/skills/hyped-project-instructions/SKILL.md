---
name: hyped-project-instructions
description: Use when starting or resuming work inside a Hyped-bound project, when project/worktree context changes, or when instructions may affect the answer.
---

# Hyped Project Instructions

Before doing project work in Hyped, treat the current working directory as the
authoritative bound project context. Read and follow project instruction files
that apply to that directory, especially `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`,
and relevant documents under `docs/` when the request touches architecture,
testing, deployment, provider runtime behavior, storage, observability, or
release behavior.

If the visible conversation mentions a different project, worktree, branch, or
CWD than the active runtime context, do not silently continue. Surface the
mismatch clearly and ask the user to switch the project or confirm the intended
target before making durable changes.

Remember that `/project find <query>` only finds candidates. It does not change
the active agent binding. The active project changes only after a successful
bind/switch command such as `/project switch <project-id>` or a clone flow that
binds the conversation.

When reporting status back to the user, distinguish what was actually verified
from adjacent confidence signals. Do not claim a live deployment, provider,
plugin, or project binding is fixed unless the relevant e2e or live check proves
that exact boundary.
