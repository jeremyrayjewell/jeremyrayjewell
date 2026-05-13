# Welcome

I’m Jeremy. I build and analyze small, real-world digital systems — focusing on network behavior, observable infrastructure, realtime browser-based visualization, and interactive technical presentation.

My work combines practical system investigation (logs, networking, infrastructure) with the development of small, focused tools for understanding how software behaves in real environments. I also build browser-based visualization and media systems using Three.js, WebAudio, and GLTF-based rendering workflows as part of my Aggregatron and industrial visualization projects.

GitHub is where I keep a working record of these activities — experiments, tools, notes, and evolving systems — rather than a polished portfolio.

---

# Digital Systems Focus

My work centers on:

- Observability of real-world systems (logs, network traffic, DNS behavior)
- Security as a property of system design, not just defensive tooling
- Lightweight, inspectable infrastructure over opaque managed services
- Browser-based computation and realtime rendering as programmable environments
- Industrial visualization and interactive technical presentation using Three.js and GLTF workflows
- Small, understandable systems with explicit interaction and rendering pipelines

These projects are designed to be small, auditable, and reproducible so their behavior can be understood, tested, extended, and communicated clearly.

---

# Public Contributions

- Contributor to OWASP Cheat Sheet Series  
  - Added "Email Validation and Verification in Identity Systems"  
  - Focus: identity security, normalization, and verification flows  
  - PR: https://github.com/OWASP/CheatSheetSeries/pull/2072

---

# Tech Stack

## Languages & Scripting

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnubash&logoColor=white)

## Security & Networking

