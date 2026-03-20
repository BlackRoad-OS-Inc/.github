# BlackRoad OS, Inc.

**Proprietary Software. Delaware C-Corp. Founded November 17, 2025.**

---

## What is BlackRoad OS?

BlackRoad OS is a complete, sovereign technology stack — infrastructure, AI, applications, and services — owned and operated on hardware we control. We exist because the modern tech stack is a dependency chain where every link is a toll booth owned by someone who can raise prices, change terms, or shut you down.

We built the replacement.

## The Stack

| Layer | What We Built | What It Replaces |
|-------|--------------|-----------------|
| Compute | 5 Raspberry Pi edge nodes + 2 cloud servers | AWS/GCP/Azure |
| AI | 52 TOPS local inference (2x Hailo-8 + Ollama) | OpenAI / Anthropic API |
| Git | RoadCode (Gitea, 239+ repos) | GitHub |
| DNS | PowerDNS on our hardware | Cloudflare DNS |
| TLS | Caddy + Let's Encrypt | Cloudflare proxy |
| Object Storage | MinIO (S3-compatible) | AWS S3 |
| Database | PostgreSQL on 3 nodes | Cloud databases |
| VPN | WireGuard mesh | Tailscale |
| Workers | 15 self-hosted workers | Cloudflare Workers |
| Chat | RoundTrip (sovereign) | Slack |
| Auth | JWT + PBKDF2, self-hosted | Auth0 / Clerk |
| Billing | RoadPay (Stripe as card charger only) | Stripe Billing |

## Products

| Product | What It Does |
|---------|-------------|
| [RoadPay](https://pay.blackroad.io) | Billing & subscriptions |
| [RoadSearch](https://search.blackroad.io) | FTS5 search + AI answers |
| [Prism Console](https://prism.blackroad.io) | Operations dashboard |
| [BlackRoad Auth](https://auth.blackroad.io) | JWT authentication |
| [Squad Webhook](https://github.com/BlackRoad-OS-Inc/squad-webhook) | AI agents on GitHub |

## Organizations

| Org | Domain |
|-----|--------|
| [BlackRoad-OS](https://github.com/BlackRoad-OS) | Core platform |
| [BlackRoad-AI](https://github.com/BlackRoad-AI) | AI & inference |
| [BlackRoad-Cloud](https://github.com/BlackRoad-Cloud) | Infrastructure |
| [BlackRoad-Security](https://github.com/BlackRoad-Security) | Security |
| [BlackRoad-Labs](https://github.com/BlackRoad-Labs) | Research |
| [BlackRoad-Studio](https://github.com/BlackRoad-Studio) | Creative tools |
| [BlackRoad-Interactive](https://github.com/BlackRoad-Interactive) | Gaming & 3D |
| [BlackRoad-Media](https://github.com/BlackRoad-Media) | Content |
| [BlackRoad-Education](https://github.com/BlackRoad-Education) | Learning |
| [BlackRoad-Hardware](https://github.com/BlackRoad-Hardware) | IoT & devices |
| [BlackRoad-Gov](https://github.com/BlackRoad-Gov) | Governance |
| [BlackRoad-Foundation](https://github.com/BlackRoad-Foundation) | Community |
| [BlackRoad-Ventures](https://github.com/BlackRoad-Ventures) | Investment |
| [BlackRoad-Archive](https://github.com/BlackRoad-Archive) | Preservation |
| [Blackbox-Enterprises](https://github.com/Blackbox-Enterprises) | Automation |

## License

All software in this organization is **proprietary** to BlackRoad OS, Inc. Source code is publicly visible for transparency, security review, and education. Commercial use, forking, and redistribution are prohibited without written authorization.

---

**BlackRoad OS — Pave Tomorrow.**
