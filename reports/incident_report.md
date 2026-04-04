# Incident Report: Attack Simulation & Detection

## 📝 Summary
A simulated cyber attack was performed using Kali Linux against a Windows machine. The activity was monitored and analyzed using Splunk SIEM and Sysmon logs.

## ⚔️ Attack Details
- Tool Used: Nmap
- Attacker Machine: Kali Linux
- Target Machine: Windows System
- Activity: Network scanning and login attempts

## 🔍 Detection

### 1. Network Activity
- Sysmon Event ID 3 captured connections between attacker and victim
- Attacker IP identified from logs

### 2. Brute Force Detection
- Multiple failed login attempts detected (Event ID 4625)
- Suspicious login pattern observed

## 📊 Findings
- Attacker IP successfully identified
- Network activity traced using logs
- Brute-force behavior detected

## ✅ Conclusion
The lab successfully demonstrates how SOC analysts detect and investigate attacks using SIEM tools like Splunk.

## 🎯 Skills Gained
- Log Analysis
- SIEM Monitoring (Splunk)
- Threat Detection
- Incident Investigation
