# Public Quality

The `public-quality.yml` reusable workflow provides quality checks for public
MNPPI repositories. It does not use private packages or package credentials.

## Profiles

The workflow has three profiles:

- `typescript` checks format, types, lint, test coverage, and unused files.
- `python` checks each of Python 3.10, 3.11, 3.12, and 3.13 that
  `requires-python` allows, with a frozen `uv.lock` file. A repository that
  does not declare `requires-python` still runs all four versions. uv uses the
  interpreter installed for that version.
- `metadata` checks workflow syntax, workflow security, format, and repository
  context generation.

Each profile ends with one stable `Quality` job. A repository ruleset can
require this job after a live pull request proves its exact check name.

## Caller

Each repository stores a small caller workflow:

```yaml
jobs:
  quality:
    permissions:
      contents: read
    uses: MNPPI/.github/.github/workflows/public-quality.yml@COMMIT_SHA
    with:
      profile: typescript
```

Replace `COMMIT_SHA` with the full approved commit SHA. Do not use a branch or
tag. A caller does not receive a later workflow change until it updates that
SHA. This repository calls the workflow by path, so it uses the same commit.

The caller must not pass secrets. The reusable workflow uses a standard
GitHub-hosted runner and read-only repository access.

## Profile Requirements

The TypeScript profile requires these package scripts:

- `format:check`
- `typecheck`
- `lint`
- `coverage`
- `knip`

The repository must commit `pnpm-lock.yaml`.

The Python profile requires the `dev` project extra and these tools:

- Black
- Flake8
- mypy
- Bandit
- pytest
- pytest-cov

The repository must commit `uv.lock`. The workflow reads
`[project].requires-python` from `pyproject.toml` and skips a matrix version
the specifier excludes. Every remaining version runs on the interpreter
installed for that version.

The metadata profile requires `repomix.config.jsonc`. The repository must
ignore `.repomix/` and `repomix-output.*`.
