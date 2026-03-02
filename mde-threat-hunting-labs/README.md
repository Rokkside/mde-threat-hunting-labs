🔎 Microsoft Defender for Endpoint – Threat Hunting Labs










📌 Overview

This repository contains structured threat hunting labs conducted in Microsoft Defender for Endpoint (MDE).

The objective of this project is to simulate real-world SOC detection workflows using:

Hypothesis-driven hunting

KQL-based telemetry analysis

Brute-force detection techniques

MITRE ATT&CK mapping

Incident triage and response recommendations

Cloud-based Git workflow (EC2 → GitHub via SSH)

Each lab scenario mirrors practical blue-team investigative processes used in enterprise environments.

🧠 Skills Demonstrated

Advanced Hunting (KQL)

Log correlation & pattern analysis

Brute-force detection logic

MITRE ATT&CK technique mapping

Detection engineering mindset

Incident response workflow

Secure Git authentication via SSH

Cloud-based development workflow (AWS EC2)

🗂 Lab Structure
mde-threat-hunting-labs
│
├── scenario-1-internet-exposed-vm
│   ├── README.md
│   ├── queries/
│   └── screenshots/
│
└── (Future Scenarios)
🔬 Current Scenarios
1️⃣ Internet-Exposed VM – Brute Force Detection

Focus:

Identify internet-exposed virtual machines

Detect excessive failed logon attempts

Correlate failed → successful authentication events

Investigate potential brute-force success

Mapped Techniques:

Tactic	Technique	ID
Initial Access	Brute Force	T1110
Credential Access	Valid Accounts	T1078
Initial Access	External Remote Services	T1133

📂 Location:

scenario-1-internet-exposed-vm/
🔐 Methodology

Each hunt follows a structured approach:

Preparation (Hypothesis Development)

Data Collection (Telemetry Validation)

Data Analysis (KQL Investigation)

Threat Validation

MITRE Mapping

Response Planning

Security Improvement Recommendations

🏗 Environment

Windows VM (Lab target)

Microsoft Defender for Endpoint

Advanced Hunting (KQL)

AWS EC2 (Git workflow)

GitHub (SSH authenticated)

All sensitive identifiers in screenshots are redacted.

🚀 Future Labs (Planned)

Remote Code Execution Detection

Lateral Movement Investigation

Suspicious PowerShell Execution

Persistence Mechanism Detection

Credential Dumping Activity Hunt

RDP Abuse & Account Lockout Analysis

🎯 Objective

This project is designed to:

Demonstrate real SOC investigative methodology

Showcase detection engineering capability

Build portfolio-ready blue team documentation

Strengthen KQL fluency

Align hunting activity with MITRE ATT&CK

📬 Contact

Orok Ironbar
Cybersecurity | Threat Hunting | Detection Engineering

🔥 What This Repo Signals to Recruiters

Structured thinking

Log-driven analysis

Security framework awareness

Practical Microsoft Defender experience

Cloud-native workflow discipline

🚀 Next Step

After pasting this into your root README.md, run:

git add README.md
git commit -m "Add professional root README"
git push
