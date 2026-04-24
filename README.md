# incident-response-playbook
Incident Response Playbook for Brute Force Attack (SOC Analyst Project)


This repository contains an Incident Response Playbook for detecting and handling cybersecurity incidents.

## 📌 Project Overview
This project demonstrates how a SOC Analyst responds to a brute-force attack using structured incident response steps.

##  Objective
To identify, analyze, contain, and recover from brute-force login attacks.

## 🛠️ Tools Used
- Splunk (SIEM)
- Linux Logs (/var/log/auth.log)
- Firewall (iptables)

## Incident Response Process
1. Detection
2. Analysis
3. Containment
4. Eradication
5. Recovery
6. Lessons Learned

## 📂 Playbook
👉 [Brute Force Attack Playbook](playbooks/brute_force_attack.md)

##  Splunk Screenshots
<img width="1488" height="894" alt="Splunk" src="https://github.com/user-attachments/assets/f626ce33-5b81-4097-b20a-0b98ec108aa7" />

##  Detection & Analysis
###  1. Raw Log Detection
- Query: index=main "Failed password"
<img width="1142" height="895" alt="raw_logs png" src="https://github.com/user-attachments/assets/40b0246f-a83f-43ff-bbcd-8f64c72c9054" />
###   2. Attacker IP Analysis
- Query: index=main "Failed password"
  | rex "from (?<ip>\d+\.\d+\.\d+\.\d+)"
  | stats count by ip
<img width="1148" height="561" alt="ip_analysis" src="https://github.com/user-attachments/assets/ef7fb171-e55d-4f0a-b12d-69acc2af9fd0" />
###   3. Attack Trend Over Time
- Query: index=main "Failed password"
  | timechart count
<img width="1145" height="680" alt="timechart" src="https://github.com/user-attachments/assets/5b95f2a4-c3f8-4160-8b93-faa0dc64c438" />


##  Skills Gained
- Incident Response
- Log Analysis
- SIEM Monitoring

---
 This project is part of my cybersecurity learning journey.
