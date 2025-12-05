# 2-Network-Forensics-LLMNR: Incident Analysis of Credential Harvesting

## Project Overview
This project involved a detailed **Network Forensics** investigation into a simulated **LLMNR/NBT-NS Poisoning** incident. The primary goal was to analyze captured network traffic (PCAP file) using Wireshark to identify the attacker, compromised accounts, and potential mitigation strategies.

## Key Investigation Steps

| Step | Technique / Tool Used | Outcome / Findings |
| :---: | :--- | :--- |
| **1** | Wireshark Filtering (LLMNR & IP) | Identified the initial **mistyped query** (`fileshaare`) that triggered the attack. |
| **2** | Rogue Machine Identification | Successfully identified the **rogue machine's IP address** (`192.168.232.215`) replying to the poisoned query. |
| **3** | Credential Extraction (SMB2) | Filtered for SMB2 protocol to expose the user account that was compromised: **`janesmith`**. |
| **4** | Mitigation Design | Proposed network and host-based strategies to disable or restrict the use of LLMNR/NBT-NS protocols to prevent credential harvesting. |

## 🛠️ Skills Demonstrated

* **Network Forensics:** Deep packet inspection and traffic analysis using **Wireshark**.
* **Protocol Analysis:** Understanding the exploitation vector of Link-Local Multicast Name Resolution (LLMNR) and NetBIOS Name Service (NBT-NS).
* **Incident Response:** Identifying affected scope, attacker infrastructure, and compromised user data.
* **Defense Strategy:** Designing effective mitigation and hardening policies.

---
[**View Full Incident Analysis Report (PDF)**](Incident%20Analysis%20Mitigating%20LLMNRNBT%20NS%20Poisoning%20&%20SMB%20Credential%20Harvesting.pdf)
