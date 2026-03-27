# Welcome

I’m Jeremy. I work across digital systems, security-oriented analysis, and browser-based media tools.

My work combines practical system investigation (logs, networking, infrastructure) with the development of small, focused tools for understanding how software behaves in real environments. I also build browser-based media systems using WebAudio and Three.js as part of my Aggregatron project.

GitHub is where I keep a working record of these activities — experiments, tools, and notes — rather than a polished portfolio.

---

# Digital Systems Focus

My work centers on:

- Observability of real-world systems (logs, network traffic, DNS behavior)
- Security as a property of system design, not just defensive tooling
- Lightweight, inspectable infrastructure over opaque managed services
- Browser-based computation and media systems as programmable environments

These projects are designed to be small, auditable, and reproducible — 
so their behavior can be understood, tested, and extended.

---

# Public Contributions

- Contributor to OWASP Cheat Sheet Series  
  - Added "Email Validation and Verification in Identity Systems"  
  - Focus: identity security, normalization, and verification flows  
  - PR: https://github.com/OWASP/CheatSheetSeries/pull/2072

---

# Tech Stack

**Languages & Scripting**  
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnubash&logoColor=white)

**Security & Networking**  
![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?logo=kalilinux&logoColor=white)
![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?logo=wireshark&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-004B87?logo=nmap&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6F00?logo=burpsuite&logoColor=white)
![Hashcat](https://img.shields.io/badge/Hashcat-800000?logo=hashnode&logoColor=white)

**Web, Apps & APIs**  
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?logo=threedotjs&logoColor=white)

**Platforms & Tooling**  
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![Windows](https://img.shields.io/badge/Windows-0078D6?logo=windows&logoColor=white)
![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?logo=virtualbox&logoColor=white)

# Current Focus

I’m concentrating on blue-team fundamentals and common support workflows:

- Extending my mini-SIEM / honeypot and reviewing the traffic it collects  
- Troubleshooting Linux and Windows (networking, permissions, services)  
- Practicing clear “problem → steps → outcome” documentation  
- Building Python and JavaScript tools for:
  - network behavior  
  - simple authentication flows  
  - encryption basics  
  - log parsing and filtering
- Running and testing my own DNS infrastructure (recursive DNS, DNSSEC, DNS-over-TLS)

I run a home lab and use GitHub to track the work chronologically.

---

# Key Projects

##  [Mini SIEM Dashboard & Honeypot (Python + JS)](https://github.com/jeremyrayjewell/mini-siem-dashboard)
Python + JavaScript

A small system that exposes fake TCP services (SSH, FTP, RDP, MySQL, Redis, MongoDB on high ports), writes structured events to JSON, and feeds a lightweight JS dashboard.

- Backend: Flask with custom TCP listeners  
- Event fields: timestamp, ip, port, src_port, protocol, event_type, banner_sent, user_agent, message  
- Frontend: polls `/api/stats` for totals, top IPs, protocol/port breakdowns, and recent events  
- Deployment: containerized; runs as a small cloud service with a static dashboard

It serves as a compact SOC-style lab for generating traffic and practicing log triage.

> [Repo: `mini-siem-dashboard` (see that repo’s README for live demo details and implementation notes)](https://github.com/jeremyrayjewell/mini-siem-dashboard)

---

## [Private DNS-over-TLS Resolver (Unbound)](https://github.com/jeremyrayjewell/secure-dns-resolver)

Unbound, DNS, TLS, DNSSEC

A self-hosted recursive DNS resolver that exposes DNS-over-TLS and performs full DNSSEC validation. Built to understand how real DNS infrastructure works at the protocol level.

- Recursive resolution (no forwarding by default)  
- DNSSEC chain validation  
- DNS-over-TLS on TCP/8853  
- Plain DNS on 8053 for testing  
- Containerized and deployed on Fly.io  
- Certificates generated and injected at runtime (no secrets in repo)

Used to practice:

- DNS packet flow (root → TLD → authoritative)  
- TLS configuration and verification  
- Service deployment and health checks  
- Testing with `dig`, `openssl`, and packet captures  
- Understanding how VPNs affect DNS egress

It’s a clean, auditable example of running real infrastructure instead of relying on managed DNS or opaque services.

> [Repo: `secure-dns-resolver`](https://github.com/jeremyrayjewell/secure-dns-resolver)

---

## [cyber_journal](https://github.com/jeremyrayjewell/cyber_journal)

A running log of labs, notes, wargames, packet captures, troubleshooting sessions, and anything else that contributes to understanding systems and protocols.

---

## [CTF Write-ups](https://github.com/jeremyrayjewell/cyber_journal/tree/main/writeups)

TryHackMe, OverTheWire, OWASP, and related exercises with emphasis on enumeration and root-cause thinking rather than shortcuts or “just the flags.”

---

## [Three.js + WebAudio Experiments](https://github.com/jeremyrayjewell/webaudioapi_aggregatron)

Browser-based synthesizers, algorithmic music tools, shader experiments, and other creative coding projects built with JS and React.

---

# Certifications

![CompTIA Security+](https://img.shields.io/badge/-CompTIA%20Security%2B-E62A36?logo=comptia&logoColor=white)  

![Google Cybersecurity Certificate](https://img.shields.io/badge/-Google%20Cybersecurity%20Certificate-4285F4?logo=google&logoColor=white)  

![IBM Cybersecurity Analyst](https://img.shields.io/badge/-IBM%20Cybersecurity%20Analyst-052FAD?logo=ibm&logoColor=white)  

---

# Skills & Tools

**Security / Blue Team**  
Network scanning · packet analysis · basic web testing · password and wireless tools · SSH workflows · VPN and tunneling basics · honeypot and log analysis

**Programming / Automation**  
Python scripting · log parsing · CLI tools · JavaScript/TypeScript · simple APIs · React · Three.js · Git · CI basics

**Systems**  
Kali Linux · Ubuntu · Arch · Windows · VirtualBox · WSL · basic server administration

---

# Background

I’ve spent more than a decade teaching online, which means constant communication, time-pressure troubleshooting, and working with different environments and constraints. I also write essays and technical notes, and I’m fluent in Spanish. My academic background in philosophy and history of ideas influences how I approach systems, problems, and threat modeling.

---

# Outside the Screen

I build small synthesizers in hardware and software — from 555-timer circuits to WebAudio/Three.js tools — and I enjoy breaking things safely to understand them better.

---

# Links

[GitHub](https://github.com/jeremyrayjewell)  
[LinkedIn](https://www.linkedin.com/in/jeremyrayjewell)  
[HackerNoon](https://hackernoon.com/u/jeremyrayjewell)
