# 1-SOAR-Automation: Automated Incident Response Playbook Design

## Project Overview
This project documents a comprehensive investigation and engineering response to a critical incident involving a persistent, suspicious Proxy Authentication pop-up detected on a corporate Windows endpoint. The goal was to move beyond manual triage to design a scalable, automated solution.

## Key Focus Areas

### 1. Root Cause Analysis (RCA)
* **Initial Triage:** Utilized DNS analysis (`nslookup`) and OSINT (VirusTotal) to investigate the suspicious domain (`trout-west-1-us.maxxxcdn.com`).
* **Discovery:** Identified the root cause as a Potentially Unwanted Program (PUP) disguised as a browser extension ("Free VeePN") attempting to force network traffic through an unauthorized external proxy.

### 2. SOAR Playbook Development
A critical outcome was the design of a **4-Step SOAR Playbook** to ensure immediate and global remediation, significantly improving the security posture and **reducing the Mean Time To Resolution (MTTR)**.

| Step | Action (Automation) | Engineering Value Added |
| :---: | :--- | :--- |
| **1** | Context Enrichment (Threat Intel Lookup) | Reduces manual lookup time and increases analyst confidence. |
| **2** | Global Network Containment (Firewall/Proxy) | Prevents all other users from connecting to the malicious C2/Proxy IP. |
| **3** | Endpoint Remediation (EDR/MDM Command) | Mass uninstallation of the malicious extension across all corporate machines instantly. |
| **4** | Case Management & Auto-Closure | Automates documentation and significantly lowers the MTTR metric. |

## 🛠️ Skills Demonstrated

* **Automation:** SOAR Playbook Design, Workflow Logic, Integration with Security Controls.
* **Incident Response:** Structured Triage, Root Cause Analysis (RCA).
* **Networking:** DNS Verification, Proxy Configuration Analysis.
* **Endpoint Security:** Identifying and remediating PUPs via EDR/MDM actions.

---
[**View Full SOC Engineering Report (PDF)**](01_SOC-Engineer_Proxy-Auth-Automation-Report.pdf)
