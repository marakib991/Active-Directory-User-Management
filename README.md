# Active Directory User Management

This repository documents my homelab project, where I set up a Windows Server 2016 domain controller and a Windows 10 Enterprise client using VirtualBox. The goal was to simulate real-world IT helpdesk tasks, including domain setup, user management, group policy configuration, and software deployment.

---


## Key Skills Demonstrated
- Virtualization with VirtualBox  
- Active Directory setup and domain management  
- DNS configuration and troubleshooting  
- Group Policy creation and enforcement  
- Remote Server Administration Tools (RSAT) usage  
- Software deployment via GPO  

---


## Project Overview
- **Virtualization Tool:** Oracle VirtualBox  
- **VMs Created:**
  - Windows Server 2016 (Domain Controller)
  - Windows 10 Enterprise (Client)  
- **Resources Allocated:** 4 GB RAM, 2 CPU cores each  
- **Networking:** Bridge mode (connected to laptop Wi-Fi)

---

## Steps & Configuration

### 1. VM Setup
- Created two VMs and assigned them RAM, Processor and Storage.
- Configured both VMs with bridge networking.

#### Setting up Windows Server 2016
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/be2b9294-189c-4531-b2be-58b3219d590d" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/4e2d8c50-b52a-47c4-a021-5dcf26bfee9d" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/0a551aee-9326-4f69-8443-519076c88394" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/85b25145-691b-47f2-8a59-5cf2b21ee394" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/3215c8f8-80d1-4997-9e79-8421eaf7e4bb" />

#### Setting up Windows 10 Enterprise
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/e525cf99-0f67-4fb6-b0be-16a11804f70c" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/593e3cf5-0bfc-45f9-b0be-72f64a452fc7" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/ab1f9935-6fec-427c-9221-fceb933cf1aa" />

<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/f1d142a9-8a96-4d5f-a539-6066c01008fe" />

#### Configure both VMs with bridge networking
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/4f035d8f-5fb6-4667-af48-c6dae084e3fe" />
<img width="2132" height="1242" alt="Image" src="https://github.com/user-attachments/assets/8cf0475e-a3ef-4a6e-9e28-35450c944233" />

---

### 2. Windows installation and initial setup

#### Windows Server 2016 installation
**Install OS:** Datacenter Evalutation (Desktop Experience).
<img width="1051" height="876" alt="Image" src="https://github.com/user-attachments/assets/c91f8ce2-c58d-45b6-972c-cba23850ea95" />
<img width="1037" height="908" alt="Image" src="https://github.com/user-attachments/assets/18eab899-0f73-4e14-ad72-f2b9b89079fd" />
<img width="1017" height="878" alt="Image" src="https://github.com/user-attachments/assets/1ddc8d90-2188-4560-9ed4-5a7f1606909e" />

#### Windows 10 installation
After the initial windows installation was done, domain joined to create a administrator user account.
<img width="1018" height="805" alt="Image" src="https://github.com/user-attachments/assets/18ccc02e-1cf1-49b9-8a34-b9ca9c664f09" />
<img width="1023" height="799" alt="Image" src="https://github.com/user-attachments/assets/5241fa31-996d-4847-8387-1baad87b3fd1" />
<img width="1019" height="783" alt="Image" src="https://github.com/user-attachments/assets/14bde080-3fbf-4d80-861d-42f924910c45" />
<img width="2138" height="1244" alt="Image" src="https://github.com/user-attachments/assets/8a6a78f8-68b9-40a7-8bc6-a9f3e61c2aa0" />

---

### 3. Active Directory Domain Setup
- Installed **Active Directory Domain Services (AD DS)** role on the server.
- Created a new forest in domain controller: **rakib.org**.
- Created a domain admin account (`user1`) for helpdesk duties.

#### Server Manager with AD DS role installed
<img width="1296" height="1069" alt="Image" src="https://github.com/user-attachments/assets/b5f1d773-c53c-4361-ba20-e6c3d6241c84" />

<img width="1303" height="1147" alt="Image" src="https://github.com/user-attachments/assets/733776ac-9d8c-4743-8155-c7211befea9f" />

<img width="1290" height="1143" alt="Image" src="https://github.com/user-attachments/assets/d917efb1-25f2-4c64-81a5-525042e85910" />

<img width="1294" height="1148" alt="Image" src="https://github.com/user-attachments/assets/51a35ff8-6e26-4958-88ba-d790b5ee14bb" />

<img width="1275" height="1129" alt="Image" src="https://github.com/user-attachments/assets/915cca80-154e-4e96-9c91-0a52bc7c9284" />

<img width="1284" height="1140" alt="Image" src="https://github.com/user-attachments/assets/51190600-1e97-4dd2-b675-bb4107881729" />

#### Domain creation wizard (rakib.org)
After the installation was done, the computer restarted and the server was activated.
<img width="1045" height="848" alt="Image" src="https://github.com/user-attachments/assets/5578bac9-3376-4137-a4bd-c3fce50df87c" />

<img width="970" height="738" alt="Image" src="https://github.com/user-attachments/assets/38e6a112-973d-4866-ab10-a039805f603b" />

<img width="944" height="710" alt="Image" src="https://github.com/user-attachments/assets/1da6e150-41e9-4dac-b27d-6b10c8b8a3fd" />

<img width="951" height="699" alt="Image" src="https://github.com/user-attachments/assets/7bbf4575-807e-41ba-8e77-4a0419ca8e76" />

