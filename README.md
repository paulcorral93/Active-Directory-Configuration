<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Domain Controller/Active Directory in Azure</h1>
This tutorial outlines how to set up a domain controller with Active Directory within Azure Virtual Machines.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services


<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Use Azure to create a domain controller
- Install Active Directory on the domain controller 


<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1598" height="763" alt="Screenshot 2026-08-13 214629" src="https://github.com/user-attachments/assets/e7f54f3a-94cf-472f-9ddc-c15b8e7cb305" />
<img width="1599" height="765" alt="Screenshot 2026-08-13 214038" src="https://github.com/user-attachments/assets/acea72eb-820f-4a1c-8b98-c2f14761786b" />
<img width="1599" height="762" alt="Screenshot 2026-08-13 213958" src="https://github.com/user-attachments/assets/544ad00a-783b-4dec-90ce-30ef61330530" />

</p>
<p>
Create a Resource Group in Azure to create a Virtual Machine and a Virtual Network. The Virtual Machine must be running Windows Server. I used Windows Server 11. Save login information so that you can log into the Virtual Machine via Remote Desktop 
<br />

<p>
<img width="404" height="481" alt="Screenshot 2026-08-13 223539" src="https://github.com/user-attachments/assets/7169706e-e13c-4abc-85e1-1c12541c8021" />
<img width="1392" height="659" alt="Screenshot 2026-08-14 172316" src="https://github.com/user-attachments/assets/bedd0630-02da-4d4d-8df5-8c8a9be4bdc0" />
<img width="582" height="427" alt="Screenshot 2026-08-14 171343" src="https://github.com/user-attachments/assets/9a8b2f4f-fddb-45e9-90d1-95767c9301db" />
<img width="583" height="424" alt="Screenshot 2026-08-14 171613" src="https://github.com/user-attachments/assets/cc6c4bf4-2b75-4062-9c39-b461258ac100" />

</p>
<p>
Use Remote Desktop to log in to the Virtual Machine. When the Server Manager window opens, click on Add roles and features to install Active Directory. The next step would be to promote the server to a Domain Controller while creating a new forest. The name and password can be anything, but be sure to remember it.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
