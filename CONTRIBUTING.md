# Contributing to BlackRoad OS, Inc.

> All repositories in this org are proprietary to BlackRoad OS, Inc.
> Contributions require signing our CLA.

## Getting Started

1. Fork the relevant repo
2. Create a branch: `git checkout -b feat/your-feature`
3. Make your changes following the [Code Standards](#code-standards)
4. Run tests locally
5. Open a PR using the template

## Code Standards

| Language | Formatter | Linter |
|----------|-----------|--------|
| TypeScript/JS | Prettier | ESLint |
| Python | Black | Ruff |
| Go | gofmt | golangci-lint |
| Shell | shfmt | shellcheck |

## Commit Messages

Follow [Conventional Commits](https://conventionalcommits.org):

```
feat: add streaming support to SDK
fix: handle null agent response in gateway
docs: update CLI installation guide
chore: bump dependencies
```

## Branch Naming

- `feat/description` — new features
- `fix/issue-number` — bug fixes
- `docs/section` — documentation updates
- `chore/task` — maintenance

## Pull Request Process

1. Ensure CI passes
2. Update `CHANGELOG.md`
3. Request review from a CODEOWNER
4. Squash merge after approval

## Questions?

Open a [Discussion](https://github.com/orgs/BlackRoad-OS-Inc/discussions) or email dev@blackroad.ai.

© BlackRoad OS, Inc. All rights reserved.
