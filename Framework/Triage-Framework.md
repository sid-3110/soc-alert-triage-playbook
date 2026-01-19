
# SOC L1 Alert Triage Framework

## Purpose
This document defines the standard alert triage workflow followed by a
Security Operations Center (SOC) Level 1 analyst.

The goal is to validate alerts, identify false positives, detect true threats,
and escalate confirmed incidents efficiently.

---

## 1. Alert Intake
The analyst begins by collecting basic alert details:

- Alert name and ID
- Severity level
- Timestamp (UTC)
- Affected user / host / IP
- Detection source (SIEM, EDR, Email Gateway, Firewall)

---

## 2. Initial Validation
The analyst determines whether the alert represents expected behavior.

Key questions:
- Is this activity normal for this user or system?
- Has this alert occurred before?
- Is the asset business-critical?

---

## 3. Investigation
If suspicious, deeper investigation is performed:

- Review relevant logs
- Correlate with other alerts
- Identify Indicators of Compromise (IOCs)
- Check IP/domain/file reputation

---

## 4. Decision Making
Each alert must be classified as one of the following:

- False Positive
- True Positive – Benign
- True Positive – Malicious

The decision must be supported with evidence.

---

## 5. Response & Escalation
Based on severity and impact:

- Close alert with documentation
- Contain threat if L1 permissions allow
- Escalate to SOC L2 when required

---

## Severity Levels & SLA

| Severity | Description | SLA |
|--------|------------|-----|
| Low | Informational | 24 hours |
| Medium | Suspicious activity | 8 hours |
| High | Confirmed compromise | 1 hour |

---

## Escalation Criteria
Escalate to SOC L2 when:

- Successful compromise is confirmed
- Malware execution is validated
- Privileged account is involved
- Lateral movement is suspected

---

## Analyst Responsibilities
- Remain calm and methodical
- Validate before escalating
- Document every action taken
- Follow process over assumptions
