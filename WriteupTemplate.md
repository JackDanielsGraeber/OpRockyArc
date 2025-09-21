# {Title / Machine Name}
**Author:** {Your Name / Handle}  
**Platform:** {HTB / THM / VulnHub / local VM}  
**Difficulty:** {Easy / Medium / Hard}  
**Time spent:** {e.g. 6h 35m}  
**Date:** {YYYY-MM-DD}  
**Summary:**  
Short (2–3 lines) high-level summary of the compromise and final impact (e.g. "Initial RCE via vulnerable upload → PrivEsc via SUID binary → root shell").

---

## Table of Contents
- [Scope & Goals](#scope--goals)
- [Target Info](#target-info)
- [Recon](#recon)
- [Enumeration](#enumeration)
- [Exploitation (user)](#exploitation-user)
- [Privilege Escalation (root)](#privilege-escalation-root)
- [Post-Exploitation](#post-exploitation)
- [Proofs](#proofs)
- [Remediation & Mitigation](#remediation--mitigation)
- [Appendix (commands, scripts)](#appendix-commands-scripts)

---

## Scope & Goals
- **Scope:** {IP / machine name / services in-scope}  
- **Objective:** {Obtain user + root / capture flag / demonstrate data exfil}

## Target Info
- **IP / Hostname:** {x.x.x.x}  
- **Open Ports / Services (summary):** {e.g. 22/ssh, 80/http, 3306/mysql}  
- **OS / Versions (if known):** {e.g. Ubuntu 18.04, Apache 2.4.29}

## Recon
Describe high-level recon steps and results:

- Interesting findings: {e.g. /admin page, unusual service banner}

## Enumeration
List commands, outputs and observations that led to exploit paths.
- **Web:** dirb/ffuf results, endpoints of interest:

- Passive info (DNS, certs, public pages)
- Nmap scan(s) run:

- **Auth / API / Login pages:** {notes}
- **Other services:** {smb, mysql, ftp notes}

## Exploitation (user)
Step-by-step exploitation chain to obtain the initial user-level access. Include commands, payloads and reasoning.

1. **Vuln identification**
   - Evidence: `{request/response snippets, screenshot small}`

2. **Exploit**

- Explain what the payload does and why it works.

3. **Result**
- Show the shell or proof (limited, non-sensitive). Example:


## Privilege Escalation (root)
Document the path from user → root with commands and explanation.

1. **Local enumeration**

2. **Privilege escalation exploit**

- Explain the vulnerability and the exploit mechanism.

3. **Root proof**


## Post-Exploitation
Notes on persistence (lab only), lateral movement, data of interest, or clean-up steps taken. (Do not include real creds or sensitive data in public repos.)

## Proofs
Include small, non-sensitive screenshots or truncated outputs as proof. Prefer hashes or truncated flags if platform allows.

## Remediation & Mitigation
Practical, prioritized fixes:
- Short-term: {e.g. patch package X / disable exposed service / fix input validation}
- Long-term: {e.g. adopt least privilege, WAF, code review, secrets management}

## Appendix — Commands, Scripts & Resources
- Full commands used (copy/paste friendly)
- Scripts/exploit code (link to repo file)
- References: CVEs / blog posts / docs used

---

> **Tip:** keep your writeups script-friendly: include `scripts/` in the repo and a short `README.md` that shows how to re-run PoCs inside a disposable VM.
