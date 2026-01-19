
# Brute Force Login Alert – SOC L1 Playbook

## Alert Description
Multiple failed authentication attempts detected within a short time window,
originating from a single source or targeting multiple accounts.

---

## Log Sources
- Windows Security Event ID 4625
- Linux /var/log/auth.log
- VPN / Firewall authentication logs

---

## Investigation Steps
1. Count number of failed login attempts
2. Identify source IP address
3. Check IP geolocation and reputation
4. Determine if targeted account exists
5. Check for successful login after failures

---

## Sample Log
Event ID: 4625
Account Name: admin
Failure Reason: Bad password
Source IP: 185.xxx.xxx.xxx


---

## False Positive Indicators
- User typed incorrect password
- Service account misconfiguration
- VPN reconnect behavior

---

## True Positive Indicators
- High-volume attempts in short duration
- Multiple usernames targeted
- Malicious IP reputation
- Successful login after failures

---

## Response Actions
- Reset affected account password
- Recommend blocking source IP
- Escalate if compromise is suspected

---

## MITRE ATT&CK Mapping
- T1110 – Brute Force
