# Wazuh SOC Home Lab

## 📌 Project Overview

This project documents my hands-on Security Operations Center (SOC) home lab using Wazuh.

The lab is designed to practice security monitoring, alert investigation, vulnerability detection, file integrity monitoring, and basic incident investigation.

## 🏗️ Lab Environment

| Component                | Configuration      |
| ------------------------ | ------------------ |
| SIEM / Security Platform | Wazuh              |
| Wazuh Manager            | Ubuntu 24.04.3 LTS |
| Endpoint                 | Windows 11         |
| Virtualization           | VMware Workstation |
| SIEM Dashboard           | Wazuh Dashboard    |

## 🛡️ What I Practiced

* Wazuh Manager installation and configuration
* Wazuh Agent deployment
* Windows endpoint monitoring
* Security alert investigation
* Rule ID and severity analysis
* File Integrity Monitoring (FIM)
* Vulnerability detection
* CVE investigation
* Agent and IP identification
* MITRE ATT&CK mapping
* Linux security commands
* Basic SOC investigation workflow

## 🔎 Rule 550 Investigation

### Alert Information

**Rule ID:** 550
**Rule Level:** 7
**Description:** Integrity checksum changed
**Event:** File modified
**File:** `/usr/bin/ps`

Wazuh File Integrity Monitoring detected changes to the file.

### Investigation

I investigated the alert using Linux commands including:

```bash
dpkg -S /usr/bin/ps
dpkg -V procps
apt-cache policy procps
grep -i "procps" /var/log/dpkg.log
stat /usr/bin/ps
```

The investigation checked:

* File ownership
* File permissions
* File timestamps
* Inode information
* MD5/SHA1/SHA256 checksums
* Package ownership
* Package verification
* Package installation history

### Finding

The investigation showed that `/usr/bin/ps` is provided by the `procps` package.

The file's current creation/change time correlated with a legitimate `procps` package update.

**Conclusion:** The alert was likely caused by a legitimate package update rather than confirmed malicious activity.

## 🎯 SOC Investigation Workflow

1. Identify the alert.
2. Check the Rule ID and severity.
3. Identify the affected agent.
4. Identify the affected file or event.
5. Examine timestamps and file attributes.
6. Check hashes and package information.
7. Review system logs.
8. Determine whether the activity appears legitimate or suspicious.
9. Document the findings.

## 📚 Lessons Learned

This investigation helped me understand how a SOC analyst can use Wazuh File Integrity Monitoring to detect changes to important system files and then investigate whether the change is legitimate or suspicious.

## 🚀 Future Improvements

* Add more Windows and Linux agents
* Create additional Wazuh detection scenarios
* Practice authentication and brute-force detection in an authorized lab
* Integrate additional log sources
* Continue practicing MITRE ATT&CK mapping
* Document additional incident investigations
