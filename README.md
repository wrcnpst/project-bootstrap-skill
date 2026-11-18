# Project bootstrap skill

A portable Codex skill for initializing project memory and a local Git baseline safely.

## Install on another machine

In Codex, ask:

> Use skill-installer to install `skills/project-bootstrap` from `wrcnpst/project-bootstrap-skill`.

Restart Codex or start a new session if needed for skill discovery. Then ask Codex to bootstrap a new project, or invoke `$project-bootstrap`.

The skill includes portable memory templates. If a workspace has its own applicable global protocol or template, the skill follows that instead. It organizes project materials into suitable folders while respecting existing structure and references, initializes Git locally where appropriate, and does not create a remote or publish a project without authorization.

For new projects, `AGENTS.md` stays at the project root so agents can discover it; `STATE.md`, `TODO.md`, `DECISIONS.md`, and `HISTORY.md` go in `memory/`. Existing project memory layouts are preserved unless reorganization is requested.