![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?logo=kalilinux&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?logo=wireshark&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-004B87?logo=nmap&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6F00?logo=burpsuite&logoColor=white)
![Hashcat](https://img.shields.io/badge/Hashcat-800000?logo=hashnode&logoColor=white)

## Web, Visualization & APIs

![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Three.js](https://img.shields.io/badge/Three.js-000000?logo=threedotjs&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)

## Platforms & Tooling

![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![Windows](https://img.shields.io/badge/Windows-0078D6?logo=windows&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?logo=virtualbox&logoColor=white)

---

# Current Focus

I prioritize understanding systems end-to-end (network → service → application → interaction layer) rather than isolated tools.

Current areas of focus include:

- Realtime browser-based industrial visualization
- GLTF-driven rendering pipelines and interactive product presentation
- Lightweight telemetry and annotation systems for technical demos
- Extending my mini-SIEM / honeypot and reviewing the traffic it collects
- Troubleshooting Linux and Windows systems (networking, permissions, services)
- Building Python and JavaScript tools for:
  - network behavior
  - authentication flows
  - encryption basics
  - telemetry presentation
  - log parsing and filtering
- Running and testing my own DNS infrastructure (recursive DNS, DNSSEC, DNS-over-TLS)
- Practicing clear “problem → system → behavior → outcome” documentation

I run a home lab and use GitHub to track the work chronologically.

---

# Key Projects

# Selected Systems

- industrial-object-viewer
- mini-siem-dashboard  
- secure-dns-resolver  

# Supporting Work

- cyber_journal  
- CTF write-ups  
- Three.js + WebAudio experiments  

---

## [industrial-object-viewer](https://github.com/jeremyrayjewell/industrial-object-viewer)

React · Three.js · TypeScript · FastAPI · GLTF

A browser-based industrial visualization framework for interactive product presentation, technical demonstrations, and exporter-facing machine explainers.

The project focuses on:

- GLTF-ready rendering architecture
- manifest-driven machine definitions
- exploded-view interaction
- annotation overlays
- telemetry visualization
- browser-based technical presentation workflows

The current system uses:

- React Three Fiber
- Three.js
- TypeScript
- FastAPI
- metadata-driven machine manifests
- mesh-binding interaction systems

The architecture is designed around a machine pipeline:

MachineManifest → Renderer → Mesh Binding → Interaction Layer → Annotation System

The long-term direction is focused on browser-native industrial visualization and realtime technical communication rather than entertainment-oriented 3D systems.

> [Repo: `industrial-object-viewer`](https://github.com/jeremyrayjewell/industrial-object-viewer)

---

## [Mini SIEM Dashboard & Honeypot (Python + JS)](https://github.com/jeremyrayjewell/mini-siem-dashboard)

Python + JavaScript

A small system that exposes fake TCP services (SSH, FTP, RDP, MySQL, Redis, MongoDB on high ports), writes structured events to JSON, and feeds a lightweight JS dashboard.

- Backend: Flask with custom TCP listeners
- Event fields: timestamp, ip, port, src_port, protocol, event_type, banner_sent, user_agent, message
- Frontend: polls `/api/stats` for totals, top IPs, protocol/port breakdowns, and recent events
- Deployment: containerized; runs as a small cloud service with a static dashboard
- Captures repeated SSH/FTP probing patterns across multiple IP ranges

### Operational Notes

- Deployed as a live containerized service
- Generates real unsolicited traffic from internet scanning activity
- Logs used for repeated analysis and pattern comparison

It serves as a compact SOC-style lab for generating traffic and practicing log triage.

> [Repo: `mini-siem-dashboard`](https://github.com/jeremyrayjewell/mini-siem-dashboard)

---

## [Private DNS-over-TLS Resolver (Unbound)](https://github.com/jeremyrayjewell/secure-dns-resolver)

Unbound · DNS · TLS · DNSSEC

A self-hosted recursive DNS resolver that exposes DNS-over-TLS and performs full DNSSEC validation.

Built to understand DNS infrastructure at the protocol level rather than relying entirely on managed services.

- Recursive resolution (no forwarding by default)
- DNSSEC chain validation
- DNS-over-TLS on TCP/8853
- Plain DNS on 8053 for testing
- Containerized deployment
- Runtime certificate injection

### Operational Notes

- Public-facing resolver testable via `dig`
- Performs real DNSSEC validation chains
- TLS endpoint verifiable via `openssl`

Used to practice:

- DNS packet flow (root → TLD → authoritative)
- TLS configuration and verification
- Service deployment and health checks
- Packet capture analysis
- DNS egress behavior across different environments

> [Repo: `secure-dns-resolver`](https://github.com/jeremyrayjewell/secure-dns-resolver)

---

## [cyber_journal](https://github.com/jeremyrayjewell/cyber_journal)

A running log of labs, notes, packet captures, troubleshooting sessions, infrastructure experiments, and protocol-focused learning work.

---

## [CTF Write-ups](https://github.com/jeremyrayjewell/cyber_journal/tree/main/writeups)

TryHackMe, OverTheWire, OWASP, and related exercises with emphasis on enumeration, protocol understanding, and root-cause analysis rather than shortcuts.

---

## [Three.js + WebAudio Experiments](https://github.com/jeremyrayjewell/webaudioapi_aggregatron)

Browser-based realtime rendering and media-system experiments using WebAudio, shaders, procedural graphics, and interactive browser computation.

These projects increasingly serve as foundations for more structured visualization and technical presentation systems.

---

# Certifications

![CompTIA Security+](https://img.shields.io/badge/-CompTIA%20Security%2B-E62A36?logo=comptia&logoColor=white)

![Google Cybersecurity Certificate](https://img.shields.io/badge/-Google%20Cybersecurity%20Certificate-4285F4?logo=google&logoColor=white)

![IBM Cybersecurity Analyst](https://img.shields.io/badge/-IBM%20Cybersecurity%20Analyst-052FAD?logo=ibm&logoColor=white)

---

# Skills & Tools

## Security / Infrastructure

Network scanning · packet analysis · DNS infrastructure · SSH workflows · VPN and tunneling basics · honeypot systems · log analysis · troubleshooting distributed systems

## Visualization / Frontend

Three.js · React Three Fiber · WebAudio · realtime rendering · GLTF workflows · interaction systems · technical presentation interfaces · telemetry overlays

## Programming / Automation

Python scripting · JavaScript/TypeScript · log parsing · CLI tools · APIs · React · FastAPI · Git · lightweight automation systems

## Systems

Linux · Windows · WSL · Docker · VirtualBox · basic server administration · network services · browser-based runtime systems

---

# Background

I’ve spent more than a decade teaching online, which means constant communication, time-pressure troubleshooting, and adapting explanations to different technical and cultural contexts.

I also write essays and technical notes, and I’m fluent in Spanish. My academic background in philosophy and history of ideas influences how I approach systems, abstraction, technical communication, and problem decomposition.

---

# Outside the Screen

I build small synthesizers in hardware and software — from 555-timer circuits to WebAudio/Three.js systems — and I enjoy understanding systems by building, testing, breaking, and restructuring them.

---

# Direction

Current long-term interests include:

- Browser-native industrial visualization
- GLTF-driven technical presentation systems
- Realtime telemetry and subsystem visualization
- Structured event pipelines and observability systems
- Inspectable authentication and identity flows
- Lightweight infrastructure with explicit operational behavior

---

# Links

[GitHub](https://github.com/jeremyrayjewell)  
[LinkedIn](https://www.linkedin.com/in/jeremyrayjewell)  
[HackerNoon](https://hackernoon.com/u/jeremyrayjewell)
