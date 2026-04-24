
# 🚨 Brute Force Attack Playbook

##  Objective
This playbook provides steps to detect and respond to brute-force login attempts.

---

##  Detection
- Multiple failed login attempts
- Splunk alert triggered
- Logs from /var/log/auth.log

---

##  Analysis
- Identify source IP address
- Check targeted usernames
- Analyze login patterns

Example:
- IP: 192.168.1.10
- Username: admin
- Attempts: 50 in 2 minutes

---

##  Containment
- Block attacker IP using firewall
- Temporarily lock user account

---

##  Eradication
- Remove malicious scripts (if any)
- Reset compromised credentials

---

##  Recovery
- Restore normal access
- Monitor system logs

---
## 👨‍💻 Response Workflow

1. **Alert Detection**  
   The SOC Analyst receives an alert from Splunk indicating multiple failed login attempts.

2. **Initial Investigation**  
   The analyst reviews logs in Splunk to confirm suspicious activity and identify the source IP address.

3. **Analysis & Validation**  
   The analyst analyzes login patterns (frequency, usernames, timestamps) to verify a brute-force attack.

4. **Containment**  
   The malicious IP address is blocked using firewall rules, and affected user accounts are temporarily locked.

5. **Eradication**  
   Compromised credentials are reset, and any malicious activity or scripts are removed.

6. **Recovery**  
   Normal system operations are restored, and user accounts are securely re-enabled.

7. **Monitoring & Closure**  
   The system is continuously monitored for further suspicious activity, and the incident is documented and closed.


##  Lessons Learned
- Weak passwords increase risk
- No login attempt limits

## 🚨 Conclusion
This playbook demonstrates a structured approach to incident detection and response, simulating real-world SOC operations using Splunk.
