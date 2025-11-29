# 🖥️ Active Directory User Management

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
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/be2b9294-189c-4531-b2be-58b3219d590d" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/4e2d8c50-b52a-47c4-a021-5dcf26bfee9d" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/0a551aee-9326-4f69-8443-519076c88394" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/85b25145-691b-47f2-8a59-5cf2b21ee394" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/3215c8f8-80d1-4997-9e79-8421eaf7e4bb" />

**Setting up Windows 10 Enterprise**
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/e525cf99-0f67-4fb6-b0be-16a11804f70c" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/593e3cf5-0bfc-45f9-b0be-72f64a452fc7" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/ab1f9935-6fec-427c-9221-fceb933cf1aa" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/f1d142a9-8a96-4d5f-a539-6066c01008fe" />

**Configure both VMs with bridge networking**
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/4f035d8f-5fb6-4667-af48-c6dae084e3fe" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/8cf0475e-a3ef-4a6e-9e28-35450c944233" />

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


