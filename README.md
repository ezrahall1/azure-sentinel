<h1>Azure Sentinel</h1>

<h2>Description</h2>
In this project I will be demonstrating how to set up a cloud based SIEM, as well as virtual machine in the cloud which will be the honeypot. It will be have vulnerabilities to the internet which I will monitor and log the attacks from different ip addresses, from different countries all over the world. I will extract the failed log on data and ingest it into Azure Sentinel and present it on a world map so you can visualize where the attacks are coming from.
<br />


<h2>Services Used</h2>

- <b>Log Analytics Workspace</b>
- <b>Sentinel (SIEM)</b>
- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Azure</b>

<h2>Program walk-through:</h2>
<H3>Step 1 - Create VM</H3>
Once you have log into the Azure account you would need to enter virtual machines in the search field.
  
<img src="https://i.imgur.com/yLaNnxc.png" height="80%" width="80%" alt="Image 1"/>

Click create and select Azure virtual machine and fill in details and click next:disk.

You can leave the disk section as default and click next: networking

In the networking section where it says "NIC network security group" select advanced and click on create new

<img src="https://i.imgur.com/ip3CC17.png" height="80%" width="80%" alt="Image 2"/>  

You would need to remove the inbound rule and add a new one with these details

<img src="https://i.imgur.com/RLkoyjN.png" height="80%" width="80%" alt="Image 3"/>

Click add, then ok.

<img src="https://i.imgur.com/ImpNzBE.png" height="80%" width="80%" alt="Image 4"/>

Click review and create




<H3>Step 2 – Setting up log analytics workspaces </H3>
The next step is to enter log analytics workspaces in the search field

<img src="https://i.imgur.com/MLyNts5.png" height="80%" width="80%" alt="Image 5"/>

The purpose of this feature is to ingest logs from the virtual machine, Windows event logs and to create custom log that contains geographic information to discover where the attackers are coming from.

Click on create log analytics workspaces, select your resource group, enter a name and click review + create

<img src="https://i.imgur.com/Nf0q73D.png" height="80%" width="80%" alt="Image 6"/>


<H3>Step 3 – Microsoft Defender for Cloud</H3>

The  next step is to go to the Microsoft Defender for Cloud. Click on Azure subscriptions and make the following changes

<img src="https://i.imgur.com/rCWsfLB.png" height="80%" width="80%" alt="Image 7"/>


<img src="https://i.imgur.com/AVGNv61.png" height="80%" width="80%" alt="Image 8"/>


<H3>Step 4 – Setting up Sentinel</H3> 

Enter Microsoft Sentinel in the search field and click on Microsoft Sentinel.

Click on create Microsoft Sentinel, and add your workspace


This is the SIEM I will be using to visualize the attack data



<H3>Step 5 – Connect to virtual machine</H3> 

In the log analytic workspace click the name of your workspace and select virtual machine. Click connect to connect to the virtual machine.
From there you would need to head over to the virtual machine section and select your virtual machine that should be available now.

<img src="https://i.imgur.com/Nzt3lgV.png" height="80%" width="80%" alt="Image 9"/>


Once you have clicked on your virtual machine make a note of the public ip address as you would need RDP into it.

<img src="https://i.imgur.com/MJsWroO.png" height="80%" width="80%" alt="Image 10"/>


Once connected to the virtual machine you would need to disable firewall. Go to the start menu and type wf.msc and select. click on Windows Defender Firewall Properties turn off domain profile, private profile off, and public profile and click apply and ok

Open up Powershell ISE and enter commands attached to this project.

<img src="https://i.imgur.com/qvGDNFO.png" height="80%" width="80%" alt="Image 11"/>

<H3>Step 5 – Create custom log</H3>

Head over to the log analytics workspaces page, click on your workspace and select custom logs, click add custom logs

<img src="https://i.imgur.com/O7qwp6t.png" height="80%" width="80%" alt="Image 12"/>

<img src="https://i.imgur.com/uDhPlsq.png" height="80%" width="80%" alt="Image 13"/>

<img src="https://i.imgur.com/mioJrrg.png" height="80%" width="80%" alt="Image 14"/>

<H3>Map of incoming attacks after 6 hours</H3>

<img src="https://i.imgur.com/iYGlutN.png" height="80%" width="80%" alt="Image 14"/>

</p>


