📔 Cybersecurity Lab: Automated Environment Deployment
Date: January 8, 2026
Tools: Vagrant, VirtualBox, macOS Monterey, Kali Linux, Metasploitable 3
1. Project Objective
To build an isolated penetration testing environment using "Infrastructure as Code" (IaC) to safely practice exploit research and network analysis.
2. Technical Implementation & Topology
• Automation: Deployed Metasploitable 3 using Vagrant to ensure a repeatable, standardized environment.
• Network Architecture: Migrated to a NAT Network (10.0.2.0/24) to bypass legacy "Host-Only" driver limitations on macOS Monterey.
3. Challenges & Troubleshooting
• PATH Configuration: Resolved command not found: vagrant by manually mapping the binary path in the .zshrc profile.
• Ruby Syntax Debugging: Fixed a Vagrantfile crash caused by a formatting error in the VirtualBox provider block (v.gui = true).
• Layer 2/3 Connectivity: Overcame DHCP failures by manually assigning static IPs (10.0.2.50 and 10.0.2.60) and verifying the "virtual cable" connection in the hypervisor settings.
4. Verification
• Connectivity: Achieved 0% packet loss during ping testing between Attacker and Victim.
• Reconnaissance: Initialized Nmap service scanning to begin vulnerability mapping.
