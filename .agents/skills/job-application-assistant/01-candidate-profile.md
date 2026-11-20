---
framework_version: 1.1.1
---

# Candidate Profile

Source: four resumes in `documents/cv/` (Resume_final, Security_Engineer, Cyber_GRC, Security_Analyst).
**⚠ = the source resumes disagree and Purvansh has not yet confirmed which version is right.
Never put a ⚠ claim on a CV or cover letter until it is confirmed.** Where resumes disagree,
the version used below is the one most resumes agree on (or the most conservative one).

## Identity
- **Name:** Purvansh Bhatt
- **Location:** Jersey City, NJ 07306, USA
- **Phone:** +1 917-999-6730
- **Email:** purvansh95b@gmail.com
- **LinkedIn:** (URL not yet recorded)
- **GitHub:** https://github.com/purvanshbhatt
- **Status:** Founder & Security Engineer at ResilAI (own startup, Feb 2026-present); seeking a full-time security role
- **Work authorization:** US F-1 STEM OPT, valid through **July 2027**. US employers must be E-Verify enrolled. Will need H-1B (or equivalent) sponsorship to continue past July 2027. Outside the US, needs an employer-sponsored work visa.
- **Constraints:** Open to relocation, can move within 2-3 weeks of an offer (visa processing time outside the US is extra). Target regions: US, Canada, UK, all of Europe (incl. Netherlands, Germany, Luxembourg), Singapore, Japan, UAE (Dubai), Qatar (Doha), Australia, New Zealand. Remote and hybrid welcome.

### Languages

| Language | Level | Notes |
|----------|-------|-------|
| English | Full professional proficiency | ⚠ Level assumed from US MS + US work. No other languages declared yet. |

## Education

| Degree | Period | Institution | Key Topics |
|--------|--------|-------------|------------|
| MS, Cybersecurity (GPA 3.9) | graduated May 2024 | Pace University, Seidenberg School of CSIS, New York, NY | Network security, incident response, penetration testing, computer & mobile forensics, cloud security, application security, vulnerability management, risk management & assessment, ISO frameworks, cryptography, Linux, SQL, Python automation |
| BS, Cybersecurity and Information Technology (GPA 3.8) | graduated May 2022 | Gujarat University, Gujarat, India | |

## Professional Experience

### Founder & Security Engineer - ResilAI (Feb 2026 - Present)
- Architected and launched ResilAI (AIRS), an AI incident readiness platform. Its custom deterministic pre-inference safety filter ("Logic Firewall"), deployed on GCP Cloud Run, achieves a 99.2% pre-ingestion block rate across 500+ adversarial payloads (MITRE ATLAS AML.T0031).
- Built an automated adversarial evaluation harness integrating Garak, Microsoft PyRIT and Promptfoo to stress-test LLM defenses against prompt injection, jailbreaks, and SSRF / IMDSv2 exploits.

### Cybersecurity Engineer (Detection & Response) - Filmy AI (Aug 2024 - Feb 2026)
⚠ Title appears as "Cybersecurity Engineer (Detection & Response)" (2 resumes), "Cybersecurity Engineer" (1), "Security Lead & Cybersecurity Engineer" (1). Do not use "Security Lead" until confirmed.
- Accelerated detection-to-containment (MTTD/MTTR) by 30% across 50+ security events/incidents by engineering automated SIEM correlation rules, log analytics, and behavioral anomaly-detection dashboards.
- Reduced manual analyst triage workload by 40% with Python and SQL automation for log extraction, event parsing, and recurring threat-intelligence reporting.
- Decreased AWS cloud attack surface by 40% (IAM, WAF, S3, CloudTrail) by enforcing least-privilege access, automated S3 encryption, and WAF protections.
- Ran security awareness training for 20+ employees, reducing phishing risk by 15%.
- Wrote Python scripts to test the website and database for security vulnerabilities.
- Built a back-end SQL database (jobs, customers, users) with queries to track user sessions and analyze behavioral patterns and web traffic.

### Cyber Security Intern - Bunchful (Mar 2024 - May 2024)
⚠ Resumes disagree on scope: "conducted penetration testing on 5+ websites" (1 resume) vs "analyzed penetration test reports and vulnerability data" (1) vs "analyzed 10+ web application incidents" (2). Conservative wording until confirmed:
- Analyzed penetration-test reports, vulnerability data and 10+ web application incidents; converted findings into remediation guidance for developers, contributing to a 10% reduction in client vulnerabilities.
- Authored 10+ structured security reports (vulnerabilities, remediation steps, best practices) used for compliance and risk reviews.

### IT Security and Systems Intern - GAOTek (Dec 2023 - Mar 2024)
- Researched potential vulnerabilities on 10+ product pages daily, contributing to security assessments.
- Improved technical documentation and troubleshooting recommendations, cutting support tickets by 20%.
- Developed and updated 5+ technical documents per week for IT audit, supporting compliance with industry standards.

