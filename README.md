
# Project Alpha

# 🗄️ Project Alpha 

### A Centralized NAS Server for Personal & Team Cloud Storage  
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
## 📡 Use Case Scenarios

### 🧑‍💻 Host and Organize Code, Documents, and PDFs
Use Project Alpha as your personal coding vault or document server — perfect for developers, writers, and students.

### 🎬 Stream Videos and Media Across LAN
Stream movies, music, or lectures directly from your NAS to devices on your network using VLC, Kodi, or DLNA apps.

### 🏫 Store and Share College Projects with Group Mates
Centralize your academic resources and share assignments, notes, and presentations securely over your campus network.

### 👨‍👩‍👧‍👦 Use as a Home Shared Family Drive
Keep family photos, videos, and important documents in one accessible place — accessible from any device at home.

----
## 🆚 Why Project Alpha > Google Drive (for Local/Private Use)

| **Feature**     | **Google Drive**     | **Project Alpha NAS**          |
|----------------|----------------------|-------------------------------|
| 🏠 Ownership     | Google-owned          | ✅ Fully yours                 |
| 💾 Storage Limit | 15 GB free            | ✅ As much as your HDD allows |
| 🔒 Privacy       | Tracks user data      | ✅ Private and offline         |
| ⚡ LAN Speed     | Cloud-only            | ✅ Gigabit LAN access          |
| 💰 Cost          | Monthly subscription  | ✅ One-time hardware cost      |



## ⚙️ Future Enhancements (Alpha v1.1+)

### 🌐 Add NextCloud for Web UI and Syncing
Integrate a user-friendly web dashboard to upload, download, and sync files across devices — similar to Google Drive.

### 🔒 User-Specific Access Controls
Create individual user accounts with custom permissions and folder-level restrictions for better access control.

### 🕐 Scheduled Backups to External Drives
Automate backup routines to mirror your NAS content to external HDDs or USB drives periodically.

### 📊 Monitor Usage Stats (Disk, Bandwidth)
Track storage space, device uptime, and network bandwidth usage through dashboards or logging scripts.

### ☁️ Backup Sync to External Cloud (Optional Hybrid)
Set up automated sync to services like Google Drive or Dropbox to maintain an off-site backup layer for critical data.

## 📜 License

This project is open-source under the **[MIT License](https://opensource.org/licenses/MIT)**.  
You are free to use, modify, and distribute this software with proper attribution.
