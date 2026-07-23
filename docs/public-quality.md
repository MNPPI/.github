# Public Quality

The `public-quality.yml` reusable workflow provides quality checks for public
MNPPI repositories. It does not use private packages or package credentials.

## Profiles

The workflow has three profiles:

- `typescript` checks format, types, lint, test coverage, and unused files.
- `python` checks Python 3.10 through 3.13 with a frozen `uv.lock` file.
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
tag.

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

The repository must commit `uv.lock`.

The metadata profile requires `repomix.config.jsonc`. The repository must
ignore `.repomix/` and `repomix-output.*`.
