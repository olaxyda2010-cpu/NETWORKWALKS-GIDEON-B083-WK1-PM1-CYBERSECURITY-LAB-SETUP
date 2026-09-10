# 🔐 CYBERSECURITY OPERATIONAL LAB DEPLOYMENT


Isolated VirtualBox/Kali Linux lab for penetration testing and ethical hacking practice.


![Cybersecurity](https://img.shields.io/badge/SKILL-CYBERSECURITY-red)
![VirtualBox](https://img.shields.io/badge/TOOL-VIRTUALBOX-blue)
![Kali Linux](https://img.shields.io/badge/OS-KALI%20LINUX-blue)
![Linux](https://img.shields.io/badge/SKILL-LINUX-purple)
![Network](https://img.shields.io/badge/NETWORK-10.0.0.0%2F24-teal)
![Penetration Testing](https://img.shields.io/badge/SKILL-PENETRATION%20TESTING-darkred)
![Virtualization](https://img.shields.io/badge/SKILL-VIRTUALIZATION-black)
![Ethical Hacking](https://img.shields.io/badge/SKILL-ETHICAL%20HACKING-orange)
![Nmap](https://img.shields.io/badge/TOOL-NMAP-green) 

---

## 📌 PROJECT OVERVIEW

This project involves creating a controlled cybersecurity laboratory using **VirtualBox and Kali Linux** to exercise  practical skills in penetration testing, ethical hacking, and network security.

The lab provides a **segmented and secure environment** for conducting reconnaissance, vulnerability identification, security assessments, and hands-on testing of cybersecurity tools and techniques without exposing unauthorized systems to risk.

---

### 🎯 OBJECTIVE


- Install and configure VirtualBox.
- Create NAT Network in the VirtualBox.
- Install/Import Kali Linux on the VirtualBox.
- Set NAT Network in the Kali Linux.
- Assign a consistent IP address to the Kali VM.
- Verify network connectivity and DNS resolution.
- Take snapshot to recover if needed.
- Document the complete setup
- prepare the environment for future tasks.


---

## 🛡️ Purpose of the Lab

This laboratory provides a secure and isolated environment for developing practical cybersecurity skills and conducting authorized security assessments.

It can be utilized for activities such as:

- Network reconnaissance
- Port and service scanning
- Vulnerability identification
- Network traffic analysis
- Web application security testing
- Exploitation techniques
- Cybersecurity tool experimentation

⚠️ **Important:** This laboratory is intended strictly for systems that you own or have explicit authorization to test. Unauthorized scanning, exploitation, or attacks against external systems are prohibited.

---

##  🛠️ Prerequisites

Before setting up the cybersecurity lab, ensure the following requirements are available:

- Oracle VirtualBox installed and configured
- Kali Linux ISO or pre-built VirtualBox image
- Minimum of 4 GB available RAM
- At least 80 GB of available storage
- CPU hardware virtualization enabled in BIOS/UEFI
- Basic familiarity with Linux command-line operations


---



## 🚀 Setup Instructions

Follow the steps below to build and configure the cybersecurity lab environment.

1. **Install 7-Zip**

   Install 7-Zip to extract the Kali Linux virtual machine files from the compressed package.

   Download 7-Zip: [https://7-zip.org/download.html](https://7-zip.org/download.html)

2. **Install Oracle VirtualBox**

   Download and install Oracle VirtualBox on your host computer. VirtualBox will be used to create and manage the virtual machines required for the lab.

   Download VirtualBox: [https://virtualbox.org/wiki/Downloads](https://virtualbox.org/wiki/Downloads)

3. **Configure the NAT Network**
   

   Open Oracle VirtualBox Manager and navigate to: Network → NAT Networks

   The first step is to create a dedicated NAT Network for the cybersecurity lab.


   Configure the network using the following address range:

   **Network:** `10.0.0.0/24`

   This provides an isolated virtual network for communication between the lab machines.

   <img width="1363" height="688" alt="image" src="https://github.com/user-attachments/assets/8191e8fc-522e-4299-ab47-82c54845ebea" />




  


