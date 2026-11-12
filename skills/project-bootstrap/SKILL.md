---
name: project-bootstrap
description: Bootstrap a new project with portable agent memory and a safe local Git baseline. Use when starting or initializing a project, not for routine work in an established project.
---

# Project bootstrap

Set up the requested project in its chosen directory. Respect existing project instructions, user choices, and higher-priority rules. Do not overwrite existing files or alter unrelated work.

1. Check whether the directory exists, what it contains, and whether `git rev-parse --show-toplevel` identifies an enclosing repository. Preserve existing repositories, remotes, history, and uncommitted changes. Do not initialize a nested repository without explicit authorization.
2. If a workspace's `GLOBAL.md` or project memory template exists, follow its applicable instructions. Otherwise use the five files in `assets/memory` as a portable starting point. Copy only missing files to the project root, tailor `AGENTS.md` to the project and its safety boundaries, and replace placeholders with verified facts or clearly empty sections. Do not invent architecture, decisions, or completed work. Refer to a global protocol only if it actually exists at the target location.
3. If the project is not already in a repository, run `git init` in the project root. Prepare a `.gitignore` appropriate to the actual stack and sensitive data before staging. Never weaken an existing ignore file or assume it catches every secret.
4. Inspect candidate files and staged diff for credentials, protected configuration, runtime data, generated files, and unrelated work. In an existing nonempty directory, stage only files explicitly verified safe; do not automatically stage unknown files. Create an initial commit when there are verified safe changes and Git identity is configured. If not, report what is needed; never invent an identity. Preserve any existing staged changes and do not include them in a bootstrap commit without authorization.
5. Do not create a remote, change visibility, or push to an unknown or public remote without explicit authorization. A local commit is not an off-machine backup. Report what was initialized, committed, and left pending.
