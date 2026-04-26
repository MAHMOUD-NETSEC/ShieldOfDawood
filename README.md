# 🛡️ Shield of Dawood - Endpoint Security Detection Tool

<img width="1914" height="1037" alt="exp" src="https://github.com/user-attachments/assets/30bd0f3b-8251-441d-8320-1c48990e1d29" />

**Shield of Dawood** is a Windows-based defensive cybersecurity tool designed to actively detect and mitigate suspicious activity and common local network attacks. Built with a custom GUI, it serves as an endpoint defense solution that correlates network behavior to reduce incident validation time.

This repository provides:
* A precompiled Windows installer (via GitHub Releases)
* High-level documentation of the detection logic
* *(Note: Source code is intentionally not published to prevent malicious adaptation).*

---

## 🎯 Impact & Capabilities
* **False Positive Reduction:** Engineered advanced validation logic to correlate IP and MAC address relationships, drastically reducing false-positive alerts by approximately 40%.
* **Active Mitigation:** Features a custom GUI that integrates directly with Windows Firewall to actively detect and mitigate Man-in-the-Middle (MITM) network attacks.
* **Framework Alignment:** Mapped detection capabilities to the MITRE ATT&CK framework, generating actionable security alerts based on abnormal network behavior aligned with standard SOC methodologies.

---

## 🔍 Detection Logic Overview
The tool performs real-time monitoring and detection of the following attack types:
* **ARP Spoofing:** Detects IP–MAC address mismatches and flags unsolicited ARP replies.
* **DNS Spoofing:** Verifies DNS responses against the legitimate gateway and detects mismatched IP/MAC responses.
* **Rogue DHCP:** Identifies unauthorized DHCP offer packets and detects unexpected DHCP servers on the network.
* **ICMP Redirect Attacks:** Monitors ICMP Type 5 packets and flags illegitimate gateway redirection attempts.
* **SSL/TLS Interception Indicators:** Detects anomalies suggesting man-in-the-middle behavior.

---

## 📥 Download & Installation
The Windows installer is available under **Releases**:
👉 Download `ShieldOfDawood_Installer.exe` from the latest release. For integrity verification, a SHA256 checksum is provided in the release notes.

### 📦 Dependencies
The installer handles required dependencies automatically:
* **Python Runtime:** Installed automatically during setup.
* **Npcap:** Installed during setup (requires user interaction). Used for packet capture and network traffic analysis.

### 🖥️ Supported Platforms
* Windows 10
* Windows 11

---

## ⚠️ Important Requirements & Notices

### 🔑 Administrator Privileges (Required)
Shield of Dawood MUST be run as Administrator.
* **Reason:** The tool relies on low-level network inspection. Packet capture and interface monitoring require elevated privileges. Npcap will not function correctly without admin rights.
* **Action:** Always right-click the application and select **Run as administrator**.

### 🛡️ Windows 11 – Smart App Control Notice
If you are running Windows 11, the operating system may block the application due to Smart App Control or reputation-based protection. This is expected behavior for custom-built, unsigned security tools and does **not** indicate malware behavior.

**Required Action (Windows 11 only):**
1. Open **Settings** -> **Privacy & Security** -> **Windows Security**
2. Click **App & browser control**
3. Open **Smart App Control** and set it to **Off**
4. Restart the system if prompted

### ⚠️ Windows SmartScreen Notice
When launching Shield of Dawood, Windows may display a SmartScreen warning indicating that the application is from an unknown publisher. To proceed, select **More info** → **Run anyway**. *(Future releases may include a digital signature to reduce or eliminate this warning).*

---

## 🛠️ Usage Notes & Disclaimer
* Run the application **only** on networks you own or are authorized to monitor.
* Administrator privileges are mandatory for correct operation.
* **Disclaimer:** This project is provided for defensive security research and educational use only. Unauthorized monitoring of networks you do not own or have permission to analyze may be illegal.



---

**Developed by Mahmoud Hamadah**