### Digital Forensics & Incident Response Analyst - Cod-Ingenuity (Feb 2021 - Mar 2023)
⚠ Title appears as "Digital Forensics and Incident Response Analyst" (2 resumes), "Web Security Specialist" (1), "Digital Forensics Analyst (Projects)" (1). Full-time vs part-time (overlaps BS until May 2022) unconfirmed. Duties as stated across resumes, all ⚠ until confirmed:
- Real-time monitoring of network and endpoint security events with CrowdStrike Falcon and Cisco firewall logs; deployed CrowdStrike Falcon and BitLocker, contributing to a 25% reduction in security incidents.
- Log correlation and analysis across database, server and application logs in Windows and Linux environments.
- Forensic analysis in 20+ DFIR/security engagements across desktops, mobile devices and networks; preserved evidence and produced reports supporting insider-threat and malware investigations; worked with legal, IT and business stakeholders.
- Implemented and managed Cisco firewalls in line with PCI DSS; configured ACLs via cPanel.
- Database security assessments with SQL to detect SQL injection; Python scripts (with a colleague) to automate brute-force and firewall-strength testing of client websites.

## Independent Projects
- **NextGen Risk Register** (Nov 2026 - present) - github.com/purvanshbhatt/nextgen-risk-register. Open-source GRC risk register (Python, FastAPI, SQLite): 5x5 scoring + FAIR-style Monte Carlo (ALE, P90 loss, loss-exceedance curves vs per-category risk appetite); residual risk from controls weighted by evidence tier (self-declared / scanner-observed / SIEM-verified); 14 threat scenarios mapped to NIST CSF 2.0, ISO 27001:2022, SOC 2, NIST AI RMF, OWASP LLM Top 10, MITRE ATT&CK/ATLAS; RBAC for four personas, SHA-256 hash-chained audit trail, time-boxed risk acceptances, KRI thresholds, printable board report; 69 automated tests.
- **AI Red Team Lab** (2025 - present) - automated red-teaming benchmark suites (Garak, PyRIT, Promptfoo) for jailbreaks, prompt injection and credential exfiltration; failure modes converted into deterministic Logic Firewall rules.
- **OriginTrace / patchproof** (2024 - present) - LLM-driven patch loop that iterates against reproducible exploits in sandboxed containers until the exploit is provably blocked; CLI published on PyPI and npm.
- **cloud-forensic-snapshot** (2024 - present) - cloud IR automation capturing volatile memory and /proc artifacts for Volatility 3; enforces STS session revocation (aws:TokenIssueTime) on AWS EC2/IAM.
- **Security Vulnerability Scanner** (Jan 2023 - present) - co-developed Python scanner detecting 100+ OS and web vulnerabilities; cut manual assessment time 90%; OWASP Top 10 prioritization.
- **Web Reconnaissance Dashboard** - cloud-based recon dashboard integrating Nmap and Sublist3r; findings mapped to MITRE ATT&CK and OWASP Top 10 with plain-language risk narratives.
- **Dark Web Research Project** (Jan - May 2023, Pace) - team of three; built an OnionShare site and a guide for dismantling illegal dark-web sites (supervised by Dr. Alexander Tsekhansky).
- **Data Lineage Mapping for User Authentication** (Jan - May 2022) - mapped auth data flows across web server, auth DB and logging; SQL feature engineering for an SVM network-intrusion model (+30% accuracy).

## Technical Skills

### Security
- **Detection & response:** SIEM correlation rules, log analytics, threat hunting, anomaly detection, incident triage and handling, MTTD/MTTR improvement
- **Cloud security:** AWS (IAM, WAF, S3, CloudTrail, EC2, STS), Azure, GCP Cloud Run
- **AI/LLM security:** Garak, Microsoft PyRIT, Promptfoo, MITRE ATLAS, OWASP LLM Top 10, prompt-injection and jailbreak defense
- **Offensive / AppSec:** Nmap, Metasploit, Hydra, Hashcat, Wireshark, OWASP Top 10, SQL-injection testing
- **Endpoint / network:** CrowdStrike Falcon (EDR), IDS/IPS, Cisco firewalls, BitLocker, VPN
- **GRC:** NIST CSF 2.0, ISO 27001:2022, SOC 2, NIST AI RMF, FAIR, PCI DSS, MITRE ATT&CK
- ⚠ **Unconfirmed (one resume only):** Splunk, FTK, Autopsy, Magnet Axiom, Burp Suite, Jira, Confluence, SAP, Tableau, Looker

### Programming
- **Python** (security automation, FastAPI, data analysis), **SQL**, Bash, PowerShell, C++, JavaScript, HTML/CSS

### Platforms & Tools
- Kali Linux, Red Hat, Ubuntu, CentOS, Debian, Windows Server 2022 / Active Directory, macOS
- VMware, VirtualBox, GitHub, Anaconda, VS Code, LaTeX, MS Office 365, Google Workspace, SQL Server

## Certifications
- CompTIA CySA+
- CompTIA Security+
- CompTIA CSAP (Security Analytics Professional)
- OSCP - in progress
- Benchmarks: TryHackMe top 5% (Level 55), Hack The Box Level 4 Operator

## Publications
None.

## Awards
- **2024 MITRE Engenuity Embedded CTF (eCTF)** - Task Manager & Secure Designer (Jan-Apr 2024). Led a team of eight building a secure microcontroller system under strict constraints (1 s wake, 216 KB firmware); 25% performance gain through efficient hashing/encryption; identified and mitigated 7 vulnerabilities using MITRE ATT&CK.

## References
Available upon request.
