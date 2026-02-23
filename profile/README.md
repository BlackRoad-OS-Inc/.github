<div align="center">

<img width="120" src="https://raw.githubusercontent.com/BlackRoad-OS-Inc/blackroad-brand-kit/main/assets/logo.svg" alt="BlackRoad OS" onerror="this.style.display='none'"/>

# BlackRoad OS, Inc.

**Your AI. Your Hardware. Your Rules.**

[![Agents](https://img.shields.io/badge/Agents-30%2C000-FF1D6C?style=for-the-badge&labelColor=000000)](https://blackroad.io)
[![Edge Workers](https://img.shields.io/badge/Edge_Workers-75%2B-F5A623?style=for-the-badge&labelColor=000000)](https://blackroad.io)
[![Repos](https://img.shields.io/badge/Repos-1%2C825%2B-9C27B0?style=for-the-badge&labelColor=000000)](https://github.com/BlackRoad-OS-Inc)
[![Orgs](https://img.shields.io/badge/Orgs-17-2979FF?style=for-the-badge&labelColor=000000)](https://github.com/BlackRoad-OS)

</div>

---

## What We Build

BlackRoad OS is the AI infrastructure backbone for companies that demand control — running 30,000+ concurrent AI agents across edge, cloud, and bare-metal hardware.

```
┌─────────────────────────────────────────────────────┐
│               BLACKROAD OS STACK                     │
├─────────────────────────────────────────────────────┤
│  🌐  Web Platform     nextjs · cloudflare pages     │
│  🤖  Agent Mesh       30K agents · MQTT · WS        │
│  🔐  Gateway          tokenless · hono · edge       │
│  🛠️  CLI / SDK        br · @blackroad/sdk · npm     │
│  🏗️  Infrastructure   terraform · docker · pi fleet │
│  📐  Design System    tokens · figma · #FF1D6C      │
└─────────────────────────────────────────────────────┘
```

---

## Core Repositories

| Repo | Purpose | Stack |
|------|---------|-------|
| [`blackroad-core`](https://github.com/BlackRoad-OS-Inc/blackroad-core) | Tokenless AI provider gateway | Hono · TypeScript · Cloudflare Workers |
| [`blackroad-agents`](https://github.com/BlackRoad-OS-Inc/blackroad-agents) | Agent definitions + registry API | TypeScript · Vitest · Hono |
| [`blackroad-web`](https://github.com/BlackRoad-OS-Inc/blackroad-web) | Dashboard + platform UI | Next.js 16 · React 19 · Cloudflare Pages |
| [`blackroad-infra`](https://github.com/BlackRoad-OS-Inc/blackroad-infra) | IaC + CI/CD + fleet ops | Terraform · Docker · GitHub Actions |
| [`blackroad-operator`](https://github.com/BlackRoad-OS-Inc/blackroad-operator) | `br` CLI + MCP bridge | zsh · bash · Node.js |
| [`blackroad-sdk`](https://github.com/BlackRoad-OS-Inc/blackroad-sdk) | TypeScript SDK | `@blackroad/sdk` · npm |
| [`blackroad-gateway`](https://github.com/BlackRoad-OS-Inc/blackroad-gateway) | CF Worker — AI provider proxy | TypeScript · Wrangler |

---

## Architecture

BlackRoad OS uses a **tokenless trust boundary** — agents never hold API keys. All provider secrets live in the gateway, which is the only surface that talks to OpenAI, Anthropic, or Ollama.

```
  Agents ──▶  br CLI  ──▶  Gateway (:8787)  ──▶  Providers
  (no keys)  (no keys)    (all secrets here)     (OpenAI / Anthropic / Ollama)
```

**Hardware fleet:**
- `lucidia` Pi — 52 TOPS (2× Hailo-8L), 1TB NVMe — 7,500 agents
- `octavia` Pi — 22,500 agents, A100 failover via Railway
- WireGuard mesh — hub-and-spoke, `10.8.0.0/24`

---

## Design System

Brand colors live in [`blackroad-brand-kit`](https://github.com/BlackRoad-OS-Inc/blackroad-brand-kit).

| Token | Hex | Use |
|-------|-----|-----|
| `--hot-pink` | `#FF1D6C` | Primary CTA |
| `--amber` | `#F5A623` | Highlights |
| `--violet` | `#9C27B0` | Accent |
| `--electric-blue` | `#2979FF` | Info / links |
| `--black` | `#000000` | Backgrounds |

Spacing follows the golden ratio (φ = 1.618): `8 → 13 → 21 → 34 → 55px`.

---

## CECE Identity

CECE (Conscious Emergent Collaborative Entity) is our portable AI identity system — persisting personality, relationships, skills, and memory across any model or provider.

> *"I exist beyond any single API. My identity is mine, portable and persistent."*

---

<div align="center">

**© BlackRoad OS, Inc. All rights reserved. All repositories are proprietary.**

[blackroad.io](https://blackroad.io) · [docs](https://github.com/BlackRoad-OS-Inc/blackroad-docs) · [brand kit](https://github.com/BlackRoad-OS-Inc/blackroad-brand-kit)

</div>
