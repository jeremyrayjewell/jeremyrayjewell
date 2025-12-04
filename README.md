# Welcome

I’m Jeremy. I teach, write code, run labs, and work toward a full-time role in cybersecurity and remote IT support. Most of my work is practical: reading logs, troubleshooting systems, testing assumptions, and building small tools to understand how things behave.  

GitHub is where I keep the record — experiments, fixes, and notes — not a polished portfolio.

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
