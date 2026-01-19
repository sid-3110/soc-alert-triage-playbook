# Active Directory Attack Alert – SOC L1 Playbook

## Alert Description
Suspicious activity detected within Active Directory indicating potential
account abuse, password spraying, brute force, or unauthorized privilege
escalation.

---

## Common AD Attack Scenarios
- Password spraying against domain accounts
- Brute force on privileged users
- Unauthorized addition to privileged groups
- Abnormal authentication behavior on Domain Controllers

---

## Log Sources
- Windows Security Logs (Domain Controller)
- Event Viewer on DCs
- SIEM alerts correlated with AD logs

Key Event IDs:
- 4625 – Failed logon
- 4624 – Successful logon
- 4672 – Special privileges assigned
- 4728 – User added to privileged group

---

## Investigation Steps
1. Identify affected user account(s)
2. Review failed and successful login patterns
3. Check source IP addresses and geolocation
4. Verify recent group membership changes
5. Determine if activity aligns with user role

---

## Sample Logs
Event ID: 4728
Target Account: Domain Admins
Member Added: temp.user
Initiated By: svc-admin

---

## False Positive Indicators
- Legitimate IT administrative changes
- Approved maintenance or access requests
- Scheduled scripts or service accounts

---

## True Positive Indicators
- Multiple accounts targeted in short time
- Privileged group changes without change request
- Logins from unusual locations
- Activity outside business hours

---

## Response Actions
- Disable affected account(s)
- Revert unauthorized group changes
- Reset credentials
- Escalate immediately to SOC L2 / IR team

---

## MITRE ATT&CK Mapping
- T1110 – Brute Force
- T1078 – Valid Accounts
- T1068 – Privilege Escalation

