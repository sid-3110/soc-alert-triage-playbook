# MITRE ATT&CK Mapping – SOC Alert Triage Playbooks

This document maps each SOC alert triage playbook in this repository to
relevant MITRE ATT&CK techniques. The purpose is to demonstrate alignment
with industry-standard threat modeling and SOC detection practices.

---

## Brute Force Login Attempts
**Description:** Repeated authentication attempts to guess credentials.

**MITRE Techniques:**
- T1110 – Brute Force

---

## Malware / Suspicious Process Execution
**Description:** Execution of malicious or suspicious processes on endpoints,
often through user interaction or scripting.

**MITRE Techniques:**
- T1059 – Command and Scripting Interpreter
- T1204 – User Execution

---

## Phishing Email Attacks
**Description:** Social engineering attacks attempting to trick users into
revealing credentials or executing malicious payloads.

**MITRE Techniques:**
- T1566 – Phishing

---

## Suspicious Login / Impossible Travel
**Description:** Logins detected from geographically distant locations in a
short time period, indicating potential credential compromise.

**MITRE Techniques:**
- T1078 – Valid Accounts

---

## Active Directory Attacks
**Description:** Abuse of Active Directory accounts and privileges, including
password spraying, brute force, and unauthorized privilege escalation.

**MITRE Techniques:**
- T1110 – Brute Force
- T1078 – Valid Accounts
- T1068 – Privilege Escalation

---

## DDoS Attacks
**Description:** Network-level attacks intended to disrupt availability by
overwhelming services or infrastructure with excessive traffic.

**MITRE Techniques:**
- T1498 – Network Denial of Service

---

## Why MITRE Mapping Matters in a SOC
MITRE ATT&CK mapping helps SOC teams:
- Understand attacker behavior patterns
- Align alerts with standardized techniques
- Improve detection coverage and response consistency
- Communicate incidents effectively across teams

---

**Maintained by:** Siddharth  
**Role:** SOC Analyst (Entry-Level Portfolio Project)
