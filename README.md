# 👋 Welcome

I’m Jeremy — an educator, technologist, and Security+ certified professional building a career in cybersecurity and remote IT support. My work blends analysis, troubleshooting, creative coding, and hands-on security practice, with an emphasis on **logs, SIEM-style workflows, and practical blue-team skills**.

I currently teach ESL remotely while transitioning into **remote U.S. help desk, security operations, and analyst roles**. I document my progress in my [cyber_journal](https://github.com/jeremyrayjewell/cyber_journal) to show real process, not just polished results.

### ⚙️ Tech Stack

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


# 🚀 Current Focus

I’m currently focused on **blue-team fundamentals and remote support workflows**, especially:

- Running and extending my **mini SIEM / honeypot** for continuous log analysis practice  
- Troubleshooting in **Linux and Windows** environments (connectivity, users, permissions, services)
- Practicing **ticket-style problem solving**: clear problem statements, steps taken, and outcomes
- Building small tools and labs in **Python and JavaScript** to deepen understanding of:
  - networking and protocols  
  - authentication and access control  
  - encryption and secure design  

I maintain an active home lab and use GitHub to keep a **transparent, chronological record** of what I’m learning and building.

---

# 🚨 Key Projects 

### 🛡️ [Mini SIEM Dashboard & Honeypot (Python + JS)](https://github.com/jeremyrayjewell/mini-siem-dashboard)
A small but complete **honeypot + mini-SIEM stack**:

- **Backend:** Python (Flask) app that runs fake TCP services (SSH, FTP, RDP, MySQL, Redis, MongoDB on high ports) and appends structured events to `events.json`.
- **Event schema:** `timestamp`, `ip`, `port`, `src_port`, `protocol`, `event_type`, `banner_sent`, `user_agent`, `message`.
- **Dashboard:** Modern JavaScript frontend that polls `/api/stats` and visualizes:
  - total events
  - top attacking IPs
  - ports/protocol distribution
  - recent events table with full metadata
- **Ops / deployment:** Containerized and deployed as a small cloud service with a static dashboard frontend and a Python API backend.

This project is designed to look and feel like a **tiny SOC tool**: I can generate malicious-looking traffic, watch events arrive in near real time, and practice log triage, basic enrichment, and pattern recognition.

**Skills:** Python (Flask), JSON logging, basic SIEM concepts, honeypots, Docker, HTTP APIs, JavaScript dashboards, Git, cloud deployment workflows

> [Repo: `mini-siem-dashboard` (see that repo’s README for live demo details and implementation notes)](https://github.com/jeremyrayjewell/mini-siem-dashboard)

---

### 📓 [cyber_journal](https://github.com/jeremyrayjewell/cyber_journal)
A continuously updated portfolio of labs, notes, and experiments covering networking, Linux, SIEM operations, cryptography, threat analysis, and exploitation fundamentals.

- OverTheWire wargames (Bandit, Natas) with structured write-ups
- Packet capture notes, log snippets, and tool usage examples
- Course notes from Google, IBM, and Security+ prep consolidated into usable references

**Skills:** Linux administration, documentation, version control, cybersecurity fundamentals, research workflow

---

### 🛡️ [CTF Write-ups](https://github.com/jeremyrayjewell/cyber_journal/tree/main/writeups)
Structured walkthroughs of OverTheWire wargames with a focus on **methodical enumeration and root-cause explanation** rather than just answers.

- Layered enumeration strategies
- Common misconfigurations and insecure defaults
- Simple automation with small Python/Bash snippets

**Skills:** enumeration, Linux CLI, Bash, Python automation, web & system exploitation basics

---

### 🎛️ [Three.js + WebAudio Experiments](https://github.com/jeremyrayjewell/webaudioapi_aggregatron)
Browser-based synthesizers, CRT-style shader overlays, audio-reactive visuals, and algorithmic music tools built with JavaScript and React.

**Skills:** JavaScript, React, Three.js, Web Audio API, creative coding, UI design

---

# 📜 Certifications

![CompTIA Security+](https://img.shields.io/badge/-CompTIA%20Security%2B-E62A36?logo=comptia&logoColor=white)  
Vendor-neutral baseline for security operations, risk management, incident response, and secure architecture.

![Google Cybersecurity Certificate](https://img.shields.io/badge/-Google%20Cybersecurity%20Certificate-4285F4?logo=google&logoColor=white)  
Hands-on labs with SIEM tools, incident reports, detection engineering basics, and SOC-style workflows.

![IBM Cybersecurity Analyst](https://img.shields.io/badge/-IBM%20Cybersecurity%20Analyst-052FAD?logo=ibm&logoColor=white)  
Coverage of network security, threat intelligence, and security operations with a focus on practical analysis and reporting.

---

# 🛠️ Skills & Tools

### Security & Blue Team  
- Network scanning and recon: Wireshark · Nmap  
- Web and application testing: Burp Suite (basic), common web vulns  
- Passwords & wireless: Aircrack-ng · Hashcat  
- Access & workflows: OpenSSH · tmux · VPN / SSH tunneling basics  
- Honeypots & SIEM-style logging via my **Mini SIEM Dashboard**

### Programming & Automation  
- **Python:** scripting, data parsing, log processing, small CLI tools  
- **JavaScript / TypeScript:** frontend dashboards, simple APIs  
- React · Three.js · Node.js  
- Git · GitHub Actions (basic CI workflows)

### Systems & Platforms  
- Kali Linux · Arch Linux · Ubuntu · Windows  
- VirtualBox · WSL  
- Basic server administration and service troubleshooting

---

# 🎙️ Background

I have over a decade of experience as an educator, delivering thousands of remote sessions that required:

- Calm, clear communication under pressure  
- Rapid troubleshooting of audio/video/connection issues  
- Working with learners and stakeholders across cultures and time zones  

I write essays, technical notes, and creative work, and I’m fluent in Spanish. My academic background in philosophy and history of ideas informs how I approach **threat modeling, systems thinking, and root-cause analysis**.

---

# 🔧 Outside the Screen

- [I build synthesizers in both code and hardware (including 555-timer noise circuits and small DIY audio projects).](https://github.com/jeremyrayjewell/soundmachines)  
- I enjoy breaking things safely, understanding them deeply, and rebuilding them with clarity and better documentation.

---

# 🌍 Find Me Online

[GitHub](https://github.com/jeremyrayjewell)  
[LinkedIn](https://www.linkedin.com/in/jeremyrayjewell)  
[HackerNoon](https://hackernoon.com/u/jeremyrayjewell)

![Snake light](https://raw.githubusercontent.com/jeremyrayjewell/jeremyrayjewell/output/github-contribution-grid-snake.svg#gh-light-mode-only)  
![Snake dark](https://raw.githubusercontent.com/jeremyrayjewell/jeremyrayjewell/output/github-contribution-grid-snake-dark.svg#gh-dark-mode-only)
