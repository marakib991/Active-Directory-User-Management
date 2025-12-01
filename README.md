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
<img width="1000" height="804" alt="Image" src="https://github.com/user-attachments/assets/787c21ee-9611-4814-8043-0bc649097d68" />

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

### 4. Client Joining the Active Directory Domain Controller
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

#### Turn off firewall
For to avoid connection issues of packet loss or network restriction between the client pc to the domain, firewall is temporarily turned off on the client machine.
<img width="1205" height="1106" alt="Image" src="https://github.com/user-attachments/assets/39a29897-5dc0-47af-837c-75ebfeb190a2" />
<img width="1291" height="1096" alt="Image" src="https://github.com/user-attachments/assets/d2007476-9c65-43cb-99b9-5bd570f9fef1" />
<img width="981" height="1029" alt="Image" src="https://github.com/user-attachments/assets/f655d95f-1764-424e-a848-9bb3f9e5207d" />
<img width="1152" height="971" alt="Image" src="https://github.com/user-attachments/assets/9580a1a4-1c94-41c6-be01-d0fbedc7003a" />
<img width="1161" height="983" alt="Image" src="https://github.com/user-attachments/assets/ef641c31-464c-41c7-9c77-cd50c62095b4" />

#### Varify the Connection between Client PC and the Domain Server
Verified domain membership with:
  - `whoami /fqdn`
  - `ping` between server and client
First checked if helpdesk is connected to **DC** machine or **Server**
<img width="1024" height="698" alt="Image" src="https://github.com/user-attachments/assets/b5ba2262-2b7a-446d-80b3-dee652827f82" />
Next checked from the windows 10 client machine/PC
<img width="1018" height="606" alt="Image" src="https://github.com/user-attachments/assets/69ae3857-c7ed-4dbd-aaac-c972cf91f2f7" />
<img width="1279" height="647" alt="Image" src="https://github.com/user-attachments/assets/915b13cb-e68a-49f0-8095-2c576cebfa92" />

---

### 5. Remote Administration Tools
- Installed **RSAT: Active Directory Domain Services Tools** on Windows 10.
- Used ADUC (Active Directory Users and Computers) to create a standard user (`user2`).

#### DNS Server Address change
Changed the **DNS Server Address** from **Server IPv4 address** to **8.8.8.8 (google DNS)** temporarily for faster downloading 
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/07a6d68d-43b3-46b0-a6c4-410a2a7cfdb2" />

#### Download RSAT: Active Directory Domain Services Tools
The tool was download from optional features of Apps & Features.
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/32e79cd6-a46f-4525-b041-ebf003b3165d" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/ee0bf6a1-2955-4da4-b91f-c671a2ce14d0" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/0e655b9c-5766-4b7e-b66b-0df6e0e52716" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/b60e1723-ea0a-4e68-8d50-37378304377b" />

#### Create New Domain User from the Windows Client PC
From **Windows Administrative Tools**, created a new domain user named **user2**.
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/e98bbacf-ea94-4291-b52a-f4e125c7bcea" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/39696b01-2d77-4726-a9e3-1924c7f5c9ad" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/e9c9e0d2-489e-49aa-92d8-a278a9aaa4d8" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/372c398a-b010-4f0c-b74e-d466e8bf01ff" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/ddd3b738-f90e-47a1-aa3f-9ec6c3891968" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/b3277852-197b-442e-b7d7-eb1138d580e7" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/91b2fd14-179e-4b32-a22e-c807fb253100" />
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/1c36d39a-4fd3-4831-977f-dd15fe409548" />

#### Changed the DNS Server Address back to the server's IP address
<img width="1686" height="1246" alt="Image" src="https://github.com/user-attachments/assets/4a913d39-0fa1-4ccf-83b9-328d0b2e05c0" />

---

### 6. Group Policy Configuration
#### Edited **Default Domain Policy**:
Default **Account Lockout Policy** was modified and the new duration was set to 30 minutes and applied the suggested **Lockout Threshold of 5 invalid attempts**.
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/00bc1334-2016-4783-aaeb-f20532575619" />
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/4c30b513-2cbc-4e55-9a6a-5a232a60f8b2" />
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/35452f80-c396-41e6-9a12-c77a20a82475" />
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/3fa1f26c-7cc4-477b-9944-4eeacebc1c3d" />
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/03592aa2-a4df-4bad-a905-0b625d2e519a" />
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/99a69507-051b-4c9c-a7c2-619f1955239a" />
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/109daaa0-5b5b-4cb0-8627-f1f1001de336" />

#### Verified the changes
Checked if the changes applied in group policy for domain account with `net accounts` in Server PC and Client PC.
<img width="1204" height="787" alt="Image" src="https://github.com/user-attachments/assets/67102525-794a-4cff-b6b5-c68af722ebbb" />
<img width="1134" height="763" alt="Image" src="https://github.com/user-attachments/assets/18920eac-e00c-4dd4-8fa5-92dfd958539b" />

#### Update group policy in Windows Client PC
As group policy changes wasn't update in the windows 10 client PC, `gpupdate /force` command was run to apply the changes and then rechecked to see if the group policy is upodated.
<img width="898" height="906" alt="Image" src="https://github.com/user-attachments/assets/1e81103e-b4b3-4a1b-b518-12a05efd5587" />

#### Generate **Group Policy Report**
**Group Policy** report (in html format) were generated using `gpresult /h c:\gpresult.html` command and run the **Command Prompt** as administrator. As **user1** is included in the **Domain Admins** group, **user1** has the access to group policy read.
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/fe37d3be-015b-44f4-adfc-a4d87f72dd41" />
<img width="771" height="375" alt="Image" src="https://github.com/user-attachments/assets/3a88d09b-77da-4d84-8d1f-58ba8a08f9ff" />
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/0e216c31-0eed-4af4-8717-77d3cc1bc203" />
<img width="1698" height="1244" alt="Image" src="https://github.com/user-attachments/assets/505df6eb-a9cb-4900-a8ef-24753530ee32" />

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

