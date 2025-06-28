
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

