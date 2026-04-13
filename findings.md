# 🔍 Technical Analysis

## 🧩 Initial Access

The infection chain started with the execution of a VBScript file from the user's temporary directory.

## ⚙️ Execution

The VBScript launched PowerShell using:

* ExecutionPolicy Bypass
* Hidden window
* No profile

## 🔐 Obfuscation

The script used:

* Base64 encoding
* XOR encryption

These techniques were used to hide:

* C2 domain
* configuration values

## 🌐 Command and Control (C2)

The malware establishes a TCP connection to a remote server, enabling bidirectional communication.

## 🧠 Functionality

The script behaves as a RAT with the following features:

* Execute shell commands remotely
* Capture screenshots
* Browse file system
* Upload and download files
* Collect system information

## 📡 Data Exfiltration

System data is serialized in JSON format and sent periodically to the C2 server.

## 🚨 Impact

The malware provides full control over the compromised endpoint.
