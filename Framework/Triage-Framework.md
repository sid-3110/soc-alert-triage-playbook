# SOC L1 Alert Triage Framework

## Purpose
This document defines the standard alert triage framework followed by a
Security Operations Center (SOC) Level 1 analyst.

The framework is designed to ensure consistent, structured, and efficient
handling of security alerts across endpoint, identity, email, and network
domains.

---

## Scope of Alerts Covered
This framework applies to, but is not limited to, the following alert types:

- Brute Force Login Attempts
- Malware / Suspicious Process Execution
- Phishing Email Attacks
- Suspicious Login / Impossible Travel
- Active Directory Attacks
- DDoS (Distributed Denial of Service) Attacks

---

## 1. Alert Intake
The SOC L1 analyst begins by gathering initial alert details:

- Alert name and unique ID
- Severity level (Low / Medium / High)
- Detection timestamp (UTC)
- Affected user, host, IP, or service
- Alert source (SIEM, EDR, Email Gateway, Firewall, IDS/IPS)

---

## 2. Initial Validation
The analyst validates whether the alert may represent expected or benign
behavior.

Key questions:
- Is the activity expected for this user or system?
- Has this alert been observed previously?
- Is the affected asset business-critical?
- Is there a known maintenance or approved change?

---

## 3. Investigation & Analysis
If suspicious activity is identified, the analyst performs deeper analysis:

- Review relevant logs and telemetry
- Correlate with related alerts or events
- Identify Indicators of Compromise (IOCs)
- Check IP, domain, or file reputation
- Analyze behavior patterns and timelines

---

## 4. Classification & Decision
Each alert must be classified with clear justification as one of the following:

- **False Positive** – Benign and expected behavior
- **True Positive (Benign)** – Policy violation without malicious intent
- **True Positive (Malicious)** – Confirmed or highly suspected attack

Evidence must support the classification.

---

## 5. Response Actions
Based on alert severity and analyst permissions:

- Close alert with documented reasoning
- Perform initial containment (if allowed)
- Recommend remediation actions
- Notify affected users or teams if required

---

## 6. Escalation Criteria
Alerts must be escalated to SOC L2 or Incident Response when:

- Successful compromise is confirmed
- Privileged or domain accounts are involved
- Malware execution is validated
- Lateral movement is suspected
- Business-critical services are impacted (e.g., DDoS)

---

## Severity Levels & SLA

| Severity | Description | Expected Action | SLA |
|--------|------------|----------------|-----|
| Low | Informational or expected behavior | Document and close | 24 hours |
| Medium | Suspicious activity | Investigate and validate | 8 hours |
| High | Confirmed or likely compromise | Immediate escalation | 1 hour |

---

## Documentation Requirements
Every alert investigation must include:

- Alert summary
- Logs reviewed
- Evidence (screenshots, log excerpts)
- Final classification decision
- Actions taken or recommended
- Analyst name and timestamp

---

## Analyst Responsibilities
- Remain calm and methodical under pressure
- Follow defined triage procedures
- Validate before escalating
- Maintain accurate and complete documentation
- Communicate clearly with senior analysts and teams

---

## Framework Objective
This framework ensures that SOC L1 analysts handle alerts consistently,
reduce false positives, and escalate genuine threats efficiently while
supporting overall security operations.
