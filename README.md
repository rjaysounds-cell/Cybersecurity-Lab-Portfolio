# 📔 Cybersecurity Lab: Automated Environment Deployment
**Date:** January 2026  
**Role:** Security Researcher / Lab Architect  
**Tools:** Vagrant, VirtualBox, macOS Monterey (Intel), Ruby, Metasploitable 3

## 1. Project Objective
To build an automated, isolated penetration testing environment using "Infrastructure as Code" (IaC) principles. This lab serves as a safe sandbox for testing vulnerability scanners and exploitation techniques without risking production hardware.

## 2. Technical Implementation
Instead of manual installation, I utilized **Vagrant** to automate the deployment of **Metasploitable 3**. 
* **Virtualization:** Oracle VM VirtualBox.
* **Automation:** Used `vagrant up` to provision the environment from a Ruby-based Vagrantfile.
* **Networking:** Configured a private, host-only network to ensure the vulnerable machines were not exposed to the public internet.

## 3. Challenges & Troubleshooting
* **Issue:** Command `vagrant` not found on macOS Monterey.
    * **Resolution:** Identified a PATH variable mismatch. Manually updated the `.zshrc` profile to correctly link the binary to `/usr/local/bin`.
* **Issue:** Ruby Syntax Error in Vagrantfile.
    * **Resolution:** Debugged the `v.gui` configuration block, correcting a line-break error that was causing a "unexpected local variable" crash. 
* **Issue:** Kernel Driver (rc=-1908) on Intel Mac.
    * **Resolution:** Managed macOS System Policy permissions via Terminal to allow Oracle extensions to run on Intel architecture.

## 4. Skills Demonstrated
* **Linux/UNIX Administration:** Environment variable management and shell configuration.
* **Virtualization:** Managing hypervisors and virtual hardware resources.
* **Infrastructure as Code (IaC):** Automating system deployment via scripts.
