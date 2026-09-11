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


4. ** 🐉 Kali Linux Setup **

 Import the Kali Linux ISO/OVA into VirtualBox.

Download Kali Linux: https://kali.org/get-kali



## Configure the Kali Linux Virtual Machine

Set up Kali Linux as the primary security-testing machine for the laboratory. You can either create a new virtual machine or import the official Kali Linux VirtualBox image.



### Recommended Configuration

   ```text
Name:        Kali-Linux-2026.2
OS Type:     Linux / Debian (64-bit)
Memory:      2048 MB
Processors:  2
Storage:     80 GB
```





<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/6d32736e-ff9c-45db-a473-0bd523be94b5" />
<img width="1920" height="1020" alt="image" src="https://github.com/user-attachments/assets/54cf186b-3bee-4f6d-9eff-99dcbc7aa32f" />




 ###
 
 **Configure the VM Network Adapter**

   The Kali Linux virtual machine was configured to use the dedicated NAT Network created for the lab.

   ```text
   Adapter:       Adapter 1
   Attached to:   NAT Network
   Network:       NatNetwork
   Adapter Type:  Intel PRO/1000 MT Desktop
```
<img width="1279" height="753" alt="image" src="https://github.com/user-attachments/assets/55f35d12-bc84-43db-99a7-80a6a6d98126" />

###
5. **Configure a Static IP Address and Verify DNS Connectivity**

   Assign a static IP address to the Kali Linux virtual machine and configure the appropriate network settings to ensure reliable communication within the lab environment.

   **Kali Linux Network Configuration:**

   <img width="1599" height="842" alt="image" src="https://github.com/user-attachments/assets/a4435749-3917-4ddc-a532-d9066a486b44" />




Open terminal in the Kali Linux and run the following commands:

*For Internet connectivity issue:* `bash sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0 `

*To deactivate network profile:* ` bash sudo nmcli connection down Wired\ connection\ 1`

*To reactivate network profile:* `bash sudo nmcli connection up Wired\ connection\ 1`
<img width="1357" height="608" alt="image" src="https://github.com/user-attachments/assets/a5bfae27-6d45-4d97-8fae-674cd7618c35" />
All connection was confirmed running





### 
6.**Verify Network Connectivity**

Open the terminal in Kali Linux and use the following commands to confirm both Internet connectivity and DNS resolution:

```bash
ping -c 4 8.8.8.8
ping -c 4 google.com
```
<img width="1354" height="355" alt="image" src="https://github.com/user-attachments/assets/f89bc1eb-1e1d-4535-8c50-d18994971936" />
Verifying Results: Both 8.8.8.8 (gateway) and google.com (DNS) successfully returned 0% packet loss, confirming full outbound network connectivity

---

###

7. *Create a Clean VM Snapshot*
After completing the initial network configuration and verification, a baseline VirtualBox snapshot was created.

The snapshot captures the fully configured state of the laboratory environment.

<img width="1248" height="401" alt="Screenshot 2026-09-11 083323" src="https://github.com/user-attachments/assets/3d016381-b1d6-4735-89cc-71693987be5c" />


If a future exercise changes system files, breaks networking, or degrades the VM state, the machine can be restored immediately to this clean baseline.


---


###

**Lab Verification**  
   Confirm that the Kali Linux machine has the correct IP address assigned and can communicate with the lab gateway and the internet.

   | Test                        | Command                         | Expected Result                     |
   |-----------------------------|---------------------------------|-------------------------------------|
   | Check IP address            | `ip a`                          | Correct Kali IP displayed           |
   | Test gateway                | `ping 10.0.0.1`                 | Successful replies                  |
   | Test Internet connectivity  | `ping 8.8.8.8`                  | Successful replies                  |
   | Test DNS resolution         | `nslookup networkwalks.com`     | Domain resolves                     |
   | Verify Nmap                 | `nmap --version`                | Nmap version displayed              |
   | Verify snapshot             | Restore snapshot and run `ip a` | Baseline configuration restored     |

 
 ###
 ## Example Result ##

IP Address:
10.0.0.2/24

Gateway:
10.0.0.1

DNS:
8.8.8.8

---

###

## Problem Encountered ##

THE problem I encountered was with the network configuration and setup but  I was able to resolved the challenge by following the guideline rules strictly



---

###
## Experience From The Session ##


- Virtual Machine Networking:

I learned that using NAT Network in VM will help the machines in the lab communicate safely.

- Static IP configuration:

I learned how to configure IP addresses, DNS Connectivity , Gateways and Test Connectivity, 

- Screenshots in Virtual Machine:

I was able to identify and able take screenshots.

- Verify Nmap
  
I learned to verify the concept of Nmap

- Snapshots:

Saved a baseline state right after setting up Kali so I can reset the VM anytime.

---

###

## 🎯 Key Takeaways & Findings ##

- Network Integrity: Verified host-to-gateway routing and DNS translation on Kali Linux (10.0.0.0/24).

- Tool Proficiency: Successfully performed host discovery, port scanning, and service enumeration using native CLI utilities (ping, nc, nmap).

- Lab Security: Enforced privacy best practices by isolating test targets and abstracting network configurations

---

###

## 🔐 Security & Ethical Issue ##
This laboratory is completely for educational purpose only.

No target-specific credentials, confidential information, patient records, private infrastructure details, or sensitive assessment evidence are included in this repository.

---
###


## 🔭 Tools and Resources ##

To install 7-Zip: https://7-zip.org/download.html.

To install VirtualBox Machine: https://virtualbox.org/wiki/Downloads.

To install Kali Linux: https://kali.org/get-kali.

---

### 👤 Author

Oyewale Olaoluwa Gideon

Cybersecurity Intern B083

 LinkedIn: www.linkedin.com/in/oyewale-olaouwa-60b252bb

---

###  

## 📌 Project Information ##
Program Name: Cybersecurity at Networkwalks | Week: 01 | Project: Cybersecurity and Pentesting Lab Setup | Repository: GitHub

   










  


