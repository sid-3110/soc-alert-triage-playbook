# Phishing Email Alert – SOC L1 Playbook

## Alert Description
An email has been flagged as suspicious due to potential phishing,
credential harvesting, or malicious attachment indicators.

---

## Alert Sources
- Email Security Gateway
- User-reported phishing emails

---

## Investigation Steps
1. Analyze sender email address and domain
2. Review email headers for spoofing
3. Inspect URLs and attachments
4. Check reputation of domains and links
5. Analyze email content for social engineering tactics

---

## Sample Indicators

From: security@micros0ft-support.com

Reply-To: attacker@evil-domain.com

URL: hxxp://login-verification[.]com


---

## False Positive Indicators
- Internal phishing simulation campaigns
- Legitimate external business partners
- Automated notification emails

---

## True Positive Indicators
- Lookalike or spoofed domains
- Urgent language requesting immediate action
- Credential harvesting pages
- Malicious attachments or shortened URLs

---

## Response Actions
- Quarantine or remove email from mailboxes
- Block sender domain and URLs
- Notify affected users
- Escalate if credentials were entered

---

## MITRE ATT&CK Mapping
- T1566 – Phishing
