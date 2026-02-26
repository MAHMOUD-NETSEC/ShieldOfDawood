# 🛡️ Shield of Dawood

**Shield of Dawood** is a Windows-based defensive cybersecurity tool designed to detect suspicious activity and common local network attacks.

This repository provides:
- A precompiled Windows installer (via GitHub Releases)
- High-level documentation of the detection logic

Source code is intentionally not published.

---

## 📥 Download

The Windows installer is available under **Releases**:

👉 Download **ShieldOfDawood_Installer.exe** from the latest release.
For integrity verification, a SHA256 checksum is provided in the release notes.

---

## ⚠️ Important Requirements

### 🔑 Administrator Privileges (Required)
**Shield of Dawood MUST be run as Administrator.**

Reason:
- The tool relies on low-level network inspection
- Packet capture and interface monitoring require elevated privileges
- Npcap will not function correctly without admin rights

➡️ Always right-click the application and select **Run as administrator**.

## 🛡️ Windows 11 – Smart App Control Notice

If you are running **Windows 11**, the operating system may block the application due to **Smart App Control** or reputation-based protection.

This is expected behavior for custom-built security tools.

### Required Action (Windows 11 only)
Before running Shield of Dawood, ensure **Smart App Control** is disabled:

1. Open **Settings**
2. Go to **Privacy & Security**
3. Select **Windows Security**
4. Click **App & browser control**
5. Open **Smart App Control**
6. Set it to **Off**
7. Restart the system if prompted

Without disabling Smart App Control, Windows 11 may prevent the application from launching.

---

This does **not** indicate malware behavior.  
The application is blocked solely because it is a custom, unsigned security tool.


---

### 📦 Dependencies
The installer handles required dependencies automatically:

- **Python Runtime**  
  Installed automatically during setup

- **Npcap**  
  Installed during setup (requires user interaction)  
  Used for packet capture and network traffic analysis

---

## 🖥️ Supported Platform
- Windows 10
- Windows 11

---

## 🔍 Detection Logic Overview

The tool performs real-time monitoring and detection of the following attack types:

- **ARP Spoofing**
  - Detects IP–MAC address mismatches
  - Flags unsolicited ARP replies

- **DNS Spoofing**
  - Verifies DNS responses against the legitimate gateway
  - Detects mismatched IP/MAC responses

- **Rogue DHCP**
  - Identifies unauthorized DHCP offer packets
  - Detects unexpected DHCP servers on the network

- **ICMP Redirect Attacks**
  - Monitors ICMP Type 5 packets
  - Flags illegitimate gateway redirection attempts

- **SSL/TLS Interception Indicators**
  - Detects anomalies suggesting man-in-the-middle behavior

---

## 🛠️ Usage Notes

- Run the application **only on networks you own or are authorized to monitor**
- Administrator privileges are mandatory for correct operation
- The tool is intended for **defensive and educational purposes**

---

## 🔐 Disclaimer

This project is provided for **defensive security research and educational use only**.  
Unauthorized monitoring of networks you do not own or have permission to analyze may be illegal.

---

**Developed by Mahmoud Hamadah**
