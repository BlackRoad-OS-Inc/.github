# BlackRoad OS — Agents

> Agent scaffold, routing, and autonomous workflow documentation.

## @blackroad-agents

The `@blackroad-agents` command triggers a **deca-layered scaffold** that governs the lifecycle of every task in the BlackRoad ecosystem — from initial review through deployment and content publishing.

### Scaffold Steps

1. **Initial Reviewer** — Lucidia Core (Layer 6) reviews the request for clarity, security compliance, and resource availability. Generates a preliminary execution plan.
2. **Task → Organization** — Route to one of the [fifteen BlackRoad organizations](organizations.json) based on functional domain.
3. **Task → Team** — Distribute within the selected organization. Pauses for human-in-the-loop (HITL) approval on high-risk operations.
4. **Task → Project** — Record in a GitHub Project board. Sync metadata (Request ID, timeline) with Salesforce.
5. **Task → Agent** — Assign a specialized agent using the **Planner-Executor-Reflector** design pattern (e.g. `fastapi-coder-agent`, `doctl-infrastructure-agent`).
6. **Task → Repository** — Create a branch in the target repo following **GitHub Flow**.
7. **Task → Device** — Route to physical hardware for firmware deployment or Droplet rebuild.
8. **Task → Drive** — Distribute artifacts to Google Drive via Service Account (GSA).
9. **Task → Cloudflare** — Execute DNS or Tunnel configuration changes.
10. **Task → Website Editor** — Update the presentation layer via AI-driven editor or headless CMS.

See **[scaffold.json](scaffold.json)** for the machine-readable definition.

## @BlackRoadBot

The `@BlackRoadBot` routing matrix responds to natural-language mentions on GitHub issues and PRs. It identifies the target platform from intent and dispatches accordingly:

| Platform | Integration |
|---|---|
| Salesforce | Apex middleware → Case/Task creation; Data Cloud telemetry via webhooks |
| Hugging Face | Programmatic inference endpoints for high-compute tasks |
| Ollama | Local models exposed via Cloudflare Tunnel |
| DigitalOcean | Droplet management via `doctl` in GitHub Actions |
| Railway | Ephemeral test environments for feature branches |

## Agent Fleet

The current fleet is defined in **[agent.json](agent.json)**:

| Agent | Role |
|---|---|
| CECE | Primary orchestrator |
| octavia-pi5 | Raspberry Pi 5 fleet node |
| aria-pi4 | Raspberry Pi 4 fleet node |
| cecilia | General-purpose agent |
| gematria-do | DigitalOcean-hosted agent |
| lucidia-pi5 | Memory-layer Pi 5 node |

## Error Handling

If a task fails at any scaffold layer, the system:

1. Creates a GitHub Issue with detailed logs from Layer 6 (Lucidia Core).
2. A **Reflect and Retry** plugin assesses the failure.
3. Resolves by adjusting agent prompts or switching the inference model.

Every request is tracked via a unique **Request ID** for server-side tracing.

## Rate-Limit Mitigation

| Provider | Mitigation |
|---|---|
| GitHub Copilot | Redirect to local Raspberry Pi LiteLLM proxy |
| Hugging Face Hub | Rotate HF_TOKEN or use authenticated SSH keys |
| Google Drive | Shared Drives with GSA Content Manager role |
| DigitalOcean API | Queue tasks via Layer 7 Orchestration |
| Salesforce API | Batch updates via Data Cloud Streaming Transforms |

See **[infrastructure.json](infrastructure.json)** for full hardware specs and mitigation details.

---

*© BlackRoad OS, Inc. All rights reserved.*
