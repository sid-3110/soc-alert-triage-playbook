# Suspicious Login / Impossible Travel – SOC L1 Playbook

## Alert Description
A user login was detected from geographically distant locations within a short
time frame, indicating potential credential compromise.

---

## Log Sources
- Identity and Access Management (IAM) logs
- Cloud authentication logs (Azure AD, Google, AWS)
- VPN authentication logs

---

## Investigation Steps
1. Review login timestamps
2. Compare IP geolocations
3. Identify device and user-agent
4. Check historical login behavior
5. Verify if MFA was enabled or bypassed

---

## Sample Log
User: john.doe
Login IP: 91.xxx.xxx.xxx (Germany)
Previous Login IP: 103.xxx.xxx.xxx (India)
Time Difference: 20 minutes


---

## False Positive Indicators
- Corporate VPN usage
- Mobile network IP changes
- User traveling internationally

---

## True Positive Indicators
- Logins from different countries within minutes
- New or unknown device fingerprint
- MFA fatigue or bypass attempts
- Other suspicious activity on the account

---

## Response Actions
- Force password reset
- Invalidate active sessions
- Enable or enforce MFA
- Escalate to SOC L2

---

## MITRE ATT&CK Mapping
- T1078 – Valid Accounts

