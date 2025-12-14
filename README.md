NetTools-Sapion

AI-Augmented Visual Network Control Plane

Enterprise-grade, vendor-agnostic network management platform combining
visual network reasoning, policy abstraction, and AI-assisted operations.

🚀 What is NetTools-Sapion?

NetTools-Sapion is a next-generation network operations platform designed for modern, multi-vendor infrastructures.

It replaces fragmented CLI workflows and vendor-locked GUIs with a visual control plane, augmented by AI-assisted reasoning, validation, and automation.

Think:

“Terraform-level abstraction + firewall reasoning + live device control — without losing the engineer.”

🧠 Core Idea

Traditional network tools:

Are vendor-specific

Are CLI-heavy

Don’t scale cognitively

Don’t reason about intent

NetTools-Sapion introduces:

Visual network reasoning (sites, devices, links, policies)

Vendor-agnostic intent models

AI-assisted configuration, validation & explanation

Real-time device interaction (agents + SSH)

Human-in-the-loop safety (commit-confirm, rollback)

✨ Key Capabilities
🧩 Unified Control Plane (UCP)

Multi-vendor support: VyOS, Cisco, Juniper, OPNsense

Abstract policies → vendor-specific compilation

Commit-confirm with automatic rollback

Configuration drift detection

Secure device onboarding

🤖 AI-Augmented Operations (VelesAI)

Retrieval-Augmented Generation (RAG)

Device-aware reasoning (configs, topology, state)

Explain why a config works or fails

Assist with upgrades, CVEs, and changes

No “AI autopilot” — engineer stays in control

🖥️ Visual Network Model

Sites, devices, links, VPNs, firewalls

Real-time state & health

Visual diff of changes

Shared mental model for teams

🏗️ High-Level Architecture
Frontend (React)
   │
   ├─ Visual Control Plane
   ├─ AI Chat & Reasoning
   └─ Live Terminal
        │
Backend (FastAPI)
   │
   ├─ Unified Control Plane
   ├─ Policy Compilers
   ├─ AI Orchestration
   └─ WebSocket / SSH
        │
Devices (VyOS / Cisco / Others)


AI runs locally (via Ollama) — no cloud dependency required.

🛠️ Tech Stack (Summary)

Backend

FastAPI (Python 3.12)

PostgreSQL + pgvector

WebSockets + SSH

Ollama (local LLM inference)

Frontend

React 19 + Vite

Tailwind CSS

XTerm.js (live device terminal)

Security

Encrypted credentials

Certificate-based agents

Role-based access control

🎯 Target Users

Network & Security Engineers

MSPs / Enterprises with multi-vendor environments

Teams scaling beyond CLI-only workflows

Organisations needing auditability, safety & clarity

🔭 Why This Matters

Networks are no longer static.

They are:

Multi-cloud

Multi-vendor

Policy-heavy

Security-critical

NetTools-Sapion treats the network as a reasoned system, not just a set of commands.

🧪 Project Status

Actively developed

Functional MVP (local + lab environments)

Designed for enterprise-scale evolution

Architecture validated through real-world network operations

📌 Roadmap (High-Level)

Advanced policy simulation

Predictive change impact analysis

Compliance & risk scoring

Enterprise integrations

Scale-up deployments

📄 Documentation

Detailed architecture and internals live in /md:

ARCHITECTURE_OVERVIEW.md

UNIFIED_CONTROL_PLANE.md

AI_REASONING_MODEL.md

⚠️ Disclaimer

This project is not a toy and not a generic “AI wrapper”.

It is built by a network engineer for network engineers —
with AI used where it adds leverage, not magic.

