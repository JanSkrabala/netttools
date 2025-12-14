# NetTools — Visual Network Reasoning Platform

NetTools is a visual network reasoning platform that allows engineers and operators to **see, understand, and safely change complex networks**, instead of parsing thousands of lines of configuration text.

The platform combines a **visual network canvas** with **AI-assisted reasoning** to reduce operational risk in multi-vendor, multi-site enterprise and industrial networks.

---

## Problem

Modern enterprise and industrial networks are:
- highly distributed (multi-site, hybrid IT/OT)
- built from multiple vendors (Cisco, VyOS, OPNsense, Juniper, etc.)
- managed through fragmented tools and raw CLI output

As a result:
- engineers reason about networks **in text**, not structure
- configuration changes are risky and error-prone
- understanding impact across sites and devices is slow and manual

This leads to outages, security incidents, and high operational cost.

---

## Solution

NetTools introduces **visual network reasoning** as the primary interface.

Key principles:
- the network is represented as a **live graph**, not text
- configurations are abstracted into a **vendor-agnostic model**
- AI augments human decision-making instead of replacing engineers

The system allows operators to:
- visually explore topology, policies, and dependencies
- validate changes before deployment
- reason about impact across devices and sites
- manage heterogeneous environments through a single control plane

---

## Core Features

- **Visual Network Canvas**
  - Drag-and-drop topology representation
  - Real-time device and connection state
  - Multi-site and multi-vendor support

- **Unified Control Plane**
  - Vendor-agnostic configuration model
  - Candidate configuration workflow with commit-confirm
  - Configuration drift and missing-config detection

- **AI-Augmented Reasoning**
  - Natural-language queries over network state
  - Impact analysis and change explanations
  - Retrieval-augmented reasoning over live configurations

- **Device Integration**
  - VyOS via secure WebSocket agents
  - Cisco via direct SSH (Netmiko)
  - Extensible vendor abstraction layer

---

## Target Users

- large enterprises
- energy and utilities
- industrial and manufacturing groups
- operators of mission-critical networks

Typical environments include hundreds of devices across many locations, where **failure cost is high** and **change safety is critical**.

---

## Technology Stack (high-level)

- Backend: Python, FastAPI
- Frontend: React, Tailwind
- Network integration: SSH, WebSockets
- Data: PostgreSQL, pgvector
- AI: local LLM inference (Ollama), RAG
- Deployment: containerised (Docker)

---

## Current Status

- working MVP with visual canvas
- live device integration (VyOS, Cisco)
- unified configuration model
- AI-assisted reasoning prototype
- pilot-ready architecture

The platform is currently in **pilot preparation phase** with focus on industrial and critical-infrastructure use cases.

---

## Vision

NetTools aims to become a **Cursor-like environment for network engineering**:
- visual first
- reasoning-driven
- vendor-agnostic
- human-in-the-loop AI

A tool that allows engineers to **understand networks as systems**, not as text files.

---

## Author

**Jan Skrabala**  
Founder & CEO  
Network architect with enterprise and critical-infrastructure experience

Contact: jan@skrabala.com
