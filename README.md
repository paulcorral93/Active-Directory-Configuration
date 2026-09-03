<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Domain Controller/Active Directory in Azure</h1>
This tutorial outlines how to set up a domain controller with Active Directory within Azure Virtual Machines. Active Directory is a Centralized system for managing users and/or computers. It can control permissions and security across an organization. It is a key tool in a Windows-based IT environment. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
      - I also have a step-by-step on how to create a virtual machine located here: (https://github.com/paulcorral93/How-to-create-a-Virtual-Machine)
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
1. Begin by logging in to an Azure account to create a Resource Group in Azure to build a Virtual Machine. 
<p/>
<br />

<p>
<img width="1182" height="726" alt="image" src="https://github.com/user-attachments/assets/1f199216-7a38-4d8a-8489-8674762bda5f" />

</p>
<p>
  2. The name of the Resource Group can be anything; for this tutorial, I will use Active-Directory. For the Region box, it is important to ensure that any Virtual Machines (VMs) have the same region as your resource group. Then click Review + create
</p>
<br />

<p>
<img width="484" height="725" alt="image" src="https://github.com/user-attachments/assets/5b237dc1-d2db-43ab-8f27-dc69f2654fe4" />

</p>
<p>
  3. Click Create.
</p>
<br />

<p>
<img width="1598" height="761" alt="image" src="https://github.com/user-attachments/assets/9629e025-800a-47ec-a762-f1706e2cb74d" />

</p>
<p>
  4. Now that we have a Resource Group in Azure, open the Virtual Machines tab and click Create a Virtual Machine. This VM in particular will be used as a Domain Controller, so we will need to set it up as a Windows Server OS instead of a traditional Windows OS.
</p>
<br />

<p>
<img width="1599" height="761" alt="image" src="https://github.com/user-attachments/assets/c3c5ade3-31c9-42bf-9765-662d910efa06" />

</p>
<p>
  5.  Ensure that the selected Resource Group is the right one. Use whatever Resource Group was created for the Domain Controller. As for the name of the Virtual Machine, type any name as needed. For this guide, I named it Domain Controller.
</p>
<br />

<p>
<img width="1597" height="763" alt="image" src="https://github.com/user-attachments/assets/bf52b092-594f-4f93-b7a7-21ff926c8364" />

</p>
<p>
      6. Scroll down until you see the input box for Image. Click the Box and select Windows Server Data Center Azure Edition- x64 Gen2 2025. Next, we will click on the Size box and select: D2ads_v7 2 VCPU 8 GiB RAM 
</p>
<br />

<p>
<img width="1210" height="730" alt="image" src="https://github.com/user-attachments/assets/7b45d2af-f2cd-40e0-94cb-08390077ef13" />

</p>
<p>
      7. Scroll down until you see Administrator Account. Fill out this area with the credentials for logging into the VM.
</p>
<br />

<p>
<img width="1213" height="727" alt="image" src="https://github.com/user-attachments/assets/e85768ff-ec07-43e8-a883-a950e599df20" />

</p>
<p>
      8. Click to check the box that says: Use an existing Windows Server license. Also click to check: I confirm, followed by the: Review and Create, to continue
</p>
<br />

<p>
<img width="1195" height="726" alt="image" src="https://github.com/user-attachments/assets/4e569f8f-0063-484e-ba14-b62a1fc3f8b0" />

</p>
<p>
      9. Click Create to finalize the VM. This may take a few minutes.
</p>
<br />

<p>
<img width="1593" height="769" alt="image" src="https://github.com/user-attachments/assets/459488f8-b36e-4ca3-aab9-838a30b846c0" />

</p>
<p>
      9. Go back to the Azure homepage and double-click on the VM tab.
</p>
<br />

<p>
<img width="1589" height="762" alt="image" src="https://github.com/user-attachments/assets/ca276250-11dc-4d6f-9dcc-470a63e45b25" />

</p>
<p>
      9. Grab the Public IP address displayed on the right side of the window: 20.84.120.172. Write this down on a Post-it note or notes app on a phone or tablet; you will use this later to access the Domain Controller.
</p>
<br />


<p>
<img width="867" height="808" alt="image" src="https://github.com/user-attachments/assets/b9b84bc8-9331-4be0-966e-5c6d1b93bde9" />

</p>
<p>
      10. Open the Start Menu on your computer and in the search bar type Remote Desktop Connection. Run the Application to continue.     
</p>
<br />

<p>
<img width="435" height="520" alt="image" src="https://github.com/user-attachments/assets/7b0225bb-77f6-49d2-9380-6ee43ede7477" />
     
</p>
<p>
      11.  To fill in the Computer section, you will need to grab the Public IP address from the Domain Controller we created in Azure. See steps () 
      Verify that the window is expanded to show options, and enter the VM username. Click OK. The next window will ask for the password created for the VM. Enter it and click OK.
</p>
<br />

<p>
<img width="404" height="401" alt="image" src="https://github.com/user-attachments/assets/00d1949c-6230-4de8-b71a-265c691170dc" />

</p>
<p>
      10.   Click Yes
</p>
<br />

<p>
<img width="827" height="791" alt="image" src="https://github.com/user-attachments/assets/fa870db6-b61b-4521-b83c-3e2c2353ecb0" />

</p>
<p>
  3. Now that we are inside the VM, we will install Active Directory on it. Click the Start menu in the VM and search for Server Manager. Double-click to run the program 
</p>
<br />

<p>
<img width="1580" height="848" alt="image" src="https://github.com/user-attachments/assets/8fd1ec91-d321-415d-b22b-e626a8a47a0d" />

</p>
<p>
  3. Click Add Roles and Features.
</p>
<br />

<p>
<img width="828" height="593" alt="image" src="https://github.com/user-attachments/assets/f393c14c-ad85-4c55-97de-76479b2f326d" />

</p>
<p>
  3. Ensure Role-based or Feature-based is selected, and click Next.
</p>
<br />

<p>
<img width="804" height="582" alt="image" src="https://github.com/user-attachments/assets/93694abc-129a-4df4-80be-34aa2a688ae6" />

</p>
<p>
  3. Ensure that the VM server we created is the one selected, and click Next.
</p>
<br />

<p>
<img width="801" height="585" alt="image" src="https://github.com/user-attachments/assets/8577cf57-2a21-4c1d-88ee-110437808454" />

</p>
<p>
  3. Select the box for Active Directory Domain Services, and a window should pop up.
</p>
<br />

<p>
<img width="821" height="588" alt="image" src="https://github.com/user-attachments/assets/1657aa50-24be-4cb0-9957-9062efcb7981" />

</p>
<p>
  3. Click Add Features.
</p>
<br />

<p>
<img width="811" height="585" alt="image" src="https://github.com/user-attachments/assets/1b0c3a58-f6ef-4157-be05-5e5e8364326e" />

</p>
<p>
  3. It will return to this page when selected. Click Next.
</p>
<br />

<p>
<img width="822" height="591" alt="image" src="https://github.com/user-attachments/assets/e4d3583f-bf32-41fb-a7b1-c5f4e0964812" />

</p>
<p>
  3. Click Create.
</p>
<br />

<p>
<img width="822" height="591" alt="image" src="https://github.com/user-attachments/assets/e4d3583f-bf32-41fb-a7b1-c5f4e0964812" />

</p>
<p>
  3. Click Create.
</p>
<br />
