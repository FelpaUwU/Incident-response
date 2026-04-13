# 🛡️ PowerShell RAT Malware Analysis

## 📌 Overview

This project documents the analysis of a malicious PowerShell script identified as a Remote Access Trojan (RAT). The malware was executed through a VBScript dropper and used obfuscation techniques to evade detection.

---

## 🧠 Objectives

* Analyze malicious PowerShell behavior
* Identify command and control (C2) infrastructure
* Perform threat hunting across endpoints
* Extract Indicators of Compromise (IOCs)

---

## 🔍 Execution Chain

```text
wscript.exe
   ↓
malicious.vbs
   ↓
powershell.exe -ExecutionPolicy Bypass -WindowStyle Hidden
   ↓
malicious.ps1 (RAT)
   ↓
C2 Communication
```

---

## 🔍 Key Findings

* Obfuscation using Base64 and XOR
* Execution via PowerShell with evasion flags
* TCP communication with remote C2 server
* Full remote control capabilities

### Capabilities:

* Remote command execution
* Screenshot capture
* File browsing and exfiltration
* Payload download and execution
* System information collection

---

## 🌐 C2 Infrastructure

* Domain: `mastermrc2.kozow.com`

---

## 🛡️ Threat Hunting

Threat hunting was performed using:

* Microsoft Defender (KQL)
* CrowdStrike Falcon (event queries)

Focus areas:

* Domain communication
* PowerShell execution patterns
* Process chains (`wscript → powershell`)

---

## ⚠️ Disclaimer

This repository is for educational and research purposes only.
All sensitive data has been sanitized.

---

## 👨‍💻 Author

* Cybersecurity student | Blue Team & Threat Hunting
