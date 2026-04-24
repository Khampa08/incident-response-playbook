
# 🚨 Brute Force Attack Playbook

## 🎯 Objective
This playbook provides steps to detect and respond to brute-force login attempts.

---

## 🔍 Detection
- Multiple failed login attempts
- Splunk alert triggered
- Logs from /var/log/auth.log

---

## 🧠 Analysis
- Identify source IP address
- Check targeted usernames
- Analyze login patterns

Example:
- IP: 192.168.1.10
- Username: admin
- Attempts: 50 in 2 minutes

---

## 🛑 Containment
- Block attacker IP using firewall
- Temporarily lock user account

---

## 🧹 Eradication
- Remove malicious scripts (if any)
- Reset compromised credentials

---

## 🔄 Recovery
- Restore normal access
- Monitor system logs

---

## 📊 Lessons Learned
- Weak passwords increase risk
- No login attempt limits

### Improvements:
- Enable MFA
- Set account lockout policy
