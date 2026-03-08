## 100monkeys

### *Stop building. Start growing.*

**The autonomous AI agent runtime built on biology's 3.5-billion-year head start.**

[![Docs](https://img.shields.io/badge/docs-docs.100monkeys.ai-00e5ff?style=flat-square&logo=gitbook&logoColor=white)](https://docs.100monkeys.ai)
[![Discord](https://img.shields.io/badge/Discord-Join%20the%20Troop-5865F2?style=flat-square&logo=discord&logoColor=white)](https://discord.100monkeys.ai)
[![Community](https://img.shields.io/badge/Community-troop.100monkeys.ai-ff2d78?style=flat-square&logo=discourse&logoColor=white)](https://troop.100monkeys.ai)
[![Cloud Waitlist](https://img.shields.io/badge/Cloud-Q2%202026%20Waitlist-ffd700?style=flat-square&logo=rocket&logoColor=black)](https://100monkeys.ai)
[![License](https://img.shields.io/badge/License-AGPL--3.0-brightgreen?style=flat-square)](https://github.com/100monkeys-ai/aegis-orchestrator/blob/main/LICENSE)
[![Self-Host](https://img.shields.io/badge/Self--Host-Available%20Now-00e5ff?style=flat-square&logo=docker&logoColor=white)](https://docs.100monkeys.ai/self-hosting)

---

## The Problem

> *An open-source agentic framework reached 180,000 GitHub stars. Forbes called it "a security nightmare." Cisco agreed. 1,800+ installations were exposed to the public internet with no authentication. Agents ran with root access, live credit cards, and unlimited filesystem permissions. A single bad prompt could delete the database.*

The market proved something undeniable: **developers desperately want autonomous AI agents.**

But every framework built so far handed the AI the keys to the kingdom and *hoped for the best*.

That's not an engineering problem. That's a **physics problem** — and physics problems require physics solutions.

---

## The Insight

> *"Biology solved the problem of autonomous agents 3.5 billion years ago. We're just implementing the spec."*

When life needed to run complex, unpredictable chemical experiments inside a cell, it didn't build a better experiment. It built a **membrane** — an immutable physical boundary that lets the nucleus do anything it wants, completely unable to destroy the environment outside it.

The cell can fail a thousand times. The organism survives.

We called this problem **The Infinite Sandbox Paradox**:

> *"If I lock the agent down, it can't do the job. If I let it loose, it might delete the database."*

**AEGIS is the membrane. 100monkeys is the nucleus. The paradox is solved.**

---

## The 100monkeys Algorithm

Traditional AI pipelines treat model output as a **final answer**. We treat it as a **first attempt**.

```markdown
┌─────────────────────────────────────────────────────────────────────────────┐
│                      THE 100MONKEYS LOOP                                    │
│                                                                             │
│   INTENT ──► GENERATE ──► EXECUTE ──► EVALUATE ──► REFINE ──► REMEMBER      │
│                 │              │           │           │          │         │
│                 │         Firecracker      │       Inject      Cortex       │
│                 │         Micro-VM         │       error       stores       │
│                 │         (125ms boot)     │       context     pattern      │
│                 │                          │                                │
│                 │        ❌ Iteration 1: ModuleNotFoundError                │
│                 │        🔄 Iteration 2: Installing missing dependency...   │
│                 │        ❌ Iteration 2: TypeError in line 47               │
│                 │        🔄 Iteration 3: Fixing type annotation...          │
│                 │        ✅ Iteration 3: All validators passed              │
│                 │                                                           │
│             LLM output is a                                                 │
│             candidate, not                                                  │
│             a commitment.                                                   │
└─────────────────────────────────────────────────────────────────────────────┘
```

**Validation is not binary.** We score outputs on a gradient (0.0 → 1.0) across five validator layers — System, Format, Schema, Script, and Semantic — feeding precise error context back into each iteration. The loop doesn't retry blindly. It learns exactly why it failed and attacks the root cause.

**The Core Claim:**
> *"We don't need the model to be perfect. We need the system to be rigorous."*

A cheap local model (`llama3.1`) in a rigorous loop outperforms GPT-4 on a single shot. **Trade compute for IQ.**

```markdown
Success Rate Evolution:
  Week 1:   60% ██████░░░░
  Month 1:  85% ████████░░
  Month 3:  95% █████████░   ← the Cortex effect
```

---

## The Biological Architecture

AEGIS maps one-to-one to biology's most successful design patterns:

| 🧬 Biological Concept | ⚙️ AEGIS Implementation | What It Does |
| --- | --- | --- |
| **The Membrane** | AEGIS Orchestrator (Rust + Firecracker) | Immutable, kernel-level physics. Enforces security without trusting the contents. |
| **The Nucleus** | 100monkeys Loop Engine | Autonomous mutation and refinement. Runs freely inside — the membrane contains any explosion. |
| **The Synapse** | Zaru (myzaru.com) | The nerve that connects human intent to the biological process. Natural language in, evolved agent out. |

**Traditional software is crystalline: rigid, fragile, breaks when hit.
AEGIS is biological: fluid, resilient, and stronger after every failure.**

---

## The Security Guarantee

```markdown
You do not trust the AI to be "good."
You do not trust the AI to be "smart."
You trust AEGIS to be impenetrable.
```

Security is moved **out of the probabilistic layer** (the LLM) and **into the deterministic layer** (the orchestrator). The AI cannot violate its policy because the policy is enforced at the kernel level — not in a system prompt.

**The Stack:**

- 🦀 **Rust** — Memory-safe runtime. No footguns in the enforcement layer.
- 🔥 **Firecracker Micro-VMs** — AWS's production-grade isolation. `rm -rf /` is a localized event.
- 🔏 **SMCP** — Secure Model Context Protocol. Every tool call is cryptographically signed with an ephemeral Ed25519 key, wrapped in a security envelope, and evaluated against Cedar policies before execution.
- 🔑 **OpenBao** — Secrets never touch agents. The orchestrator holds all credentials behind the Keymaster Pattern.
- 🚪 **AegisFSAL** — Transport-agnostic File System Abstraction Layer. Every file operation passes through the orchestrator's security gateway with per-operation authorization, path traversal prevention, and a forensic audit trail.
- 🏛️ **Keycloak** — Single trusted OIDC identity issuer across every surface: UI, API, gRPC, M2M.

**The result:** An Enterprise CTO can sleep at night while autonomous agents run on their infrastructure — because trust is not required.

---

## The Ecosystem

### 🌐 Zaru — [myzaru.com](https://myzaru.com)

The consumer AI product. A LibreChat front-end wired directly into the AEGIS execution engine.

Describe what you want. Zaru generates an agent manifest, runs the 100monkeys loop, and shows you the **Glass Laboratory** — every iteration attempt, every failure, every refinement, live.

> *"We trust things we see overcome adversity."*

Tiers: Free · Pro · Enterprise

---

### 🎛️ Control Plane — AEGIS Operator Dashboard

Three instruments for operators building on AEGIS:

- **The Architect** — Turn natural language intent into production-ready agent YAML manifests
- **The Synapse** — Watch the 100monkeys loop execute in real time
- **The Cortex Explorer** — Browse the living pattern graph your agents are building

---

### 🐒 Monkey Troop — [troop.100monkeys.ai](https://troop.100monkeys.ai) · MIT

Our gift to the community.

A FOSS P2P decentralized AI compute grid. Donate your idle GPU time. Earn **Banana credits** based on hardware performance. Redeem for inference against an OpenAI-compatible API.

Drop-in replacement for any `openai` client. Use Llama. Pay $0.

---

## Repository Map

### 🔬 Core Platform

| Repository | What It Is | Language |
| --- | --- | --- |
| [**aegis-orchestrator**](https://github.com/100monkeys-ai/aegis-orchestrator) | The beating heart. Agent lifecycle, execution engine, 100monkeys loop, Firecracker/Docker runtimes, SMCP gateway, gRPC API, CLI. | ![Rust](https://img.shields.io/badge/-Rust-000?logo=rust) |
| [**aegis-smcp-gateway**](https://github.com/100monkeys-ai/aegis-smcp-gateway) | Standalone SMCP tooling gateway for macro-tools (`ToolWorkflow`) and secure external tool invocation. | ![Rust](https://img.shields.io/badge/-Rust-000?logo=rust) |
| [**secure-model-context-protocol**](https://github.com/100monkeys-ai/secure-model-context-protocol) | SMCP specification and SDK. Cryptographically signed MCP envelopes with Cedar policy evaluation. | ![Mixed](https://img.shields.io/badge/-Spec-lightgrey) |
| [**aegis-proto**](https://github.com/100monkeys-ai/aegis-proto) | Protobuf definitions for the AEGIS gRPC API surface. | ![Proto](https://img.shields.io/badge/-Proto-blue) |
| [**aegis-temporal-worker**](https://github.com/100monkeys-ai/aegis-temporal-worker) | Temporal.io durable workflow worker for long-running, fault-tolerant executions. | ![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) |

### 🖥️ Interfaces & SDKs

| Repository | What It Is | Language |
| --- | --- | --- |
| [**aegis-sdk-python**](https://github.com/100monkeys-ai/aegis-sdk-python) | Python client SDK. Type-safe manifest construction, execution watching. | ![Python](https://img.shields.io/badge/-Python-3776AB?logo=python&logoColor=white) |
| [**aegis-sdk-typescript**](https://github.com/100monkeys-ai/aegis-sdk-typescript) | TypeScript/JS client SDK. Same surface, same guarantees, better DX. | ![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) |
| [**aegis-mcp-tools**](https://github.com/100monkeys-ai/aegis-mcp-tools) | Curated MCP server implementations, including the Zaru MCP server for LibreChat. | ![Mixed](https://img.shields.io/badge/-Mixed-lightgrey) |
| [**aegis-examples**](https://github.com/100monkeys-ai/aegis-examples) | Example agents — `hello-world`, `coder`, `code-reviewer`, `container-test` — plus the full Docker Compose stack to run them. **Start here.** | ![YAML](https://img.shields.io/badge/-YAML-red) |

### 📚 Knowledge & Community

| Repository | What It Is |
| --- | --- |
| [**aegis-docs**](https://github.com/100monkeys-ai/aegis-docs) | Public documentation site at [docs.100monkeys.ai](https://docs.100monkeys.ai). Fumadocs on Next.js. |
| [**monkey-troop**](https://github.com/100monkeys-ai/monkey-troop) | FOSS P2P AI compute grid. MIT licensed. Coordinator (Python), Worker (Rust), Client (Rust). Fork it, run it, earn Bananas. |

---

## Get Started in 3 Minutes

**Prerequisites:** Docker, Docker Compose, an OpenAI or Anthropic API key (or a local Ollama instance).

```bash
# 1. Clone the examples repo
git clone https://github.com/100monkeys-ai/aegis-examples.git
cd aegis-examples

# 2. Spin up the full AEGIS stack
cp .env.example .env
docker compose -f deploy/docker-compose.yml up -d

# 3. Deploy and run your first agent
cargo install aegis-orchestrator
aegis agent deploy ./agents/hello-world/agent.yaml
aegis task execute hello-world \
  --input '{"task": "Write a Python function that returns the Fibonacci sequence up to n."}' \
  --follow
```

Watch the loop run:

```markdown
2026-02-25T13:56:43.091943Z  INFO Delegating to daemon API
Executing agent 88b73d1b-0da0-4b92-9376-fd744b9cafbf...
✓ Execution started: f668f593-370f-4c19-b043-0487e9bd1ae5
[2026-02-25T13:56:43.140898+00:00] Execution started
[2026-02-25T13:56:43.164238272+00:00] Iteration 1
[2026-02-25T13:57:34.455428513+00:00] LLM [default]
[STDOUT] "First, I would write the required `fib_sequence` function in `/workspace/solution.py`:
```

→ **Full documentation:** [docs.100monkeys.ai](https://docs.100monkeys.ai)
→ **Create your first agent:** [docs.100monkeys.ai/docs/guides/writing-agents](https://docs.100monkeys.ai/docs/guides/writing-agents)

---

## The Agent Manifest

AEGIS agents are defined declaratively — Kubernetes-style YAML with physics built in:

```yaml
apiVersion: aegis/v1
kind: Agent
metadata:
  name: code-reviewer
  description: Reviews pull requests and suggests improvements
spec:
  runtime:
    kind: Standard
    language: python
    version: "3.11"
  security:
    network:
      mode: allowlist
      allowlist:
        - api.github.com
    filesystem:
      read: ["/workspace"]
      write: ["/workspace/output"]
    resources:
      cpu: "1.0"
      memory: "512Mi"
      timeout: "120s"
  validation:
    max_iterations: 10
    validators:
      - type: script
        path: validators/test_suite.py
      - type: schema
        schema_path: schemas/review_output.json
  capabilities:
    tools:
      - github.get_pr
      - filesystem.read
      - cmd.run:
          python: ["-m", "pytest", "test"]
```

The manifest is the contract. The orchestrator enforces it. The LLM operates inside it.

---

## Why Not OpenAI Assistants / LangChain / Others?

| | AEGIS | OpenAI Assistants | LangChain / OpenClaw |
| --- | --- | --- | --- |
| Kernel-level isolation | ✅ Firecracker | ❌ Cloud-only | ❌ None |
| Transparent iteration | ✅ Every attempt visible | ❌ Black box | ⚠️ Manual |
| System-wide learning | ✅ Cortex (persists forever) | ❌ Thread-scoped | ❌ None |
| Self-hostable | ✅ Full control | ❌ | ⚠️ DIY |
| BYOLLM | ✅ Any model, any provider | ❌ OpenAI only | ⚠️ Complex |
| Compliance-ready audit trail | ✅ Cryptographic (SMCP) | ⚠️ Cloud logs | ❌ Manual |
| Cost model | ✅ Local + cloud hybrid, $0 Llama | 💸 Token-metered | 💸 Pass-through |
| Security model | ✅ Deterministic (physics) | 🎲 Probabilistic (ToS) | 🎲 Probabilistic (prompt) |

> *"While OpenAI and Anthropic race to build a smarter Brain (the Model), AEGIS is building a better Body (the Runtime). A smart brain in a fragile body dies. An average brain in an AEGIS body survives, learns, and eventually wins."*

---

## The Cortex Effect

Every execution teaches the next one.

```markdown
Execution 1:   TypeError: 'NoneType' has no attribute 'split'  →  Fixed on iteration 3
               ↓ Pattern stored: null-check-before-string-split (weight: 1)

Execution 47:  Same error class detected
               ↓ Cortex pattern retrieved
               → First-attempt success (no iterations needed)

Execution 847: The pattern has been reinforced 800 times.
               Every new agent born into this runtime already knows the answer.
```

Patterns compose into Skills. Skills persist across restarts, upgrades, and model swaps. The intelligence is **in the runtime**, not in the model weights.

---

## The License Philosophy

| Repository | License | Why |
| --- | --- | --- |
| `aegis-orchestrator` | **AGPL-3.0** | If you run it as a service, you open-source your changes. We believe in the commons. |
| `monkey-troop` | **MIT** | Community compute infrastructure should be maximally free. Fork it, run it, profit from it. |

---

## Join the Evolution

> *"We are not betting on the Monkey. We are betting on the Loop."*

[📖 **Documentation**](https://docs.100monkeys.ai) · [💬 **Discord**](https://discord.100monkeys.ai) · [🌐 **Community**](https://troop.100monkeys.ai) · [🚀 **Cloud Waitlist**](https://100monkeys.ai) · [🐒 **Try Zaru**](https://myzaru.com) · [📧 **Investors**](mailto:invest@100monkeys.ai)

> *Pre-alpha · Self-host available now · Cloud launching Q2 2026*

---

**100monkeys** · Powered by [AEGIS](https://github.com/100monkeys-ai/aegis-orchestrator) · Built in Rust · Isolated by Firecracker · Remembered by Cortex
