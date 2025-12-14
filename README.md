# NetTools-VelesAI

**Description:** Enterprise-grade network device management platform with AI-powered assistance and a unified control plane

---

<!-- TOC -->
## Table of contents

- [Overview](#overview)
- [Architecture Overview](#architecture-overview)
- [Core Capabilities](#core-capabilities)
  - [Unified Control Plane (UCP)](#unified-control-plane-ucp)
  - [VelesAI – AI Assistant](#velesai--ai-assistant)
  - [Device & Site Management](#device--site-management)
- [Technology Stack](#technology-stack)
  - [Backend](#backend)
  - [Frontend](#frontend)
  - [Infrastructure](#infrastructure)
- [Quick Start](#quick-start)
  - [Prerequisites](#prerequisites)
  - [Running locally (example)](#running-locally-example)
- [Security Architecture](#security-architecture)
- [Observability](#observability)
- [Roadmap](#roadmap)
- [Project Status](#project-status)
- [License](#license)
<!-- /TOC -->

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

NetTools-VelesAI follows a modern, layered architecture with a clear separation of concerns:

Presentation layer
- Web UI (React 19)
- API clients (REST / WebSocket)
- Mobile UI (planned)

Application layer
- Frontend (Vite + React)
- Backend (FastAPI)
- WebSocket server

Business logic layer
- Unified Control Plane
- Policy & config services
- AI tool orchestration

Data layer
- PostgreSQL
- pgvector (RAG embeddings)
- Encrypted credential storage

Integration layer
- VyOS agents (WebSocket)
- Cisco devices (SSH)
- Ollama (local LLM)
- External APIs

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
- Batch command execution and deployment optimization
- Real-time monitoring and health checks

## Visual Network Canvas

At the core of NetTools-VelesAI is a **visual network canvas** that allows engineers to *see* the network instead of parsing text configurations.

The canvas provides:
- A live, interactive topology view across sites and vendors
- Visual representation of devices, links, zones, and dependencies
- Context-aware actions (inspect, configure, validate, deploy)
- Real-time status indicators (health, drift, VPN state)

The visual layer acts as a **reasoning surface**:
changes, risks, and dependencies are visible before commands are executed.

![Visual Network Canvas – Topology View](docs/images/canvas-topology.png)
![Visual Network Canvas – Device Context](docs/images/canvas-device-context.png)


### VelesAI – AI Assistant

An AI-powered assistant designed to support engineers, not replace them.

Capabilities:
- Retrieval-Augmented Generation (RAG) over device configurations
- Context-aware chat with persistent memory
- Tool-based reasoning (inventory, analysis, config, knowledge)
- Web search and vulnerability knowledge integration
- Streaming responses and file-assisted analysis

## Vulnerabilities & Compliance

NetTools-VelesAI includes a dedicated vulnerability and lifecycle awareness layer.

Features:
- CVE ingestion and correlation (device, OS, firmware)
- Impact mapping: vulnerability → affected devices → sites
- End-of-life and end-of-support tracking
- Upgrade recommendations aligned with vendor guidance
- Compliance-ready views for audits and reporting

Vulnerabilities are treated as **operational risk**, not isolated alerts.

![Vulnerability Dashboard](docs/images/vulnerabilities-dashboard.png)
![End-of-Life & Compliance View](docs/images/eol-compliance.png)


### Financial & Lifecycle Controls

NetTools-VelesAI connects **technical network state** with **financial and lifecycle awareness**.

Capabilities include:
- Device-level CapEx and OpEx tracking
- License and support contract visibility
- Firmware lifecycle awareness (recommended, non-standard, end-of-life)
- CSV import/export for finance, inventory, and audits
- Aggregated cost and risk views per site or region

This enables engineering, security, and finance teams to reason over the **same source of truth**.

![Financial Overview – Devices & Lifecycle](docs/images/finance-overview.png)
![CSV Import & Export](docs/images/csv-import.png)

### Device & Site Management

- Multi-vendor inventory and classification
- Site-based topology organization
- Firmware lifecycle and compliance tracking
- Vulnerability correlation (CVE → device impact)
- Automated configuration backups
- SSH / API-based data collection with vendor parsers

---

## Technology Stack

### Backend
- FastAPI — async web framework
- SQLModel / SQLAlchemy 2.0
- PostgreSQL 16+
- pgvector — semantic embeddings
- Ollama — local LLM inference
- Paramiko / Netmiko — device connectivity
- WebSockets — real-time agent communication
- Prometheus — metrics
- Sentry — error tracking

### Frontend
- React 19
- Vite
- Tailwind CSS
- Radix UI
- React Router
- Axios
- XTerm.js — interactive terminal
- Chart.js — visual analytics

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
- Ollama (for AI features; optional if you plan to run AI features locally)
- Docker (optional, recommended for local sandbox)


---

## Security Architecture

- Encrypted credential storage (AES-256)
- Role-based access control (RBAC)
- SSH key and certificate-based device authentication
- Mutual TLS for agent communication
- Full audit and communication logging
- Secure defaults across the stack

---

## Observability

- Structured JSON logging
- Correlation IDs for request tracing
- Prometheus metrics endpoint
- Health checks for database, agents, and external services
- Real-time device and VPN status monitoring

---

## Roadmap (High Level)

- Multi-region support
- Predictive analytics and AI-assisted remediation
- External REST API for third-party integrations
- Advanced authentication (OAuth2, SAML, MFA)

---

## Project Status

Actively developed — MVP+ with working UI, backend, and AI integration. Designed for pilot deployments with enterprise / industrial partners.

---

## License

License will be defined prior to first public release / pilot agreement.

