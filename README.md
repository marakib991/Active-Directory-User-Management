# 🖥️ Active Directory Homelab Project

This repository documents my homelab project, where I set up a Windows Server 2016 domain controller and a Windows 10 Enterprise client using VirtualBox. The goal was to simulate real-world IT helpdesk tasks, including domain setup, user management, group policy configuration, and software deployment.

---


## ✅ Key Skills Demonstrated
- Virtualization with VirtualBox  
- Active Directory setup and domain management  
- DNS configuration and troubleshooting  
- Group Policy creation and enforcement  
- Remote Server Administration Tools (RSAT) usage  
- Software deployment via GPO  

---


## 📌 Project Overview
- **Virtualization Tool:** Oracle VirtualBox  
- **VMs Created:**
  - Windows Server 2016 (Domain Controller)
  - Windows 10 Enterprise (Client)  
- **Resources Allocated:** 4 GB RAM, 2 CPU cores each  
- **Networking:** Bridge mode (connected to laptop Wi-Fi)

---

## ⚙️ Steps & Configuration

### 1. VM Setup
- Installed Windows Server 2016 and Windows 10 Enterprise.
- Configured both VMs with bridge networking.

**Setting up Windows Server 2016**
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/fc9a8d96-9379-4365-abf3-6f1747621e1a" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/8797a069-3139-4bc8-a62c-8e5f47a25ccb" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/e90fd125-9f5e-4ab9-a289-acd2d4bc6f0b" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/efa4e925-9373-4cbf-875e-c5064170fad8" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/20fa8607-7bac-4aa5-b7f8-cba46a417c1d" />

**Setting up Windows 10 Enterprise**
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/36cd58ec-20db-45b3-ba60-4285b4d49c7d" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/f066fb30-02c9-4266-ac73-f1a7daf46594" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/c3f92abc-2e34-4d09-85b2-c3cdb1a1fa04" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/27d23c2a-756b-4c54-8ab3-c0a489561b18" />

**Configure both VMs with bridge networking**
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/22b4b5f8-059b-42da-b530-626346125ea0" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/616b913d-e83e-46f9-b51e-e37fa3e33f19" />

---

### 2. Active Directory Domain Setup
- Installed **Active Directory Domain Services (AD DS)** role on the server.
- Created a new forest: **rakib.org**.
- Created a domain admin account (`user1`) for helpdesk duties.

📸 *Screenshot Placeholder: Server Manager with AD DS role installed*  
📸 *Screenshot Placeholder: Domain creation wizard (rakib.org)*

---

### 3. Client Domain Join
- Renamed Windows 10 client to **HELPDESK**.
- Configured DNS to point to the server’s IP.
- Joined the client to the **rakib.org** domain using `user1`.
- Verified domain membership with:
  - `whoami /fqdn`
  - `ping` between server and client

📸 *Screenshot Placeholder: Windows 10 domain join confirmation*  

---

### 4. Remote Administration Tools
- Installed **RSAT: Active Directory Domain Services Tools** on Windows 10.
- Used ADUC (Active Directory Users and Computers) to create a standard user (`user2`).

📸 *Screenshot Placeholder: RSAT installation on Windows 10*  
📸 *Screenshot Placeholder: ADUC showing user2 creation*

---

### 5. Group Policy Configuration
- Edited **Default Domain Policy**:
  - Account lockout duration: 30 minutes
  - Lockout threshold: 5 invalid attempts
- Verified changes with:
  - `net accounts`
  - `gpupdate /force`
  - `gpresult /h c:\gpresult.html`

📸 *Screenshot Placeholder: Group Policy Management Console (Account Lockout Policy)*

---

### 6. Software Deployment via GPO
- Created an OU named **Staff** and moved HELPDESK + user1 into it.
- Shared a folder `C:\Software` with **Domain Users** permissions.
- Added **Firefox MSI installer** to the shared folder.
- Created and linked a GPO to deploy Firefox to the HELPDESK computer.
- Verified installation after `gpupdate /force` and restart.

📸 *Screenshot Placeholder: GPO Software Installation settings (Firefox MSI)*  
📸 *Screenshot Placeholder: Firefox installed on HELPDESK desktop*

---


