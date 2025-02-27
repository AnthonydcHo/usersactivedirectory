<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Creating Users, Group Policy, and Managing Accounts with Active Directory </h1>


<h2>Description</h2>
Configure Remote Desktop for non-administrative users, automated user creation with PowerShell, and managed group policies.
<br/>
<br />

<br />

This is a continuation of the [Active Directory - Deployment/Post-Installation Configuration](https://github.com/AnthonydcHo/addeployment) project
<br />


<h2>Environments and Utilities Used</h2>

- <b>Microsoft Azure</b>
- <b>Virtual Machines</b>
- <b>Remote Desktop Connection</b>
- <b>Active Directory</b>

<h2>Operating Systems Used </h2>

- <b>Windows Server </b>
- <b>Windows 10</b>

<h2>Project Walk-through:</h2>

Setup Remote Desktop for non-administrative users on Client-1
—
Log into Client-1 as mydomain.com\jane_admin (masOs or Windows)
<p align="center">  
<img src="https://i.imgur.com/sFs92X0.png" height="80%" width="80%"
<p align="center">  


Open system properties: </b> 
<p align="center">
<img src="https://i.imgur.com/si9YI0X.png" height="80%" width="80%" 
<p align="center">

Click “Remote Desktop”
	-(in settings)
<p align="center">
<img src="https://i.imgur.com/G6BSSrD.png" height="80%" width="80%" 
<p align="center">
    
Allow “domain users” access to remote desktop 
	-(in settings)
<p align="center">
<img src="https://i.imgur.com/PeqBASu.png" height="80%" width="80%"  
<p align="center">

type domain users
<p align="center">
<img src="https://i.imgur.com/wLojVnS.png" height="80%" width="80%" 
<p align="center">

    
You can now log into Client-1 as a normal, non-administrative user now!


Normally you’d want to do this with Group Policy that allows you to change MANY systems at once (maybe a future lab)


Create a bunch of additional users and attempt to log into client-1 with one of the users:



Login to DC-1 as jane_admin (masOS or windows):
<p align="center">
<img src="https://i.imgur.com/ChgVf3A.png" height="80%" width="80%" 
<p align="center">



Open PowerShell_ise as an administrator:
<p align="center">
<img src="https://i.imgur.com/xp6FV6O.png" height="80%" width="80%" 
<p align="center">


Create a new File and paste the contents of the [script](https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1) into it
    > click script above 
        > copy raw file:
<p align="center">
<img src="https://i.imgur.com/MuHdSLM.png" height="80%" width="80%" 
<p align="center">


Create new file in powershell:
<p align="center">
<img src="https://i.imgur.com/HQwXjzk.png" height="80%" width="80%" 
<p align="center">

Save to desktop as create-users:
<p align="center">
<img src="https://i.imgur.com/wCSB38V.png" height="80%" width="80%" 
<p align="center">

Paste script:
<p align="center">
<img src="https://i.imgur.com/slOSKIu.png" height="80%" width="80%" 
<p align="center">



Run the script and observe the accounts being created:
<p align="center">
<img src="https://i.imgur.com/TQbcpr0.png" height="80%" width="80%" 
<p align="center">


When finished, open Active Directory Users and Computers and observe the accounts in (_EMPLOYEES):
<p align="center">
<img src="https://i.imgur.com/UoxG7Ih.png" height="80%" width="80%" 
<p align="center">


Attempt to log into Client-1 with one of the accounts in macOs or windows (take note of the password in the script, which is password1). We can use gig.foc account:
<p align="center">	
<img src="https://i.imgur.com/UoxG7Ih.png" height="80%" width="80%" 
<p align="center">

<p align="center">
<img src="https://i.imgur.com/K2eJRXE.png" height="80%" width="80%" 
<p align="center">

<p align="center">
<img src="https://i.imgur.com/xr8hXb8.png" height="80%" width="80%" 
<p align="center">

We've successfully configured Remote Desktop for non-administrative users, automated user creation with PowerShell, and managed group policies! <br/>
