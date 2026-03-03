# Changelog

All notable changes to the BlackRoad OS, Inc. org-wide GitHub configuration are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [Unreleased]

### Added
- `dependabot.yml` — weekly automated updates for GitHub Actions dependencies
- `ISSUE_TEMPLATE/config.yml` — structured template chooser; blank issues disabled; links to Discussions, security email, and status page
- `CHANGELOG.md` — this file (referenced in `CONTRIBUTING.md`)

### Changed
- `org-ci.yml` — added `permissions` (least-privilege), `concurrency` (cancel duplicate runs), `timeout-minutes: 10`; expanded secret-scanning patterns to include JSON/YAML files; added JSON and YAML validation steps
- `blackroad-agent.yml` — added `permissions`, `concurrency`, and `timeout-minutes: 10`
- `stale.yml` — added explicit `permissions` (`issues: write`, `pull-requests: write`) and `timeout-minutes: 10`

---

## [0.1.0] — 2026-02-23

### Added
- `profile/README.md` — org profile
- `PULL_REQUEST_TEMPLATE.md` — standardized PR checklist
- `ISSUE_TEMPLATE/bug_report.yml` — structured bug reports
- `ISSUE_TEMPLATE/feature_request.yml` — structured feature requests
- `ISSUE_TEMPLATE/task.yml` — internal engineering task template
- `workflows/org-ci.yml` — org-wide CI: secret scanning, AGENTS.md check
- `workflows/blackroad-agent.yml` — shared agent identity workflow
- `workflows/stale.yml` — stale issue/PR automation
- `CODEOWNERS` — default reviewers
- `CONTRIBUTING.md` — contribution guidelines
- `SECURITY.md` — vulnerability reporting policy
- `FUNDING.yml` — sponsorship configuration
- `agent.json` — org agent identity config
- `LICENSE` — BlackRoad OS, Inc. Proprietary License

© BlackRoad OS, Inc. All rights reserved.
