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

- When prompted restart the server  <br/>
<p align="center">
<img src="https://i.imgur.com/cUWMDDy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/6i72sAa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/3rUJEDI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
