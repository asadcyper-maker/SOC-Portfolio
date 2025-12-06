# 5-SharePoint-RCE-Webshell-Analysis: Advanced Incident Response & Host Forensics

## Project Overview
This project documents an advanced **Incident Response** case focused on the exploitation of a critical **SharePoint Vulnerability (CVE-2025-53770)**. The investigation traced the attacker's complex, multi-stage activity, which involved:
1.  Bypassing authentication via a crafted request.
2.  Deploying a **Webshell** for persistence.
3.  Utilizing **C# compilation (`csc.exe`)** to execute custom code (Living-off-the-Land technique).
4.  The final goal of extracting sensitive **cryptographic machine keys** for potential token forgery.

## Key Investigation Steps

| Step | Technique / Artifact Analyzed | Engineering Value Added |
| :---: | :--- | :--- |
| **1** | **Vulnerability Triage (CVE-2025-53770)** | Confirmed the initial unauthenticated POST request targeting the vulnerable SharePoint `ToolPane.aspx` endpoint. |
| **2** | **Execution Analysis (LotL)** | Identified the use of the native C# compiler (`csc.exe`) to compile a custom payload and successfully write a malicious ASPX webshell (`spinstall0.aspx`). |
| **3** | **Post-Exploitation & Data Theft** | Traced the final stage where a PowerShell command was executed to extract sensitive **cryptographic machine keys** from the server's configuration files. |
| **4** | **Detection Strategy** | Identified new detection gaps related to the abuse of native compiler tools (`csc.exe`) and patterns of sensitive data extraction, proving proactive detection skills. |

## 🛠️ Skills Demonstrated

* **Advanced Incident Response:** Structured investigation and tracing of multi-stage web exploitation and post-exploitation activity.
* **Web Forensics:** Analyzing HTTP traffic for webshell drops and unauthenticated exploit attempts.
* **Host Forensics:** Correlating process creation (PowerShell, `csc.exe`) with network logs to build the full timeline.
* **Vulnerability Analysis:** Understanding and documenting the impact of high-severity CVEs (CVSS 9.8) on critical enterprise infrastructure.
* **Malware Analysis:** Identifying the Webshell and its malicious intent (key extraction).

---
[**View Full Incident Response Report (PDF)**](./SharePoint_RCE_Webshell_IR_Report.pdf)
