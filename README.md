<h1>Active Directory Home Lab</h1>
 
<h2>Description</h2>
This is my first attempt at a home lab IT project and is very much a learning experience so bear with me!  I am trying to get familiar with essential programs that will be used in almost every IT environment and gain hands-on experience.  Project consists of a downloading Oracle VM VirtualBox, setting up two virtual machines, and running Active Directory. The first virtual machine will be the Domain Controller and will have Active Directory.  The second will be an end user/client computer.  By the end, I will be able to make policy updates on the Domain Controller and see it take affect on the End User virtual machine. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Lab walk-through:</h2>

<p align="center">
Download and install Oracle VM Virtual Box AND Extension Pack: <br/>
<img src="https://i.imgur.com/fULG1ql.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Download Windows 10 - select 64bit if prompted:  <br/>
<img src="https://i.imgur.com/ezTBkKx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Follow setup steps and remember where you have the Windows 10 on your File Explorer: <br/>
<img src="https://i.imgur.com/vebEfAV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Download Windows Server 2019 - select ISO 64bit - remember where it is in File Explorer:  <br/>
<img src="https://i.imgur.com/Q9s3oNn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open Oracle VM Virtual Box:  <br/>
<img src="https://i.imgur.com/pvqYVWf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Click "New" to create the first virtual machine - name it Domain Controller - select Microsoft Windows and Windows 10 64bit:  <br/>
<img src="https://i.imgur.com/tBDhkxM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
