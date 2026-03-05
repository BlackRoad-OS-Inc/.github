# CLAUDE.md — BlackRoad OS, Inc. Organization Repository

> This file provides context for AI assistants working in this repository.

## Repository Purpose

This is the **`.github` organization-level repository** for [BlackRoad OS, Inc.](https://blackroad.io). It defines default community health files, GitHub Actions workflows, issue/PR templates, and org metadata that apply across all repositories in the `BlackRoad-OS-Inc` GitHub organization (1,825+ repos, 17 orgs).

This repo does **not** contain application source code. It is a governance and configuration repository.

## Directory Structure

```
.github/
├── ISSUE_TEMPLATE/
│   ├── bug_report.yml        # Bug report form (component, severity, repro steps)
│   ├── feature_request.yml   # Feature request form (motivation, category)
│   └── task.yml              # Internal engineering task template
├── PULL_REQUEST_TEMPLATE.md  # Default PR template for all org repos
├── agent.json                # Repo-level agent metadata
└── workflows/
    ├── blackroad-agent.yml   # Shared agent CI — loads agent identity per branch
    ├── org-ci.yml            # Org-wide CI — secrets scan, AGENTS.md check
    └── stale.yml             # Auto-stale issues/PRs after 30 days
profile/
└── README.md                 # GitHub org profile page (public-facing)
agent.json                    # Org-level agent config (CECE agent, Pi fleet)
CODEOWNERS                    # @blackboxprogramming owns all files
CONTRIBUTING.md               # Contribution guide, code standards, branch naming
FUNDING.md                    # Sponsorship info ($0/mo self-hosted model)
FUNDING.yml                   # GitHub Sponsors + custom funding links
LICENSE                       # Proprietary license (BlackRoad OS, Inc.)
SECURITY.md                   # Vulnerability reporting policy (security@blackroad.ai)
```

## Key Conventions

### Commit Messages
Follow [Conventional Commits](https://conventionalcommits.org):
- `feat:` — new features
- `fix:` — bug fixes
- `docs:` — documentation updates
- `chore:` — maintenance tasks

### Branch Naming
- `feat/description` — new features
- `fix/issue-number` — bug fixes
- `docs/section` — documentation
- `chore/task` — maintenance

### Code Standards
| Language       | Formatter | Linter         |
|----------------|-----------|----------------|
| TypeScript/JS  | Prettier  | ESLint         |
| Python         | Black     | Ruff           |
| Go             | gofmt     | golangci-lint  |
| Shell          | shfmt     | shellcheck     |

### PR Process
1. CI must pass (secrets scan, validation)
2. Update `CHANGELOG.md` if applicable
3. Request review from CODEOWNER (`@blackboxprogramming`)
4. Squash merge after approval

## Workflows

### `blackroad-agent.yml`
Runs on `self-hosted, pi` runners. Loads agent identity from the central `blackroad` repo based on branch name, then emits a health ping. Triggers on push to `main`/`dev`/`master` and on PRs.

### `org-ci.yml`
Runs on `ubuntu-latest`. Scans for hardcoded secrets (`sk_live`, `ghp_`, `AKIA`, private keys) and checks for `AGENTS.md`. Triggers on push to `main`/`master`/`develop` and PRs to `main`/`master`.

### `stale.yml`
Marks issues/PRs stale after 30 days of inactivity, closes after 7 more days. Runs weekly on Monday at 9 AM UTC.

## Agent Configuration

The org uses a self-hosted AI agent named **CECE** (defined in root `agent.json`):
- **Fleet**: `octavia-pi5`, `aria-pi4`, `cecilia`, `gematria-do`, `lucidia-pi5`
- **Runners**: `blackroad-fleet` (self-hosted Pi hardware)
- **Gateway**: `http://octavia.local:8787`
- **Cost**: $0 (models run on Pi fleet via Hailo-8 + Ollama)

## Important Notes for AI Assistants

- **Proprietary codebase**: All code is proprietary to BlackRoad OS, Inc. Do not suggest open-sourcing or changing the license.
- **No secrets in code**: The `org-ci.yml` workflow will fail the build if secrets patterns are detected. Never commit API keys, tokens, or private keys.
- **CODEOWNERS**: `@blackboxprogramming` is the default reviewer for all files. All PRs require their review.
- **Security vulnerabilities**: Report to `security@blackroad.ai`, never open public issues.
- **AGENTS.md**: Many repos in the org are expected to have an `AGENTS.md` file describing agent capabilities. The CI checks for its presence.
- **Self-hosted infrastructure**: The platform runs on Raspberry Pi fleets and edge hardware. Be aware that workflows may target `self-hosted, pi` runners.
- **File changes in this repo propagate org-wide**: Templates, workflows, and community health files here are defaults for all repos in the org. Edit with care.
