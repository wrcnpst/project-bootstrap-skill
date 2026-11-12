# Project bootstrap skill

A portable Codex skill for initializing project memory and a local Git baseline safely.

## Install on another machine

Sign in to GitHub with an account that can access this private repository, and configure Git authentication. In Codex, ask:

> Use skill-installer to install `skills/project-bootstrap` from `wrcnpst/project-bootstrap-skill`.

Restart Codex or start a new session if needed for skill discovery. Then ask Codex to bootstrap a new project, or invoke `$project-bootstrap`.

The skill includes portable memory templates. If a workspace has its own applicable global protocol or template, the skill follows that instead. It initializes Git locally where appropriate and does not create a remote or publish a project without authorization.
