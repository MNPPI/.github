# Agent instructions

This repository is `MNPPI/.github`: the organization profile README and
related meta content. It is not an application codebase.

## Scope

- Edit profile and docs content under `profile/` and `docs/` as needed.
- Existing GitHub meta this repo already owns (`.github/`, `SECURITY.md`,
  this file) is in scope only when the task is about that owned content.
- There is no installable runtime, package manager lockfile, or app build.
- Do not add Docker, Node, or Python bootstrap scripts unless this repo
  gains real installable code.

## Guardrails

- Keep changes small and reviewable.
- Do not invent deploy or CI contracts that this meta repo does not own.
  You may edit the reusable public workflows already published here when
  asked. Refuse new app CI, deploy pipelines, secrets contracts, package
  managers (pnpm, uv, npm, pip), or Docker added only to look "complete."

## Cursor Cloud specific instructions

There is nothing to build or install. Cloud Agents should only edit
meta and docs content.

- `.cursor/environment.json` runs `.cursor/install.sh`, a no-op that
  exits 0. Do not replace it with a Node, Python, or package-manager
  stack.
- Do not add `start`, `terminals`, ports, or a Dockerfile unless this
  repo becomes a real application.
- There is no local app, test suite, or development server to run.