#### New domain user creation
From **Server Manager**, new user were created named "user1". Then the user1 was temporarily added to "Domain Admins" group to give it access to **Administrative Tools**.
<img width="1262" height="1095" alt="Image" src="https://github.com/user-attachments/assets/5f044890-325e-4db8-b115-3abc0d7170b6" />

<img width="1298" height="1105" alt="Image" src="https://github.com/user-attachments/assets/868d70bd-619f-4a96-b2c5-326088683027" />

<img width="1258" height="1109" alt="Image" src="https://github.com/user-attachments/assets/533a30b1-0c29-4f0d-ae41-00908d0410d7" />

<img width="827" height="759" alt="Image" src="https://github.com/user-attachments/assets/0af78e29-6081-4bd2-86a4-ae7670b638f3" />

<img width="695" height="710" alt="Image" src="https://github.com/user-attachments/assets/6c207b4f-c02b-4521-87b6-6678b558e6ac" />

<img width="1169" height="952" alt="Image" src="https://github.com/user-attachments/assets/1e133dfe-dde8-42f3-a14d-496421a5aeb0" />

<img width="1045" height="925" alt="Image" src="https://github.com/user-attachments/assets/882cafb4-a9a7-45d9-ae2a-e265f0dfd9c8" />

<img width="1126" height="712" alt="Image" src="https://github.com/user-attachments/assets/1a522ca2-1c86-4567-9213-ce7ee46e88c4" />

<img width="1005" height="923" alt="Image" src="https://github.com/user-attachments/assets/556a1d80-97c0-44d4-bafe-83356e55cf9a" />

Using **Command Prompt**, run `ipconfig` to find out the server's IPv4 address to setup the network adapter of users to let them connect to the domain controller.
<img width="835" height="873" alt="Image" src="https://github.com/user-attachments/assets/e0718a43-d722-4bd0-8d48-47b369125d6e" />

---

### 4. Client Domain Join
#### Rename PC
Renamed Windows 10 client to **HELPDESK**.
<img width="1090" height="935" alt="Image" src="https://github.com/user-attachments/assets/9b6b078d-b15a-4ecd-b156-e68f5897f2b9" />
<img width="1056" height="725" alt="Image" src="https://github.com/user-attachments/assets/ab2ddd23-86e7-4b4b-a6cd-1787853a7489" />

#### Change DNS Server
Configured DNS to point to the server’s IP.
<img width="1281" height="1093" alt="Image" src="https://github.com/user-attachments/assets/b4944b2e-0eca-4238-9324-94d23496212e" />
<img width="1047" height="811" alt="Image" src="https://github.com/user-attachments/assets/2205b31e-8b03-42af-86f3-8d74084db0c0" />
<img width="816" height="792" alt="Image" src="https://github.com/user-attachments/assets/446f5721-6654-4fbb-bae6-1a9c0409119a" />
<img width="691" height="931" alt="Image" src="https://github.com/user-attachments/assets/0dfbb928-5ae5-4211-9055-0133c94763f4" />
<img width="732" height="980" alt="Image" src="https://github.com/user-attachments/assets/1fe15912-3e20-4223-837d-21f75a706158" />

#### Connect the PC to the domain
Joined the client to the **rakib.org** domain using `user1`.
<img width="1094" height="826" alt="Image" src="https://github.com/user-attachments/assets/93fca4b9-0ea0-4f1c-aa9a-42e50dde5455" />
<img width="844" height="738" alt="Image" src="https://github.com/user-attachments/assets/98aec5f7-27d7-4719-9ce7-ff2a88b49d0f" />
<img width="894" height="853" alt="Image" src="https://github.com/user-attachments/assets/3eb32220-bf78-4c14-a580-7059aa221a3d" />
<img width="868" height="780" alt="Image" src="https://github.com/user-attachments/assets/cce8380e-33bb-4a19-b44b-be50e72add5e" />
<img width="955" height="795" alt="Image" src="https://github.com/user-attachments/assets/7e784ae2-9dcb-4212-b65a-9b102b2c54c8" />

#### Varify the Connection between Client PC and the Domain Server
Verified domain membership with:
  - `whoami /fqdn`
  - `ping` between server and client


📸 *Screenshot Placeholder: Windows 10 domain join confirmation*  

---

### 5. Remote Administration Tools
- Installed **RSAT: Active Directory Domain Services Tools** on Windows 10.
- Used ADUC (Active Directory Users and Computers) to create a standard user (`user2`).

📸 *Screenshot Placeholder: RSAT installation on Windows 10*  
📸 *Screenshot Placeholder: ADUC showing user2 creation*

---

### 6. Group Policy Configuration
- Edited **Default Domain Policy**:
  - Account lockout duration: 30 minutes
  - Lockout threshold: 5 invalid attempts
- Verified changes with:
  - `net accounts`
  - `gpupdate /force`
  - `gpresult /h c:\gpresult.html`

📸 *Screenshot Placeholder: Group Policy Management Console (Account Lockout Policy)*

---

### 7. Software Deployment via GPO
- Created an OU named **Staff** and moved HELPDESK + user1 into it.
- Shared a folder `C:\Software` with **Domain Users** permissions.
- Added **Firefox MSI installer** to the shared folder.
- Created and linked a GPO to deploy Firefox to the HELPDESK computer.
- Verified installation after `gpupdate /force` and restart.

📸 *Screenshot Placeholder: GPO Software Installation settings (Firefox MSI)*  
📸 *Screenshot Placeholder: Firefox installed on HELPDESK desktop*

---


