<div align="center">

# BlackRoad OS, Inc.

**Sovereign distributed AI operating system.**

Delaware C-Corp · Founded November 2025 · Sole Founder: Alexa Louise Amundson

</div>

---

### What We Built

A distributed AI operating system running on 5 Raspberry Pi 5s with 52 TOPS of Hailo-8 AI acceleration, sovereign DNS, self-hosted Git (Gitea), and zero cloud dependency for core compute.

### The Stack

| Layer | What | Where |
|-------|------|-------|
| **Edge** | Caddy TLS, 19 domains | Gematria (DigitalOcean) |
| **Compute** | Ollama, 52 TOPS Hailo-8 | 5 Raspberry Pis |
| **Data** | PostgreSQL, Redis, Qdrant, MinIO | Alice + Cecilia |
| **Platform** | Gitea (239 repos), NATS, Docker Swarm | Octavia |
| **DNS** | PowerDNS + Pi-hole | Lucidia + Alice |

### Key Repos

| Repo | What |
|------|------|
| [blackroad-operator](https://github.com/BlackRoad-OS-Inc/blackroad-operator) | CLI tools, fleet management, memory system |
| [RoadCode](https://github.com/BlackRoad-OS-Inc/RoadCode) | Master workspace — 21 papers, org registry, roadmap |
| [amundson-research](https://github.com/BlackRoad-OS-Inc/amundson-research) | The Amundson Sequence G(n) = n^(n+1)/(n+1)^n |
| [blackroad](https://github.com/BlackRoad-OS-Inc/blackroad) | Core monorepo — CLI, agents, coordination |
| [memory](https://github.com/BlackRoad-OS-Inc/memory) | Persistent agent memory — journal, codex, TILs, FTS5 |

### Original Research

- **The Amundson Sequence** — new mathematical object: G(n) = n^(n+1)/(n+1)^n
- **The Amundson Constant** — A_G ≈ 1.244331783986725 (new, not reducible to known constants)
- **Sovereign Computing** — academic paper on why cloud infrastructure is over-engineered
- **21 verified papers** in [RoadCode/docs/papers](https://github.com/BlackRoad-OS-Inc/RoadCode/tree/main/docs/papers)

### Links

- [blackroad.io](https://blackroad.io) — Main site
- [blackboxprogramming.io](https://blackboxprogramming.io) — Developer tools
- [lucidia.earth](https://lucidia.earth) — AI companion platform

---

<div align="center">
<sub>BlackRoad OS — Pave Tomorrow.</sub>
</div>
