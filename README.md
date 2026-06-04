# Welcome

I’m Jeremy. I build and document small, real-world digital systems focused on IT support, networking, security operations, observability, and browser-based technical presentation.

My GitHub is a working record of hands-on labs, infrastructure experiments, troubleshooting notes, security exercises, and digital systems projects. Current work includes a mini-SIEM / honeypot, a private DNS-over-TLS resolver, Linux and Windows troubleshooting labs, CTF writeups, and browser-based visualization systems using Three.js, WebAudio, TypeScript, and GLTF workflows.

My focus is practical: build small systems, observe their behavior, document what happens, and explain the results clearly.

---

# Technical Focus

My work centers on:

- IT support and systems troubleshooting across Linux, Windows, browsers, networking, and remote tools
- Security operations fundamentals: logs, alerts, SIEM workflows, honeypots, and incident notes
- Network behavior, DNS infrastructure, packet flow, SSH, VPNs, and service exposure
- Lightweight, inspectable infrastructure over opaque managed services
- Browser-based visualization and technical presentation using Three.js, WebAudio, TypeScript, and GLTF workflows
- Clear documentation that explains the problem, system behavior, troubleshooting process, and outcome

These projects are designed to be small, auditable, reproducible, and easy to explain.

---

# Public Contributions

- Contributor to OWASP Cheat Sheet Series
  - Added "Email Validation and Verification in Identity Systems"
  - Focus: identity security, normalization, verification flows, and safer account-handling logic
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

I prioritize understanding systems end-to-end: network behavior, service configuration, application behavior, logs, user interaction, and documentation.

Current areas of focus include:

- Extending my mini-SIEM / honeypot and reviewing the traffic it collects
- Troubleshooting Linux and Windows systems, including networking, permissions, services, and remote access
- Running and testing my own DNS infrastructure, including recursive DNS, DNSSEC, and DNS-over-TLS
- Practicing log parsing, filtering, alert review, and basic incident notes
- Building Python and JavaScript tools for network behavior, authentication flows, encryption basics, telemetry presentation, and log analysis
- Developing realtime browser-based industrial visualization systems
- Working with GLTF-driven rendering pipelines and interactive technical presentation workflows
- Practicing clear “problem → system → behavior → outcome” documentation

I run a home lab and use GitHub to track the work chronologically.

---

# Selected Systems

## [Mini SIEM Dashboard & Honeypot](https://github.com/jeremyrayjewell/mini-siem-dashboard)

Python · JavaScript · Flask · TCP listeners · JSON logging · Dashboard

A compact SOC-style lab that exposes fake TCP services, records unsolicited traffic, and feeds a lightweight dashboard for log review and pattern analysis.

The system exposes fake services such as SSH, FTP, RDP, MySQL, Redis, and MongoDB on high ports, writes structured events to JSON, and displays summary data in a browser-based dashboard.

Event fields include:

- timestamp
- IP address
- port
- source port
- protocol
- event type
- banner sent
- user agent
- message

The dashboard polls `/api/stats` for totals, top IPs, protocol and port breakdowns, and recent events.

### Operational Notes

- Deployed as a live containerized service
- Generates real unsolicited traffic from internet scanning activity
- Captures repeated SSH/FTP probing patterns across multiple IP ranges
- Used for log triage, alert review, and repeated pattern comparison

