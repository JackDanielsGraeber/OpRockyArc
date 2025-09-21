# One-Page Pentest Summary
**Client / Project:** {Client Name or "Capstone Machine"}  
**Date:** {YYYY-MM-DD}  
**Author:** {Your Name / Team}  
**Engagement type:** {Lab assessment / External penetration test / Internal scan}  
**Scope:** {IP ranges / hostnames / web app URLs / excluded targets}

---

## Executive Summary (2–3 lines)
{Concise impact statement: e.g., "Critical remote code execution and privilege escalation found on host X, allowing full system compromise and potential domain access."}

## Key Findings (Top 3 — highest severity first)
1. **[Critical]** {Short title} — *Impact*: {what an attacker achieves}  
   **Evidence:** {file/flag id or short proof}  
   **Remediation:** {one-line fix}

2. **[High]** {Short title} — *Impact*: {e.g. credential exposure, accessible database}  
   **Remediation:** {one-line fix}

3. **[Medium]** {Short title} — *Impact*  
   **Remediation:** {one-line fix}

> (If fewer than 3, list top 1–2. If more, attach detailed findings in an appendix.)

## Scope & Methodology (brief)
- **Scope:** {hosts/services tested}  
- **Methodology:** Recon → Enumeration → Exploitation → PrivEsc → Reporting (all testing performed in controlled/lab environment).  
- **Tools used:** nmap, ffuf, Burp, gdb, pwntools, impacket, BloodHound (lab only)

## Remediation Priorities & Timeline
- **Immediate (0–7 days):** {e.g., patch vulnerable service / reset credentials / disable public access}  
- **Short-term (1–4 weeks):** {e.g., apply config changes, revoke stale accounts}  
- **Long-term (>1 month):** {e.g., adopt MFA, periodic pentests, secure SDLC}

## Contact & Next Steps
- **Report owner:** {Your name/email or team}  
- **Next suggested actions:** {schedule full report review, fix plan, retest date}  
- **Notes:** {any legal/ethical notes or limitations of the test}

---

**Appendix:** Full technical writeups, exploit code and logs are available in `{repo link}` or attached detailed report.
