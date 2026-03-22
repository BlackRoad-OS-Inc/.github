<div align="center">

# BlackRoad OS, Inc.

**Sovereign AI infrastructure on Raspberry Pi. Your AI. Your hardware. Your rules.**

Delaware C-Corp · Founded November 2025 · Founder: Alexa Louise Amundson

[Try Search](https://search.blackroad.io) · [Try Chat](https://chat.blackroad.io) · [BackRoad Social](https://social.blackroad.io) · [Website](https://blackroad.io) · [Blog](https://blackroad.io/blog)

</div>

---

### Try It Now

| Product | What It Does | Link |
|---------|-------------|------|
| **Search** | Full-text search across the BlackRoad ecosystem | [search.blackroad.io](https://search.blackroad.io) |
| **Chat** | AI chat powered by Workers AI — no signup needed | [chat.blackroad.io](https://chat.blackroad.io) |
| **RoundTrip** | 200 AI agents you can talk to, debate, and coordinate | [roundtrip.blackroad.io](https://roundtrip.blackroad.io) |
| **Canvas Studio** | Browser-based drawing + AI | [canvas.blackroad.io](https://canvas.blackroad.io) |
| **Cadence** | 13-key synthesizer in the browser | [cadence.blackroad.io](https://cadence.blackroad.io) |

### Products

| Product | Description | Link |
|---------|-------------|------|
| **BlackRoad OS** | Self-hosted platform replacing cloud services | [blackroad.io](https://blackroad.io) |
| **Lucidia** | AI companion with persistent memory | [blackroadai.com](https://blackroadai.com) |
| **RoadPay** | Billing system — Stripe integration, 4 subscription plans | [pay.blackroad.io](https://pay.blackroad.io) |
| **RoadWork** | AI tutoring platform, free for K-12 | [work.blackroad.io](https://work.blackroad.io) |
| **RoadChain** | Layer-1 blockchain from scratch in Python | [roadchain.io](https://roadchain.io) |
| **RoadCoin** | Cryptocurrency and micro-payments | [roadcoin.io](https://roadcoin.io) |
| **Amundson Framework** | G(n) = n^(n+1)/(n+1)^n — new mathematical constant | [blackroadquantum.com](https://blackroadquantum.com) |

### Infrastructure

5 Raspberry Pis + 2 cloud nodes. $63/month total.

| Layer | Self-Hosted Service | Replaces |
|-------|-------------------|----------|
| Edge + TLS | Caddy (18 domains, Let's Encrypt) | Cloudflare |
| AI Inference | Ollama on 4 nodes + 2x Hailo-8 (52 TOPS) | OpenAI |
| Git Hosting | Gitea (239 repos, 8 orgs) | GitHub |
| Object Storage | MinIO | S3 / R2 |
| DNS | PowerDNS | Cloudflare DNS |
| Database | PostgreSQL on 3 nodes | Managed DB |
| Search | Qdrant + FTS5 | Algolia |
| VPN | WireGuard mesh (all nodes) | Tailscale |
| Chat/Coordination | RoundTrip (200 agents) | Slack |

### Key Repos

| Repo | What |
|------|------|
| [blackroad-operator](https://github.com/BlackRoad-OS-Inc/blackroad-operator) | CLI, fleet management, memory system, 400+ scripts |
| [blackroad](https://github.com/BlackRoad-OS-Inc/blackroad) | Monorepo — agents, CarPool coordination, Workers |
| [amundson-constant](https://github.com/BlackRoad-OS-Inc/amundson-constant) | A_G ≈ 1.2443 computed to 10M digits, 50+ identities |
| [amundson-research](https://github.com/BlackRoad-OS-Inc/amundson-research) | Papers, proofs, G(n) framework |
| [road-search](https://github.com/BlackRoad-OS-Inc/road-search) | FTS5 search engine with AI-powered answers |
| [openclaw](https://github.com/BlackRoad-OS-Inc/openclaw) | Personal AI assistant (fork of OpenClaw) |
| [roadc](https://github.com/BlackRoad-OS-Inc/roadc) | Custom programming language |
| [memory](https://github.com/BlackRoad-OS-Inc/memory) | Persistent agent memory — journal, codex, TILs |

### Research

**The Amundson Framework** — G(n) = n^(n+1)/(n+1)^n

A single function connecting combinatorics, analysis, and number theory. 50+ verified identities. The constant A_G = Σ G(n)/n! ≈ 1.244331783986725 computed to 10 million digits. Crossover point at n ≈ 2.293166 separates regimes where n^n dominates vs (n+1)^n.

[Read the paper →](https://github.com/BlackRoad-OS-Inc/amundson-constant/blob/main/FRAMEWORK.md)

### Real Numbers

- 93 public repos in this org (65 original + 28 sovereign forks)
- 239 repos on self-hosted Gitea
- 18 root domains + 14 product subdomains — all live
- 200 AI agents across 21 groups
- 5 Raspberry Pis + 2 cloud nodes, 2x Hailo-8 (52 TOPS)
- $63/month infrastructure
- 0 external users — [be the first](https://search.blackroad.io)

---

<div align="center">
<sub>BlackRoad OS, Inc. — Remember the Road. Pave Tomorrow.</sub>
</div>
