# 4-KQL-Detection-Engineering: Spear-Phishing & Data Exfiltration Threat Hunt

## Project Overview
This project showcases a full-cycle **Threat Hunting** exercise using **KQL (Kusto Query Language)** within a SIEM environment (KC7/Chronicle simulation). The investigation focused on exposing a targeted spear-phishing campaign that resulted in account compromise and successful **Data Exfiltration**.

## KQL Investigation Chain

| Step | KQL Pivot / Table Used | Goal / Finding |
| :---: | :--- | :--- |
| **1** | Web Logs (URL table) | Identified initial reconnaissance by the attacker's IP (`18.66.52.227`) to gather sensitive OSINT for password reset. |
| **2** | PassiveDNS Table | Pivoted from the attacker's IP to confirm the malicious phishing domain: **`betterlyrics4u[.]com`**. |
| **3** | Email Logs / Employees Join | Confirmed the phishing campaign was **targeted** by showing that only specific job roles (Rappers) received the malicious emails. |
| **4** | Authentication & Inbound Network Logs | Confirmed successful login and tracked the final stage: **Data Exfiltration** via suspicious URL parameters involving a `.zip` file transfer. |

## 🛠️ Skills Demonstrated

* **Threat Hunting:** Structured, iterative investigation methodology using KQL.
* **KQL Proficiency:** Advanced use of joins, pivots, and filtering across multiple log sources (Email, Web, DNS).
* **Detection Engineering:** Understanding the full attack lifecycle (Recon -> Compromise -> Exfiltration).
* **Security Posture:** Highlighting the critical failure of Operational Security (OPSEC) as the initial vulnerability.

---
[**View Full Detection Engineering Report (PDF)**](Detection%20Engineering%20KQL%20Rules%20for%20Spear%20Phishing%20&%20Data%20Exfiltration%20Analysis.pdf)