> Repo: [`mini-siem-dashboard`](https://github.com/jeremyrayjewell/mini-siem-dashboard)

---

## [Private DNS-over-TLS Resolver](https://github.com/jeremyrayjewell/secure-dns-resolver)

Unbound · DNS · TLS · DNSSEC · Docker

A self-hosted recursive DNS resolver that exposes DNS-over-TLS and performs full DNSSEC validation.

Built to understand DNS infrastructure at the protocol level rather than relying entirely on managed services.

The resolver supports:

- Recursive resolution with no forwarding by default
- DNSSEC chain validation
- DNS-over-TLS on TCP/8853
- Plain DNS on 8053 for testing
- Containerized deployment
- Runtime certificate injection

### Operational Notes

- Public-facing resolver testable via `dig`
- Performs real DNSSEC validation chains
- TLS endpoint verifiable via `openssl`
- Used for packet capture analysis, service testing, DNS flow review, and infrastructure troubleshooting

Used to practice:

- DNS packet flow from root to TLD to authoritative servers
- TLS configuration and verification
- Service deployment and health checks
- Packet capture analysis
- DNS egress behavior across different environments

> Repo: [`secure-dns-resolver`](https://github.com/jeremyrayjewell/secure-dns-resolver)

---

## [Industrial Object Viewer](https://github.com/jeremyrayjewell/industrial-object-viewer)

React · Three.js · TypeScript · FastAPI · GLTF

A browser-based industrial visualization framework for interactive product presentation, technical demonstrations, and exporter-facing machine explainers.

The project focuses on:

- GLTF-ready rendering architecture
- Manifest-driven machine definitions
- Exploded-view interaction
- Annotation overlays
- Telemetry visualization
- Browser-based technical presentation workflows

The current system uses:

- React Three Fiber
- Three.js
- TypeScript
- FastAPI
- Metadata-driven machine manifests
- Mesh-binding interaction systems

The architecture is designed around a machine pipeline:

MachineManifest → Renderer → Mesh Binding → Interaction Layer → Annotation System

The long-term direction is focused on browser-native industrial visualization and realtime technical communication rather than entertainment-oriented 3D systems.

> Repo: [`industrial-object-viewer`](https://github.com/jeremyrayjewell/industrial-object-viewer)

---

# Supporting Work

## [cyber_journal](https://github.com/jeremyrayjewell/cyber_journal)

A running log of labs, notes, packet captures, troubleshooting sessions, infrastructure experiments, protocol-focused learning work, and CTF writeups.

The emphasis is on documenting process clearly: what the problem was, what tools were used, what behavior was observed, and what conclusions can be drawn.

---

## [CTF Write-ups](https://github.com/jeremyrayjewell/cyber_journal/tree/main/writeups)

TryHackMe, OverTheWire, OWASP, and related exercises with emphasis on enumeration, protocol understanding, troubleshooting logic, and root-cause analysis rather than shortcuts.

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

## IT Support / Systems

Linux · Windows · WSL · Docker · VirtualBox · basic server administration · browser troubleshooting · remote support · service configuration · permissions · connectivity troubleshooting · documentation

## Security / Infrastructure

Network scanning · packet analysis · DNS infrastructure · SSH workflows · VPN and tunneling basics · honeypot systems · SIEM concepts · log analysis · vulnerability assessment · hardening · troubleshooting distributed systems

## Programming / Automation

Python scripting · JavaScript · TypeScript · Bash · log parsing · CLI tools · APIs · React · FastAPI · Flask · Git · lightweight automation systems

## Visualization / Frontend

Three.js · React Three Fiber · WebAudio · realtime rendering · GLTF workflows · interaction systems · technical presentation interfaces · telemetry overlays

---

# Background

I’ve spent more than a decade teaching online, which means constant communication, time-pressure troubleshooting, and adapting explanations to different technical and cultural contexts.

I also write essays, technical notes, documentation, and editorial copy. My academic background in philosophy and history of ideas influences how I approach systems, abstraction, technical communication, and problem decomposition.

---

# Outside the Screen

I build small synthesizers in hardware and software, from 555-timer circuits to WebAudio and Three.js systems. I enjoy understanding systems by building, testing, breaking, documenting, and restructuring them.

---

# Direction

Current long-term interests include:

- IT support and systems troubleshooting
- Security operations fundamentals
- Structured event pipelines and observability systems
- Inspectable authentication and identity flows
- Lightweight infrastructure with explicit operational behavior
- Browser-native industrial visualization
- GLTF-driven technical presentation systems
- Realtime telemetry and subsystem visualization
- Technical documentation that makes system behavior understandable

---

# Links

[GitHub](https://github.com/jeremyrayjewell)  
[LinkedIn](https://www.linkedin.com/in/jeremyrayjewell)  
[HackerNoon](https://hackernoon.com/u/jeremyrayjewell)
