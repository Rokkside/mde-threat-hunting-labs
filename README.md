# Microsoft Defender for Endpoint (MDE) Threat Hunting Labs

Enterprise-grade threat detection and response labs built using Microsoft Defender for Endpoint (MDE), focused on detection engineering, MITRE ATT&CK mapping, and incident response workflows.

---

## 📖 Overview

This repository contains hands-on threat hunting and detection engineering labs performed in a controlled environment using Microsoft Defender for Endpoint (MDE).

Each lab simulates realistic attack behavior, builds custom detection logic using Kusto Query Language (KQL), and validates automated response actions.

These labs mirror real-world SOC workflows including:

- Threat simulation
- Telemetry validation
- Custom detection rule creation
- Automated containment
- Incident investigation
- Root cause analysis
- Remediation and cleanup

---

## 🧠 Objectives

- Develop practical detection engineering skills
- Strengthen KQL query writing proficiency
- Understand MDE telemetry sources
- Map adversary behavior to MITRE ATT&CK
- Practice automated response (device isolation, investigation packages)
- Build documented, reproducible SOC lab scenarios

---

## 🏗 Lab Architecture

<img width="482" height="268" alt="Screenshot 2026-03-02 at 10 47 00 AM" src="https://github.com/user-attachments/assets/79b158a5-4a64-40d4-8ab8-d58ee69295bd" />

---

## 🧪 Lab Scenarios

### 🔹 Scenario 1: Internet-Exposed VM with Simulated RCE

Simulates a Windows VM exposed to the internet with firewall disabled for controlled threat emulation.

**Attack Simulation:**
- PowerShell-based execution activity
- Suspicious process execution patterns
- Command-line behavioral indicators

**Detection Engineering:**
- Custom KQL rule creation
- Behavioral filtering logic
- Alert tuning

**Response Validation:**
- Automated device isolation
- Investigation package collection
- Incident timeline analysis

**MITRE ATT&CK Mapping:**
- T1059 – Command and Scripting Interpreter
- T1105 – Ingress Tool Transfer (if applicable)
- T1071 – Application Layer Protocol (if applicable)

---

## 🔍 Key Technologies Used

- Microsoft Defender for Endpoint (MDE)
- Kusto Query Language (KQL)
- Windows Event Logging
- PowerShell
- MITRE ATT&CK Framework
- AWS EC2 (Lab Hosting)
- Git / GitHub for version control

---

## 📂 Repository Structure

<img width="482" height="268" alt="Screenshot 2026-03-02 at 10 48 02 AM" src="https://github.com/user-attachments/assets/86888a6c-8b07-469e-9376-4a9943c70542" />


---

## 🛡 Skills Demonstrated

- Detection Engineering
- Threat Hunting
- Endpoint Telemetry Analysis
- Incident Response Workflow
- Adversary Behavior Mapping
- Security Documentation
- Cloud-hosted lab deployment

---

## 📊 Why This Matters

Modern SOC teams require engineers who can:

- Build detections from behavior, not signatures
- Understand telemetry deeply
- Reduce false positives
- Automate containment
- Translate activity into MITRE ATT&CK techniques

This lab environment demonstrates those competencies.

---

## 🚀 Future Labs (Planned)

- Persistence mechanism detection
- Lateral movement simulation
- Credential dumping detection
- Living-off-the-land binaries (LOLBins)
- Advanced KQL hunting queries
- Defender XDR correlation scenarios

---

## 📌 Author

Orok Ironbar  
Security Operations | Detection Engineering | Threat Hunting  

---

## ⚠️ Disclaimer

All attack simulations were performed in isolated lab environments for educational and defensive security research purposes only.

No production systems were targeted.

