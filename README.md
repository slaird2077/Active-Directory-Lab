<h1>Active Directory Home Lab</h1>
 
<h2>Description</h2>
This is my first attempt at a home lab IT project and is very much a learning experience so bear with me!  I am trying to get familiar with essential programs that will be used in almost every IT environment and gain hands-on experience.  Project consists of a downloading Oracle VM VirtualBox, setting up two virtual machines, and running Active Directory. The first virtual machine will be the Domain Controller and will have Active Directory.  The second will be an end user/client computer.  By the end, I will be able to make policy updates on the Domain Controller and see it take affect on the End User virtual machine. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>Oracle VM Virtual Machine</b>
- <b>Active Directory</b>
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
Allocate the RAM and CPUs that will work best for your computer:  <br/>
<img src="https://i.imgur.com/ZIiItgu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
 Allocate Virtual Hard Disk size (I did 40GB but the default of 20GB should be fine):  <br/>
 <img src="https://i.imgur.com/nmzt01O.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br />
 <br />
 Make sure info looks correct and click "Finish":  <br/>
 <img src="https://i.imgur.com/ZHfc5lC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Before we install Windows Server 2019 on the Domain Controller, click "Settings":  <br/>
 <img src="https://i.imgur.com/Oa92id3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Under "General" and then "Advanced", select "Bidirectional" for Shared Clipboard and Drag'n'Drop - Shared Clipboard allows you to ctrl+c and ctrl+v from your desktop to your VM and Drag'n'Drop allows you to drag files from your desktop to your VM:  <br/>
 <img src="https://i.imgur.com/bG6jDmJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Under "Network" and "Adapter 1", make sure "Enable Network Adapter" is selected and "NAT" is selected - this will act as our Network Interface Card (NIC) and will be how we connect to the internet:  <br/>
 <img src="https://i.imgur.com/fwh9xlV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Under "Adapter 2", click "Enable Network Adapter" and select "Internal Network" under the drop down list:  <br/>
 <img src="https://i.imgur.com/vkaMS3U.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Double-click the Domain Controller VM to start it - It will give you an error saying that it "failed to boot" - Under "DVD" and then "Other", you will have to find where you stored your Windows Server 2019 in File Explorer:  <br/>
 <img src="https://i.imgur.com/whhwPYh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Your Windows 2019 Server ISO file might have a confusing name - select it:  <br/>
 <img src="https://i.imgur.com/BUiAvuU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Once it is loaded into the VM drop down list, click "Mount and Retry Boot":  <br/>
 <img src="https://i.imgur.com/ZG6MHym.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 The virtual machine should start up and you will be prompted to install Windows Server 2019 - click "Install Now" - select the language you need and click "Next":  <br/>
 <img src="https://i.imgur.com/6UMxgRa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Select the "Windows Server 2019 Standard Evaluation (Desktop Experience)" - this will have the graphical user interface (GUI) - click "Next" - accept license agreements:  <br/>
 <img src="https://i.imgur.com/PzcUTJg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Click "Custom: Install Windows only" to install Windows Server 2019:  <br/>
 <img src="https://i.imgur.com/PCwToeS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 On the next screen, Drive 0 should be the only drive listed - click "Next":  <br/>
 <img src="https://i.imgur.com/PLtXnqs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Windows will begin installing on your virtual machine - this should take a while - the virtual machine will reboot - do not press anything during this process:  <br/>
 <img src="https://i.imgur.com/VAw1ve7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 <br/>
 <br/>
 Enter a password for the "Administrator" user account and click "Finish":  <br/>
 <img src="https://i.imgur.com/GJlAV7G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
