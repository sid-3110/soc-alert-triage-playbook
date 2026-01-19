# DDoS Attack Alert – SOC L1 Playbook

## Alert Description
A Distributed Denial of Service (DDoS) attack was detected based on abnormal
network traffic patterns overwhelming a service or network resource.

---

## Common DDoS Indicators
- Sudden spike in inbound traffic
- Large number of requests from multiple IPs
- Service performance degradation or outage
- IDS/IPS DDoS signatures triggered

---

## Log Sources
- Firewall logs
- IDS / IPS alerts
- Web server access logs
- Network monitoring tools

---

## Investigation Steps
1. Identify affected service or IP
2. Analyze traffic volume and protocol
3. Review source IP distribution
4. Check for known DDoS signatures
5. Confirm impact on availability

---

## Sample Log
Source IPs: Multiple
Destination IP: 203.xxx.xxx.xxx
Protocol: TCP SYN
Requests/sec: 50,000+



---

## False Positive Indicators
- Legitimate traffic spikes (marketing events)
- Internal vulnerability scans
- Load testing activities

---

## True Positive Indicators
- Sustained traffic from distributed IPs
- SYN flood or UDP flood patterns
- Service downtime or latency increase

---

## Response Actions
- Notify network / infrastructure team
- Enable rate limiting or firewall rules
- Coordinate with ISP or cloud provider
- Escalate to SOC L2 / NOC

---

## MITRE ATT&CK Mapping
- T1498 – Network Denial of Service
