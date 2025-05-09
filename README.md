<h1>Renaming Windows PC and Installing Active Directory Domain Services</h1>

 

<h2>Description</h2>
This lab focused on preparing a Windows Server for domain management by first renaming the PC to match standard naming conventions, then installing the Active Directory Domain Services (AD DS) role. Completing this setup allowed the system to become a Domain Controller, laying the groundwork for managing users, computers, and group policies in a centralized environment—an essential part of enterprise IT infrastructure.
<br />


<h2>Utilities Used</h2>

- <b>Windows Server 2016</b> 
- <b>File Explorer</b>
- <b>Server Manager</b>
- <b>System Properties</b>

<h2>Environments Used </h2>

- <b>Windows Server 2016</b> 
- <b>VirtualBox</b> 
<h2>Walk-through:</h2>

<b>Step 1: Log into Windows server & Change Windows Server Name</b>

- Login into the Windows server through VirtualBox and navigate to “File Explorer” application and open it up.

- In “File Explorer” on the left hand side of the menu, right click on “This PC” and select the “Properties” tab. This is where we have the ability to change the name of the server. <br/>
<p align="center">
<img src="https://i.imgur.com/bFWHJtc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
 [Take a look at the System information and you will get the important info in regards to the Windows]
 
 
- On the right hand side of the display page, under the Computer name, domain, and workgroup settings tab you will see the option to change settings. Click on “change settings”.

- As you can see the default computer name is long and we are going to change it and make more personable.  <br/>
<p align="center">
<img src="https://i.imgur.com/bAjUzEF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
 [The System Properties tab has functionalities that will allow you to make changes to the Window server. For now all we are concerned with is changing the name.]

 - Click “change” <br/>
<p align="center">
<img src="https://i.imgur.com/iSlIVBZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


- Enter your desired name, leave the rest of the settings on the default and select ok  <br/>
<p align="center">
<img src="https://i.imgur.com/PKNLJGA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Click "OK"  <br/>
<p align="center">
<img src="https://i.imgur.com/cUWMDDy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- When prompted restart the server
<p align="center">
<img src="https://i.imgur.com/6i72sAa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
 [The changes will take place after you restart the server]

- After restarting the server and logging back in. Navigate to the file explorer and you should see the server/computer name updated to the one you chose!  <br/>
<p align="center">
<img src="https://i.imgur.com/3rUJEDI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
[The computer is now renamed]

<b>Step 2: Add Roles and Features for Active Directory</b>
- Open Server Manager from the bottom menu, Click on the Manage tab and select “Add roles and features”
 <p align="center">
<img src="https://i.imgur.com/8EtPWGU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
 [The Add Roles and Features Wizard allows for installation of services and features that can you provide all the proper resources an organization needs to thrive successfully.]
 
 - Click “Next”
 <p align="center">
<img src="https://i.imgur.com/nUytOds.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Select the “Role-based or feature-based installation”.
 <p align="center">
<img src="https://i.imgur.com/gnJs8La.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
- Select the server of your choice. (In this matter there is only one server).
- Click “Next”
 <p align="center">
<img src="https://i.imgur.com/DVzfcJy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Under server roles select the option for “Active Directory Domain Services”. You will see by default other roles that will be part of the installation, do not worry about them we are only concerned with getting Active Directory Domain Services on our server.
- Click “Next”
<p align="center">
<img src="https://i.imgur.com/iXOy6Q4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - Click “Next”
<p align="center">
<img src="https://i.imgur.com/L1urWNg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Click “Next”
<p align="center">
 <img src="https://i.imgur.com/QjULnaz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- The installation confirmation page will display all roles and services that will be installed.
- Click “Install”. The installation will take anywhere between 5–10mins depending on your system settings. The system will automatically restart the server to apply all the new changes!
<p align="center">
<img src="https://i.imgur.com/Bo6N6Hv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Server is restarting and applying all the new changes. Once logged back in, Active Directory Domain Services will be installed on the server.
<p align="center">
<img src="https://i.imgur.com/urBVQpY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 - The Active Directory Domain Services needs a domain controller and since we do not have one we will promote our server as the controller.
- For context, Active Directory Domain Services is like a digital manager for computer stuff. It helps control who can use computers in a big group, like a school or a company. It keeps track of usernames, passwords, and what people are allowed to do on the computers. It’s kind of like a gatekeeper that keeps everything organized and secure.
- A domain controller is like a boss computer in charge of a group of computers. It decides who’s allowed to use the computers, keeps everyone’s info safe, and makes sure things run smoothly in an organization.
- Click on “Promote this server to a domain controller” highlighted in blue.
<p align="center">
<img src="https://i.imgur.com/x0xCHom.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<b>Step 3: Active Directory Domain Services Configuration</b>

- For the deployment operation we will create a new forest and create a demo domain name for this server.
- A “forest” is a collection of connected computer networks. These networks share the same rules and security, making it easier to manage users and resources across them. It’s like a digital community of computer neighborhoods, all under one management system.
- I chose my name as the domain name. Create your own.
- Click “Next”
<p align="center">
<img src="https://i.imgur.com/5Bj3XiP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><p align="center">
<p align="center">
[Make sure to include ".local",".net", etc. in the root domain name or it will not let you continue]
 <img src="https://i.imgur.com/x0xCHom.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><p align="center">
<img src="https://i.imgur.com/x0xCHom.png" height="80%" width="80%" alt="Disk Sanitization Steps"/><p align="center">
<img src="https://i.imgur.com/x0xCHom.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  
  <!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
