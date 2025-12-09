
# Offensive Security Engineer
Offensive Security Engineer Roadmap

It takes 2 hours of study per day, total time 20 months.

---
## List of Contents
- **[PHASE 0 — Setup & Mindset](#phase-0--setup--mindset)**
- **[PHASE A — Core Foundations](#phase-a--core-foundations)**
- **[PHASE B — Scripting & Recon Automation](#phase-b--scripting--recon-automation)**
- **[PHASE C — Web & Application Pentesting](#phase-c--web--application-pentesting)**
- **[PHASE D — System & Exploit Development Basics](#phase-d--system--exploit-development-basics)**
- **[PHASE E — Cloud & Infrastructure Offensive Security](#phase-e--cloud--infrastructure-offensive-security)**
- **[PHASE F — Post-Exploitation, Red Teaming & Tooling](#phase-f--post-exploitation-red-teaming--tooling)**
- **[PHASE G — Professionalization & Portfolio](#phase-g--professionalization--portfolio)**
- **[Final Deliverables Before Applying for Jobs](#final-deliverables-before-applying-for-jobs)**

---
## PHASE 0 — Setup & Mindset
**(20 hours)**

**Goal :** Understand what pentesting is, have a clear plan, and have a ready-to-use lab
-   **Learn these terms:** pentester, red team, blue team, bug bounty, PoC, scope, permission
- **Read a basic overview of legal frameworks (Thai and international):** never hack systems without explicit authorization

**Set up the lab:**
- PC/Notebook + VirtualBox/VMware
- Kali Linux / Parrot OS
- Create basic snapshots/backups
  
**Sign up for platforms:**
- TryHackMe, HackTheBox (start with beginner rooms/easy boxes)

### Practical recommendations
([hackers-arise: getting-started](https://hackers-arise.com/getting-started/))
- **Phase 0–A (Linux / Network / basic Python)**
	- Use the book Linux Basics for Hackers and the introductory Linux/Networking articles on the site as a reading list to support your labs on TryHackMe/HTB.
- **Phase C–E (Web / Exploit / ICS/SDR)**
	- Select free tutorials specifically in the Web App, Network Exploitation, and SCADA/ICS categories, focusing on topics where good resources are harder to find (e.g. ICS/SCADA, SDR).

---
## PHASE A — Core Foundations
**(140 hours ~2 months)**

**Goal:** Build your lab, learn OS fundamentals, understand networking/HTTP, and use essential tools.  

**Key Skills:** Linux CLI, basic Windows PowerShell, TCP/IP, DNS, HTTP, Git, Docker/VM operations.  

**Tools:** VirtualBox/VMware, Ubuntu/Kali VM, Windows VM, Docker, Git, tcpdump, Wireshark, curl.  

**Deliverables:** Lab README, VM snapshots, sample pcap files, Bash scripts, PowerShell snippets, screenshots.

**Core Activities:**
- Set up VMs + snapshots. 
- Install Docker, Git, and create a repo (offsec-lab).
- Practice CLI: ls, cd, cat, grep, awk, sed, chmod, chown, ps, top, systemctl, journalctl.  
- Capture packets using tcpdump and analyze with Wireshark.

**Practical Exercises:**
- Write a Bash port-scan script (host-only network).  
- Use Python’s http.server + send GET/POST with curl + capture traffic.
    
**KPIs:** Working lab, 1 artifact/week in GitHub, able to explain TCP 3-way handshake.

**Lab Practice:**
- TryHackMe: module “Complete Beginner/Pre-Security/Intro to Pentesting”

### [Arsenal](#arsenal-phase-a--core-foundations)

---
## PHASE B — Scripting & Recon Automation
**(140 hours ~2 months)**

**Goal:** Build automation skills for scanning, reconnaissance, and data collection.  

**Key Skills:** Python (requests, sockets, asyncio), Bash, regex, JSON/CSV parsing.
  
**Tools:** Python3, requests, BeautifulSoup, Nmap, masscan, Amass.

**Deliverables:**
- 2 working recon scripts (custom port-scanner + basic web crawler).
- README + optional unit tests.
    
**Core Activities:**
- Build a Python socket-based scanner.
- Create a web crawler that enumerates links/forms.
- Resolve domains, query WHOIS, and store results in CSV.
    
**KPIs:** Two fully functioning recon scripts + automated recon workflow.

**Lab Practice:**
- TryHackMe: module “Scripting/Intro to Python/Linux privilege escalation”  (The part that uses script)

### [Arsenal](#arsenal-phase-b--scripting--recon-automation)

---
## PHASE C — Web & Application Pentesting
**(200 hours ~3 months)**

**Goal:** Identify OWASP Top 10 vulnerabilities and create PoC exploits.  

**Key Skills:** HTTP internals, cookies/sessions, auth flaws, XSS, SQLi, CSRF, SSRF, IDOR.  

**Tools:** Burp Suite, browser devtools, sqlmap, ZAP.

**Deliverables:**
- 1 sanitized pentest report.
- Working PoC (XSS or SQLi).
- Write-up explaining methodology.

**Core Activities:**
- Manual testing workflow with Burp Suite.
- Analyze authentication & session flows.
- Write PoCs demonstrating exploitation inside your lab.

**KPIs:** Ability to identify and exploit 3 OWASP categories.

**Lab Practice:**
- TryHackMe: module “Web Fundamentals, OWASP Top 10, Burp”

### [Arsenal](#arsenal-phase-c--web--application-pentesting)

---
## PHASE D — System & Exploit Development Basics
**(220 hours ~3 months)**

**Goal:** Understand memory basics, debugging, and write simple exploits.  
**Key Skills:** C/C++ fundamentals, memory layout, buffer overflows, ASLR/NX, ROP basics.  
**Tools:** gcc/clang, GDB + pwndbg, Ghidra, radare2, pwntools.

**Deliverables:**
- 1–2 pwn CTF write-ups.
- Working basic exploit (sanitized).

**Core Activities:**
- Compile small C programs, introduce crashes, debug with GDB.
- Solve “easy” pwn challenges (stack overflow).
- Write automated exploits using pwntools.
    
**KPIs:** Can explain buffer overflows and create an exploit that works in your local lab.

**Lab Practice:**
- TryHackMe/HTB: Box difficulty Easy/Medium (that emphasizes privileges)

### [Arsenal](#arsenal-phase-d--system--exploit-development-basics)

---
## PHASE E — Cloud & Infrastructure Offensive Security
**(200 hours ~3 months)**

**Goal:** Identify cloud misconfigurations + offensive testing in cloud and infrastructure. 

**Key Skills:** AWS/Azure/GCP fundamentals, IAM weaknesses, container security, Terraform misconfigs.  

**Tools:** AWS CLI, Azure CLI, gcloud, ScoutSuite, Prowler, Docker, kubectl, Terraform.

**Deliverables:**
- Cloud misconfiguration report + remediation.
- Cloud automation or scanning script.

**Core Activities:**
- Build an AWS free-tier lab (VPC, EC2, S3, IAM).
- Test metadata service, S3 ACLs, weak IAM roles.
- Audit misconfigurations with ScoutSuite/Prowler.
    
**KPIs:** One real misconfig scenario exploited + documented remediation.

**Lab Practice:**
- TryHackMe/HTB: Windows/AD machine, internal network

### [Arsenal](#arsenal-phase-e--cloud--infrastructure-offensive-security)

---
## PHASE F — Post-Exploitation, Red Teaming & Tooling
**(200 hours ~3 months)**

**Goal:** Build offensive tradecraft, tooling, and post-exploitation skills.  

**Key Skills:** Lateral movement, persistence, credential extraction (lab only),  
PowerShell/WinRM, custom agent dev, OPSEC fundamentals.  

**Tools:** PowerShell, WinRM, Metasploit (concept only), custom Python/Go tools, C2 frameworks (lab only).

**Deliverables:**
- Simple post-exploitation tool or agent prototype.
- Mini red team scenario write-up.
- Detection & mitigation recommendations.

**Core Activities:**
- Build reverse-shell prototype.
- Linux/Windows privilege escalation labs.
- Simulate mini red team operation: initial access → lateral movement → persistence → exfil (all inside lab).
    
**KPIs:** Working tool prototype + red-team report showing offensive/defensive understanding.

### [Arsenal](#arsenal-phase-f--post-exploitation-red-teaming--tooling)

---
## PHASE G — Professionalization & Portfolio
**(180 hours ~3 months)**

**Goal:** Turn everything above into a professional identity and be ready to apply for jobs / take on work.
  
**Key Focus:** Portfolio, certifications, soft skills, workflow.

**Portfolio/GitHub**
- **Keep:**
	- THM/HTB writeups (with sensitive information properly redacted).
	- Scripts/tools you wrote yourself (recon, brute helpers, parsers, etc.).
	- A lab report template (following the structure real pentest companies use).
- **Create a personal site (static is fine) including:**
	- About me (Offensive Security Engineer / Pentester).
	- Skill matrix + the roadmap you’ve followed.
	- Links to GitHub and your TryHackMe/HTB profiles.

**Certifications to Target**
- **Start with (depending on your style):**
	- eJPT / PNPT / Security+.
- **Then move on to:**
	- OSCP or other practical, hands-on exam-style certifications.
- **Use the roadmap above to align with each exam’s objectives** 
	(e.g. OSCP → web, buffer overflow, privilege escalation, basic AD).
    
**Bug Bounty & Real-world Practice**
- **Sign up on platforms like HackerOne, Intigriti, etc.**  
	— choose programs that are open to beginners.
- **Initial goals:**
	- Aim to find some low/medium-severity issues  
	→ practice writing clear, solid reports.
- **Skills to train:**
	- Recon, finding forgotten subdomains.
	- Basic misconfigurations.
	- IDOR and access control flaws.

---
## Final Deliverables Before Applying for Jobs
**To look strong as an Offensive Security Engineer (Full-Stack), you must have:**
- **3–6 GitHub Projects:**  
	Recon scripts, web PoCs, exploit PoCs, cloud audit tools.
- **2 sanitized pentest reports**
- **1–3 CTF write-ups**
- **1 cloud misconfig analysis**
- **Professional README + lab setup documentation**

**Career-Ready KPIs (Global Targets)**
- Solve 3–5 challenges/week (TryHackMe/HTB).
- Multiple working PoCs.
- Full pentest report.
- Faster solving time week-over-week.

**Ethics & Legal Guidelines**
- Train only on systems you own or have explicit permission for.
- Sanitize PoCs before sharing.
- Follow responsible disclosure and regional laws.

---
## Arsenal PHASE A — Core Foundations

**Linux**
- [abex.io/linuxjourney](https://labex.io/linuxjourney)
- [tcm-sec: linux-fundamentals](https://academy.tcm-sec.com/p/linux-fundamentals)
- [inuxcommand.org](https://linuxcommand.org/index.php)
- [w3schools: bash](https://www.w3schools.com/bash/)

**PowerShell**
- [youtube: PowerShell For Beginners Full Course](https://youtu.be/UVUd9_k9C6A)

**TCP/IP, DNS**
- [udemy: comptia-networkplus-certification](https://www.udemy.com/course/comptia-networkplus-certification/) (Buy)    
- [youtube: Computer Networking Course](https://youtu.be/qiQR5rTSshw)
    
**HTTP**
- [developer: HTTP overview, status codes, methods](https://developer.mozilla.org/en-US/) 
   
 **Git**
- [w3schools: git](https://www.w3schools.com/git/)
- Book “Pro Git”
    
**Docker**
- [youtube: Complete Docker Course](https://youtu.be/RqTEHSBrYFw)
- [youtube: Docker Crash Course for Absolute Beginners](https://youtu.be/pg19Z8LL06w)
    
**VM operations**
- “VirtualBox/VMware – create lab, snapshots” + article “beginner home lab pentesting” (someone teaches how to set up Kali + Windows + AD mini-lab)
    
**IT**
- [tcm-sec: practical-help-desk](https://academy.tcm-sec.com/p/practical-help-desk)  
- [udemy: comptia-aplus-core-1](https://www.udemy.com/course/comptia-aplus-core-1/) (Buy)  
- [udemy: comptia-aplus-core-2](https://www.udemy.com/course/comptia-aplus-core-2/) (Buy)

---
## Arsenal PHASE B — Scripting & Recon Automation

---
## Arsenal PHASE C — Web & Application Pentesting

---
## Arsenal PHASE D — System & Exploit Development Basics

---
## Arsenal PHASE E — Cloud & Infrastructure Offensive Security

---
## Arsenal PHASE F — Post-Exploitation, Red Teaming & Tooling

---
## Arsenal PHASE G — Professionalization & Portfolio

---
