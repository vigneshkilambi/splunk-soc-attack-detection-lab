# 👨‍💻 Vignesh Kilambi

### 🚨 SOC Home Lab: Attack Simulation & Detection

This project demonstrates a real-world cyber attack simulation using **Kali Linux** and detection using **Splunk SIEM** with **Sysmon logs**.

---

## 🏗️ Lab Architecture

The lab consists of:

* **Kali Linux (Attacker)**
* **Windows Machine (Target)**
* **Splunk SIEM (Monitoring & Detection)**
* **Sysmon (Log Collection)**

![Architecture](images/architecture.png)

---

## ⚔️ Attack Simulation

An attacker machine (Kali Linux) performed reconnaissance using an **Nmap scan** on the target system.

### 🔹 Command Used:

```
nmap -sT <target-ip>
```

### 🔹 Outcome:

* Identified open ports on the target machine
* Generated network activity logs

![Nmap Attack](images/nmap_attack.png)

---

## 🔍 Detecting Attacker Activity (Sysmon Logs)

Sysmon Event ID **3 (Network Connection)** was analyzed in Splunk to detect communication between attacker and victim.

### 🔹 Key Findings:

* Source IP → Attacker (Kali Linux)
* Destination IP → Target (Windows)
* Network connection successfully captured

![Sysmon Logs](images/sysmon_network.png)

---

## 🚨 Brute Force Attack Detection

Multiple failed login attempts were detected using Windows Security logs (**Event ID 4625**).

### 🔹 Detection Query:

```spl
index=wineventlog EventCode=4625
| stats count by Account_Name, Source_Network_Address
| where count > 5
```

### 🔹 Analysis:

* Repeated failed login attempts observed
* Suspicious behavior identified as brute-force attack

![Brute Force Detection](images/brute_force_detection.png)

---

## 🛠 Tools Used

* Splunk SIEM
* Sysmon
* Kali Linux
* Nmap
* Windows Event Logs

---

## 📁 Project Structure

```
splunk-soc-attack-detection-lab/
│── images/
│── queries/
│── detections/
│── logs/
│── reports/
│── project-files/
```

---

## 📊 Outcome

* Simulated real-world cyber attack scenario
* Detected attacker activity using SIEM
* Identified brute-force login attempts
* Performed log analysis and investigation

---

## 🎯 Skills Gained

* SIEM Monitoring (Splunk)
* Log Analysis (Sysmon & Windows Logs)
* Threat Detection
* Incident Investigation
* Basic Blue Team Operations

---

## 📌 Author

**Vignesh Kilambi**
Aspiring SOC Analyst
