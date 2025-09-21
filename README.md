# One Day or Day One...

It's time that we locked in. 

I just finished watching Whiplash, and it showed me a lot about what it means to be good.

This marks the beginning of my four week plan to get good.


# The plan...
I definitely did not tell ChatGPT to make me a plan - (i did)

---

### A — Weekly themes & measurable goals

1. Week 1 — Recon + Web App Offense (Goal: solid web workflow & 10 writeups)

    - Complete 8–12 web challenges (OWASP Top10 style) + 2 small full web machines.
  
    - Produce 5 short writeups (recon → exploit → remediation).

2. Week 2 — Binary Exploitation & Reverse Engineering (Goal: exploit basics + 6 writeups)

    - Do 8–10 pwn/reverse/crypto challenges (mix easy→medium).
  
    - Complete at least 1 small local buffer overflow / format string challenge with PoC.

3. Week 3 — Active Directory / Windows Privilege Escalation (Goal: 2 full AD boxes + 6 writeups)

    - Finish 2 AD domain boxes (one initial access → foothold → domain compromise).
  
    - Practice common AD tools and attack paths (Kerberoast, AS-REP, lateral movement).

4. Week 4 — Red Team Capstone + Reporting (Goal: 1 full multi-service machine + portfolio polish)

    - Take one medium/hard full-scope machine (web + network + AD + binaries) start→finish.
  
    - Prepare a polished report + actionable remediation for the capstone and three prior writeups.

---

### B — Daily routine (repeatable)

Warm-up (15–30 min)

  - Read 1 short blog post / CVE summary or do 3 easy CTF micro-challenges (recon, crypto, or forensics).

Tool warmup (15–30 min)

  - Run a quick Nmap, a quick gobuster/dirsearch, a single Burp repeater experiment, or one GDB step on a small snippet.

Main session (60–180+ min)

  - Focused task (one machine or 3–5 challenges). Document as you go (commands + reasoning).

Wrap & reflect (15–30 min)

  - Write a small note or start a writeup section. Save screenshots and commands.

Weekend deep dive

  - Two long sessions for the week’s hardest machine(s). Record a screencap or time-lapse if you can.

---

### C — Specific exercise targets (types / objectives)

Aim to complete the following each week (substitute specific HTB/VulnHub/THM boxes you like):

Week 1 (Web)

  - 5 directory-bruteforce / content discovery tasks (use dirsearch / ffuf).
  
  - 4 SQLi / auth bypass / IDOR tasks (exploit and extract data).
  
  - 2 SSRF / deserialization / RCE web challenges (one LFI→RCE chain).
  
  - 1 full web machine that goes from user to root via web vuln → local pivot.

Week 2 (Pwn/RE)

  - 3 easy pwns (baby stack-smashing, NX/ASLR off).

  - 3 medium pwns (ROP basics, ret2libc).

  - 2 reversing/crypto (extract hidden key / decode algorithm).

  - 1 exploit where you write a small Python exploit and explain offsets.

Week 3 (AD/Windows)

  - 1 Windows box with misconfig / credential reuse to obtain user.

  - 1 Domain-joined box to escalate to domain admin (kerberoast / DCSync or GPO misconfig).

    - Practice: bloodhound runs, smbclient, impacket tools, wmiexec/CrackMapExec flows.

  - 2 privilege escalation Linux boxes (capabilities, SUID misconfig) to keep Linux skills sharp.

Week 4 (Capstone + Reporting)

  - Full scope machine: recon (network + web) → initial access → pivot → domain takeover or full host compromise.

  - Produce a 2–3 page professional pentest report and a one-page executive summary for the capstone.

  - Publish 3 polished writeups to your GitHub / personal blog.

---

### D — Tooling & command drills (daily/weekly)

Have these in your toolkit and practice the command flows (copyable checklist):

Recon

  `nmap -sC -sV -p- -oN nmap/full_$IP.txt $IP`

  `nmap -p- --min-rate=1000 -oN nmap/fast_$IP.txt $IP`

Web enumeration

  `ffuf -u http://$HOST/FUZZ -w /path/wordlist -mc 200,302`

  `nikto -h http://$HOST -output nikto/$HOST.txt`

Web exploitation

  - Burp repeater + Intruder chains; learn Burp extensions (Collaborator for OOB).

  `sqlmap --dbs -u 'http://host/vuln?id=1' --batch`

Binary / pwn

  - gdb-peda / gdb-pwntools for debugging

  `python3 -c 'print("A"*500)' > payload`

  - pwntools scripts for remote connect & exploit

AD / post-exploitation

  - rpcclient, smbclient, smbmap

  - impacket examples: GetNPUsers.py, psexec.py, secretsdump.py

  - BloodHound collection: SharpHound ingest and Neo4j query basics

Post-exploitation hygiene

  - Mimikatz for creds (lab only), hta/ps1 scripts for persistence (lab only).

  - Always clear logs only in labs where you own the environment.

---

### E — Writeups & portfolio checklist (do this for every machine)

For each completed challenge/machine, create:

  - Title + short summary (2–3 lines).

  - Timeline (how long it took).

  - Recon notes + commands.

  - Exploit steps (commands, payloads, screenshots).

  - Root/roothash proof + remediation suggestions.

  - GitHub repo with scripts (no sensitive data) and a markdown writeup.

    - Aim for 10 solid writeups by the end of Week 4 — pick 3 to polish into blog posts.
