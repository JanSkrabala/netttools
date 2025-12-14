# NetTools-VelesAI

**Version:** 2.2.0  
**Description:** Enterprise-grade network device management platform with AI-powered assistance and a unified control plane  

---

## Overview

**NetTools-VelesAI** is an enterprise-grade, vendor-agnostic network management platform designed to replace text-heavy, CLI-driven workflows with **visual network reasoning augmented by AI**.

The platform combines:
- a **Unified Control Plane** for multi-vendor network devices
- a **visual canvas** for understanding topology and dependencies
- **AI-assisted reasoning** for configuration, validation, and troubleshooting

It is built for complex, multi-site, multi-vendor environments where reliability, clarity, and operational safety matter.

---

## Architecture Overview

NetTools-Sapion follows a modern, layered architecture with clear separation of concerns.

Presentation Layer
├─ Web UI (React 19)
├─ API Clients (REST / WebSocket)
└─ Mobile UI (planned)

Application Layer
├─ Frontend (Vite + React)
├─ Backend (FastAPI)
└─ WebSocket Server

Business Logic Layer
├─ Unified Control Plane
├─ Policy & Config Services
└─ AI Tool Orchestration

Data Layer
├─ PostgreSQL
├─ pgvector (RAG embeddings)
└─ Encrypted credential storage

Integration Layer
├─ VyOS agents (WebSocket)
├─ Cisco devices (SSH)
├─ Ollama (local LLM)
└─ External APIs


---

## Core Capabilities

### Unified Control Plane (UCP)

A next-generation control plane for enterprise and industrial networks.

Key features:
- Multi-vendor device support (VyOS, Cisco IOS / IOS-XE, Juniper, OPNsense)
- Configuration lifecycle: draft → pending → applied → confirmed
- Commit-confirm pattern with automatic rollback
- Firewall, VPN, and service policy management
- Configuration drift detection
- Batch command execution and deployment optimisation
- Real-time monitoring and health checks

---

### VelesAI – AI Assistant

An AI-powered assistant designed to **support engineers**, not replace them.

Capabilities:
- Retrieval-Augmented Generation (RAG) over device configurations
- Context-aware chat with persistent memory
- Tool-based reasoning (inventory, analysis, config, knowledge)
- Web search and vulnerability knowledge integration
- Streaming responses and file-assisted analysis

---

### Device & Site Management

- Multi-vendor inventory and classification
- Site-based topology organisation
- Firmware lifecycle and compliance tracking
- Vulnerability correlation (CVE → device impact)
- Automated configuration backups
- SSH / API-based data collection with vendor parsers

---

## Technology Stack

### Backend

- **FastAPI** – async web framework
- **SQLModel / SQLAlchemy 2.0**
- **PostgreSQL 16+**
- **pgvector** – semantic embeddings
- **Ollama** – local LLM inference
- **Paramiko / Netmiko** – device connectivity
- **WebSockets** – real-time agent communication
- **Prometheus** – metrics
- **Sentry** – error tracking

### Frontend

- **React 19**
- **Vite**
- **Tailwind CSS**
- **Radix UI**
- **React Router**
- **Axios**
- **XTerm.js** – interactive terminal
- **Chart.js** – visual analytics

### Infrastructure

- Docker & Docker Compose
- Nginx (production reverse proxy)
- GitHub Actions (CI/CD)

---

## Quick Start

### Prerequisites

- Python 3.12+
- Node.js 18+
- PostgreSQL 16+
- Ollama (for AI features)
- Docker (optional)

---

🔐 Security Architecture

Encrypted credential storage (AES-256)

Role-based access control

SSH key and certificate-based device authentication

Mutual TLS for agent communication

Full audit and communication logging

Secure defaults throughout the stack

📊 Observability

Structured JSON logging

Correlation IDs for request tracing

Prometheus metrics endpoint

Health checks for database, agents, and external services

Real-time device and VPN status monitoring

🗺️ Roadmap (High Level)

Kubernetes deployment

Multi-region support

Predictive analytics and AI-assisted remediation

External REST API for third-party integrations

Advanced authentication (OAuth2, SAML, MFA)

Mobile companion application

🚧 Project Status

Actively developed

MVP+ with working UI, backend, and AI integration

Designed for pilot deployments with enterprise / industrial partners

📄 License

TBD
