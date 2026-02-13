Hybrid Enterprise Infrastructure & Zero Trust Lab
An enterprise-grade simulation of a hybrid-cloud environment focusing on Identity Management, Network Segmentation, and Security Hardening.

🏗 Architecture Overview
This lab simulates a 50-user corporate environment. It bridges a local Proxmox virtualization stack with Microsoft Entra ID (Azure) to demonstrate modern hybrid identity and "Assume Breach" security logic.

Core Components

Hypervisor: Proxmox VE

Networking: pfSense Firewall (4-VLAN Segmentation)

Identity: Windows Server 2022 (AD DS) + Microsoft Entra ID (Azure AD)

Cloud Integration: Entra ID Connect (Hybrid Sync)

Storage: TrueNAS Core (SMB Shares with AD-integrated ACLs)

🔐 Security Features (Zero Trust Implementation)
Network Micro-segmentation: Traffic is restricted between Management, Server, User, and DMZ zones via pfSense rules.

Identity Protection: Implemented Conditional Access policies to require MFA for all administrative logins.

Least Privilege: Configured Role-Based Access Control (RBAC) to ensure users have only the permissions necessary for their specific OUs.

Audit Logging: Centralized Windows Event forwarding and Azure Sign-in log monitoring.

📸 Network Diagram
[INSERT YOUR DIAGRAM IMAGE HERE - Use Draw.io or LucidChart]
Tip: A visual map of your VLANs and how the Sync works is the #1 way to prove you built this.

🚀 Key Learning Outcomes
Hybrid Sync: Successfully configured the Entra ID Connect bridge, solving common UPN suffix and synchronization errors.

Firewall Logic: Developed "Deny by Default" rulesets to prevent lateral movement within the network.

Disaster Recovery: Created automated ZFS snapshots on TrueNAS and performed a successful "Restoration Test" on a deleted AD object.

🛠 How to Use This Repo
This repository contains:

/Docs: Detailed step-by-step implementation guides.

/Scripts: PowerShell scripts used for bulk user creation and GPO hardening.

/Diagrams: High-resolution PDF of the network architecture.
