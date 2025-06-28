
# Project Alpha

# 🗄️ Project Alpha v1.0

### A DIY Centralized NAS Server for Personal & Team Cloud Storage  
_Built using Samba, SSH, and an old PC turned into a reliable home server_

---

## 📌 Overview

**Project Alpha 1.0** transforms any old PC into a fully functional **Network Attached Storage (NAS)** system using lightweight open-source tools. Designed to enable **secure file sharing**, **remote access**, and **LAN streaming**, it acts as your private cloud — an alternative to Google Drive or Dropbox, but with full ownership and no monthly fees.

---

## 🧠 Key Features

- ✅ Centralized File Storage over LAN/WAN  
- ✅ SMB/Samba File Sharing for Windows/Linux/Mac  
- ✅ SSH Access for remote CLI-based management  
- ✅ Media Streaming via LAN (e.g., VLC, Kodi)  
- ✅ Expandable with external hard drives  
- ✅ Power backup via power bank/UPS for reliability  
- ✅ Internet Access with DDNS (optional)

---

## 🛠️ Technologies Used

| Component          | Purpose                        |
|--------------------|--------------------------------|
| 🐧 Ubuntu Server / Raspberry Pi OS | Lightweight headless OS |
| 🔐 SSH Server       | Secure remote access           |
| 📂 Samba (SMB)      | Network file sharing           |
| 📡 DDNS (DuckDNS/No-IP) | Remote access via domain  |
| 🔌 Power Bank / UPS | Power failure resistance       |
| 📱 File Manager App | Mobile file access (optional)  |

---

## 🏗️ Hardware Requirements

| Component            | Recommendation                      |
|----------------------|--------------------------------------|
| 💻 Old PC / Raspberry Pi | Dual-core CPU, 2 GB RAM minimum |
| 💾 Storage Drive      | HDD/SSD (internal or USB external)  |
| 🌐 Network            | Ethernet recommended, Wi-Fi okay    |
| 🔌 Backup Power       | Power Bank (for Pi) or UPS (for PC) |

---

## 🚀 Setup Guide

### 1. Install the OS

- Install **Ubuntu Server** or **Raspberry Pi OS Lite**.
- Enable SSH during setup (or manually with `sudo systemctl enable ssh`).

### 2. Install & Configure Samba

```bash
sudo apt update
sudo apt install samba
sudo nano /etc/samba/smb.conf
```
---
You can now access it via:

Windows: \<server-ip>\alpha-share

Linux/Mac: smb://<server-ip>/alpha-share

3. Enable SSH for Remote Access
```
sudo apt install openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh
```
You can now SSH from another device:
```
ssh username@<server-ip>
```
---
📡 Use Case Scenarios
🧑‍💻 Host and organize code, documents, and PDFs

🎬 Stream videos and media across LAN

🏫 Store and share college projects with group mates

👨‍👩‍👧‍👦 Use as a home shared family drive

🔐 Keep private backups away from cloud providers

🆚 Why Project Alpha > Google Drive (for local/private use)
Feature	Google Drive	Project Alpha NAS
Ownership	Google-owned	✅ Fully yours
Storage Limit	15 GB free	✅ As much as your HDD
Privacy	Tracks data	✅ Private and offline
LAN Speed	Cloud-only	✅ Gigabit LAN access
Cost	Monthly fees	✅ One-time hardware

⚙️ Future Enhancements (Alpha v1.1+)
 🌐 Add NextCloud for web UI and syncing

 🔒 User-specific access controls

 🕐 Scheduled backups to external drives

 📊 Monitor usage stats (disk, bandwidth)

 ☁️ Backup sync to external cloud (optional hybrid)

📜 License
This project is open-source under the MIT License.
