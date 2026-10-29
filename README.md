# WK1-PM1: VirtualBox & Kali Linux Cyber Lab Setup

## Introduction
This report documents the successful setup of a foundational Cybersecurity Testing Lab Environment. The objective of this project was to build a secure, isolated network using Oracle VirtualBox to host an attacking machine (Kali Linux). I have documented the exact steps taken, the network architecture designed, and the configuration of the virtual machine to ensure seamless usability. All activities were run on a Windows host machine. I have included screenshots as evidence of the network configuration and system integration.

## Tools Used
The table below lists each tool used in this report and its purpose.

| Tool | Purpose |
| :--- | :--- |
| **Oracle VirtualBox** | A free, open-source hypervisor used to run the virtual machines. |
| **Kali Linux** | A Debian-derived Linux distribution designed for digital forensics and penetration testing (the Attacker Machine). |
| **NAT Network** | A VirtualBox network mode that allows VMs to communicate with each other and the internet while remaining isolated from the host. |
| **VirtualBox Guest Additions** | A set of drivers and system applications installed inside the guest OS to improve performance and enable host-guest integration. |

## Activities Performed

### 1. Network Architecture & NAT Network Setup (WK1 PM1)
**Objective:** Create a custom isolated subnet (`10.0.0.0/24`) for the lab environment.

*   **STEP 1 - NAT Network Creation:** Opened VirtualBox global settings and navigated to the Network section. Created a new NAT Network named `NatNetwork`.
*   **STEP 2 - Subnet Configuration:** Configured the IPv4 Prefix to `10.0.0.0/24` to ensure all future Virtual Machines exist on the same isolated subnet.
*   **STEP 3 - DHCP Settings:** Enabled the DHCP server on the NAT Network so that if any VM is set to automatic, it will receive an IP within the correct range.

### 2. Kali Linux VM Configuration & Integration
**Objective:** Attach the Kali Linux VM to the custom network and enable host-guest communication.

*   **STEP 1 - Adapter Configuration:** Opened the Kali VM settings, enabled Network Adapter 1, and attached it to the `NAT Network` created in the previous step. Set the adapter type to `Intel PRO/1000 MT Desktop` for optimal compatibility.
*   **STEP 2 - Static IP Assignment:** Booted Kali Linux and opened the Network Settings. Configured a manual IPv4 profile with the address `10.0.0.2`, Netmask `24`, Gateway `10.0.0.1`, and DNS `8.8.8.8`.
*   **STEP 3 - Guest Additions:** Ensured VirtualBox Guest Additions were installed to enable seamless integration between the host and the guest VM.
*   **STEP 4 - Shared Folders:** Configured a shared folder to allow file transfers from the host machine into the Kali environment, verifying the successful mount on the Kali desktop.

LinkedIn: www.linkedin.com/in/alabi-isreal-bab9b8432
