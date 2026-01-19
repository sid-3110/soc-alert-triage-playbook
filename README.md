# SOC Alert Triage Playbook (SOC L1)

This repository demonstrates **real-world SOC Level 1 alert triage workflows**
based on common security incidents observed in enterprise environments.

The project focuses on **alert validation, investigation steps, false-positive
analysis, MITRE ATT&CK mapping, and escalation decisions**, independent of any
specific SIEM or security tool.

---

## 🎯 Objective
To showcase how a SOC L1 analyst investigates and triages different types of
security alerts using structured playbooks and industry-standard practices.

---

## 🚨 Alerts Covered

- Brute Force Login Attempts  
- Malware / Suspicious Process Execution  
- Phishing Email Attacks  
- Suspicious Login / Impossible Travel  
- **Active Directory Attacks (Password Spraying, Privilege Abuse)**  
- **DDoS (Distributed Denial of Service) Attacks**

---

## 🧠 Skills Demonstrated

- SOC Level 1 alert triage methodology
- Log analysis (Windows, AD, endpoint, network)
- Incident investigation & validation
- False positive vs true positive decision-making
- MITRE ATT&CK mapping
- Security documentation & escalation workflows

---

## 📁 Repository Structure

soc-alert-triage-playbook/
│
├── README.md
├── framework/
│ └── triage-framework.md
├── playbooks/
│ ├── brute-force.md
│ ├── malware.md
│ ├── phishing.md
│ ├── suspicious-login.md
│ ├── active-directory-attack.md
│ └── ddos-attack.md
├── docs/
│ └── mitre-mapping.md
└── images/
├── brute-force/
├── malware/
├── phishing/
├── suspicious-login/
├── active-directory/
└── ddos/

---

## 🧪 How to Use This Repository
Each playbook follows a consistent SOC L1 structure:
1. Alert description
2. Log sources
3. Investigation steps
4. False positive indicators
5. True positive indicators
6. Response & escalation actions
7. MITRE ATT&CK mapping

Screenshots included in the `images/` directory represent realistic examples
used for investigation and validation.

---

## 👤 Author
**Siddharth**  
SOC Analyst (Entry-Level)  
Cybersecurity Portfolio Project

---

## 📌 Note
This project is designed for **learning, interview preparation, and portfolio
demonstration purposes**, and does not simulate live attacks.

