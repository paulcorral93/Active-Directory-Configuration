<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Domain Controller/Active Directory in Azure</h1>
This tutorial outlines how to set up a domain controller with Active Directory within Azure Virtual Machines. Active Directory is a Centralized system for managing users and/or computers. It can control permissions and security across an organization. It is a key tool in a Windows-based IT environment. <br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services


<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 11 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Use Azure to create a virtual machine that will be used for a domain controller
- Install Active Directory on the domain controller 


<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1597" height="763" alt="image" src="https://github.com/user-attachments/assets/9c99f5f8-72cb-48ff-b9c0-4f6d8dbbc3b1" />

</p>
<p>
1. Begin by creating a Resource Group in Azure to create a Virtual Machine. 
<p/>
<br />

<p>

</p>
<p>
  2. The Virtual Machine must be running Windows Server. I used Windows Server 11. Save login information so that you can log into the Virtual Machine via Remote Desktop 
</p>
  <br />

<p>

</p>
<p>
Use Remote Desktop to log in to the Virtual Machine. When the Server Manager window opens, click on Add roles and features to install Active Directory. The next step would be to promote the server to a Domain Controller while creating a new forest. The name and password can be anything, but be sure to remember it.
</p>
<br />

<p>

</p>
<p>
Active Directory is now installed and ready to use. 
</p>
<br />
