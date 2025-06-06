
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Log into our DC-1 Virtual Machine
- Install Active Directory Domain Services and set new forest as mydomain.com
- Create a new organizational unit and make admins
- Create users and admins to access the Domain Controller

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When we are logged into the DC-1 VM we want to click on add server roles and then we want to enable Active directory domain services. Now we want to make DC-1 an actual domain controller and give it a new forest. There will be a flag we can click on the top right of the screen from here we can make a new forest, and make the root name mydomain.com. Then you can keep clicking next until the install prompt comes up then finally you can install it. Now we restart our domain controller.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
log back into DC-1 and we are going to create a domain admin user. We are going to go into active directory users and computer and we need to make 3 folders that say ADMINS, EMPLOYEES, and CLIENTS. We will make jane Doe an admin and put it in the admin folder. For this example we will use Jane Doe as an admin and now we can log into the Domain controller as jane doe now because we made her an admin.
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
So now we join client 1 to the domain. So log back into the DC-1 VM from the azure portal as jane doe. We need to go into the computer setting and make DC-1 a domain of mydomain.com. Save and restart so it will be a member of the domain. Now we need to go to the client folder and we can make a client john doe. Then in the employess we can make many employees with powershell.
</p>
<br />
