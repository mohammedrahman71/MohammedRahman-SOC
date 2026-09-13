# RahmanMohammed-SOC

## 👨‍💻 About Me

I am building hands-on experience in cybersecurity and Security Operations Center (SOC) analysis through practical home lab projects.

My current focus is learning how to monitor security events, investigate alerts, analyze logs, identify vulnerabilities, and understand security incidents.

## 🛡️ Cybersecurity Skills

* Wazuh SIEM
* Splunk
* Linux / Ubuntu
* Kali Linux
* Windows 11
* Log Analysis
* Security Alert Investigation
* File Integrity Monitoring (FIM)
* Vulnerability Detection
* MITRE ATT&CK
* Nmap
* Basic Firewall Configuration

## 🔎 Featured Project

### Wazuh SOC Home Lab

Built a home SOC lab using Wazuh Manager on Ubuntu and a Windows 11 endpoint.

**Activities:**

* Installed and configured Wazuh Manager
* Connected Windows 11 as a Wazuh Agent
* Monitored security alerts
* Investigated Rule IDs and alert severity
* Investigated file integrity events
* Reviewed CVE vulnerability alerts
* Analyzed agent information, IP addresses, and log events
* Used MITRE ATT&CK information during alert investigation

### Rule 550 Alert Investigation

Investigated a Wazuh File Integrity Monitoring alert involving:

`/usr/bin/ps`

The alert reported:

**Rule ID:** 550
**Rule Level:** 7
**Event:** File modified
**Description:** Integrity checksum changed

The investigation included checking:

* File ownership and permissions
* File timestamps
* File hashes
* Package ownership
* Package verification
* Ubuntu package installation history

The investigation indicated that the file change was likely associated with a legitimate `procps` package update.

## 📊 Splunk Home Lab

Practicing:

* Searching security logs
* Understanding Splunk alerts
* Using SPL
* Investigating security events
* Reviewing system activity

## 🐧 Kali Linux Lab

Practicing:

* Linux command-line fundamentals
* Nmap
* Network discovery
* Firewall configuration
* Security testing in authorized lab environments
* Metasploitable security lab

## 📚 Currently Learning

* SOC Analyst fundamentals
* SIEM monitoring
* Incident investigation
* Network security
* Vulnerability management
* Linux security
* Windows security
* MITRE ATT&CK
* Log analysis

## 🎯 Career Goal

My goal is to develop practical cybersecurity and SOC Analyst skills through hands-on labs and real-world security investigation techniques.

---

**This repository documents my cybersecurity learning journey and hands-on projects.**
