# .github

Velumbra's defaults for every repo (profile, `CONTRIBUTING.md`, `SECURITY.md`, issue and pull request forms), the shared workflows and the Renovate presets (`renovate/`).

| Workflow           | Does                                                                         |
| ------------------ | ---------------------------------------------------------------------------- |
| `node.yml`         | Lint, format, typecheck, tests; checks the pull request title                |
| `release.yml`      | semantic-release: tag, GitHub release, optionally publish to GitHub Packages |
| `docker-image.yml` | Image to `ghcr.io`, tagged with the release                                  |

A repo calls them from its `.github/workflows/ci.yml`, pinned to a release; Actions → New workflow offers it ready-made (`workflow-templates/`, module or app):

```yaml
jobs:
  check:
    uses: velumbra/.github/.github/workflows/node.yml@v0.1.0
    secrets: inherit
```

Inputs are described in each workflow. Repos need a `PACKAGES_TOKEN` secret (classic token, `read:packages`).
