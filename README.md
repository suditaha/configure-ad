<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/5XMXSUT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Created the Domain Controller VM (Windows Server 2022) named “DC-ONE” & the Client VM (Windows 10) named “client-one”
</p>
<br />

<p>
<img src="https://i.imgur.com/GpbVkiK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I set the Domain Controller’s NIC Private IP address to be "static" instead of "dynamic"
</p>
<br />

<p>
<img src="https://i.imgur.com/A7LLtss.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Logged into the "DC-ONE" VM and disabled the Windows Firewall (for testing connectivity)
</p>
<br />

<p>
<img src="https://i.imgur.com/9oV3sXu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I set client-one’s DNS settings to DC-ONE’s Private IP address. This ensures that client-one can locate and communicate with the Domain Controller (DC-ONE) for authentication and Active Directory services.
</p>
<br />

<p>
<img src="https://i.imgur.com/KLxwJlv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Logged into client-one and attempted to ping DC-ONE’s private IP address. Ensured the ping succeeded.
</p>
<br />

<p>
<img src="https://i.imgur.com/GHFsFlx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From client-one, I opened PowerShell and ran ipconfig /all. The output for the DNS settings showed DC-ONE’s private IP Address ✅.
</p>
<br />

<p>
<img src="https://i.imgur.com/2ANleZh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Logged into DC-ONE and installed Active Directory Domain Services.
</p>
<br />

<p>
<img src="https://i.imgur.com/U3rkfbJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Promoted/Configured "DC-ONE" as a Domain Controller: Setup a new forest as "mydomain.com" (this can be anything by the way, does not necessarily have to be "mydomain.com").
</p>
<br />

<p>
<img src="https://i.imgur.com/yIovR72.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Installed the forest. ✅
</p>
<br />

<p>
<img src="https://i.imgur.com/awTVnlI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Restarted and then logged back into DC-1 as user: mydomain.com\suditaha.
</p>
<br />

<p>
<img src="https://i.imgur.com/rQG2uvq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In Active Directory Users and Computers (ADUC), I created an Organizational Unit (OU) called “_EMPLOYEES”
</p>
<br />

<p>
<img src="https://i.imgur.com/nQ5JfIz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I also Created a new Organizational Unit (OU) named “_ADMINS”
</p>
<br />

<p>
<img src="https://i.imgur.com/tUxy5ou.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Created a new employee named “Jane Doe” with the username of “jane_admin” & password of Cyberlab123!
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
