# WK1-PM1: VirtualBox & Kali Linux Cyber Lab Setup

## Introduction
This report covers the setup of a foundational Cybersecurity Testing Lab Environment. The objective of this project was to build a secure, isolated network using Oracle VirtualBox to host an attacking machine (Kali Linux). This report includes the process of configuring the NAT Network, setting up a static IP, and enabling host-to-guest integration. All activities were run on a Windows host machine. I have properly documented below every step I took, including the exact tools used, the process, and the results achieved. I also took several screenshots of the activities as evidence.

## Tools Used
The table below lists each tool used in this report and its purpose.

| Tools | Purpose |
| :--- | :--- |
| **VirtualBox** | A free, open-source hypervisor used to run the virtual machines. |
| **Kali Linux** | A Debian-derived Linux distribution designed for digital forensics and penetration testing (the Attacker Machine). |
| **NAT Network** | A VirtualBox network mode that allows VMs to communicate with each other and the internet while remaining isolated from the host. |
| **Guest Additions** | A set of drivers and system applications installed inside the guest OS to improve performance and enable host-guest integration. |

## Activities Performed

### Environment Setup and Network Configuration (WK1 PM1)
**Objective:** Create a custom isolated subnet (`10.0.0.0/24`) and configure Kali Linux to act as the attacking machine.

*   **STEP 1 - NAT Network Creation:** Opened VirtualBox global settings and navigated to the Network section. Created a new NAT Network named `NatNetwork` and configured the IPv4 Prefix to `10.0.0.0/24`.
*   **STEP 2 - Adapter Configuration:** Opened the Kali VM settings, enabled Network Adapter 1, and attached it to the `NAT Network` created in the previous step. 
*   **STEP 3 - Static IP Assignment:** Booted Kali Linux and opened the Network Settings. Configured a manual IPv4 profile with the address `10.0.0.2`, Netmask `24`, Gateway `10.0.0.1`, and DNS `8.8.8.8`.
*   **STEP 4 - Integration:** Ensured VirtualBox Guest Additions were installed and configured a shared folder to allow file transfers from the host machine into the Kali environment.
*   **STEP 3 - Guest Additions:** Ensured VirtualBox Guest Additions were installed to enable seamless integration between the host and the guest VM.
*   **STEP 4 - Shared Folders:** Configured a shared folder to allow file transfers from the host machine into the Kali environment, verifying the successful mount on the Kali desktop.

LinkedIn: www.linkedin.com/in/alabi-isreal-bab9b8432
