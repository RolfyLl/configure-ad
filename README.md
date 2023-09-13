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

- Setup Resources in Azure
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory
- Create an Admin and Normal User Account in AD
- Join Client-1 to your domain (RolphyLluveres.com)
- Setup Remote Desktop for non-administrative users on Client-1
- Create a bunch of additional users and attempt to log into client-1 with one of the users

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/EJ0r7Sw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, I started with Creating the Domain Controller VM (Windows Server 2022) named “DC-1”
Set the Domain Controller’s NIC Private IP address to be static. Then i
Create the Client VM (Windows 10) named “Client-1”. Used the same Resource Group and Vnet that was created with DC-1. I
Ensure that both VMs are in the same Vnet.
</p>
<br />

<p>
<img src="https://i.imgur.com/zxSd3o3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/NfZS6Vt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I Logged in to the Domain Controller and enabled ICMPv4 on the local Windows firewall. I Check back at Client-1 to see if the ping succeeds.

</p>
<br />

<p>
<img src="https://i.imgur.com/Yoh73qQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hbj7efr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/01I31vA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this part of the lab, I downloaded Active Directory Domain Services. Set up a new forest as RolphyLluveres.com, restart, and log back into DC-1 as a user. 
</p>
<br />

<p>
<img src="https://i.imgur.com/OdqetLD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/KzGrjzm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/8wj9lDc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
</p>
<p>
In Active Directory Users and Computers (ADUC), I created two Organizational Unit (OU) called
 
  - _EMPLOYEES
  - _ADMINS

Create a new employee named “Hector Troy” with the username of “Hector_admin”
Add Hector_admin to the “Domain Admins” Security Group
Log out/close the Remote Desktop connection to DC-1 and log back in as “RolphyLluveres.com\jane_admin”
User Hector_admin was my admin account from now on.

</p>
<br />

<p>
<img src="https://i.imgur.com/xscFRa7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/AWosORO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, I started with Creating the Domain Controller VM (Windows Server 2022) named “DC-1”
Set the Domain Controller’s NIC Private IP address to be static. Then i
Create the Client VM (Windows 10) named “Client-1”. Used the same Resource Group and Vnet that was created with DC-1. I
Ensure that both VMs are in the same Vnet.
</p>
<br />

<p>
<img src="https://i.imgur.com/EJ0r7Sw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, I started with Creating the Domain Controller VM (Windows Server 2022) named “DC-1”
Set the Domain Controller’s NIC Private IP address to be static. Then i
Create the Client VM (Windows 10) named “Client-1”. Used the same Resource Group and Vnet that was created with DC-1. I
Ensure that both VMs are in the same Vnet.
</p>
<br />

<p>
<img src="https://i.imgur.com/EJ0r7Sw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First, I started with Creating the Domain Controller VM (Windows Server 2022) named “DC-1”
Set the Domain Controller’s NIC Private IP address to be static. Then i
Create the Client VM (Windows 10) named “Client-1”. Used the same Resource Group and Vnet that was created with DC-1. I
Ensure that both VMs are in the same Vnet.
</p>
<br />
