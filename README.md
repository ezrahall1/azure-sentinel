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
The next step is to eneter log analytics workspaces in the search field




<img src="https://i.imgur.com/MLyNts5.png" height="80%" width="80%" alt="Image 5"/>



<H3>Step 3 – Install Jenkins</H3>
To ensure that your software packages are up to date on your instance, use the following command to perform a quick software update:

- [ec2-user ~]$ sudo yum update –y

Add the Jenkins repo using the following command:

- [ec2-user ~]$ sudo wget -O /etc/yum.repos.d/jenkins.repo \https://pkg.jenkins.io/redhat-stable/jenkins.repo

Import a key file from Jenkins-CI to enable installation from the package:

- [ec2-user ~]$ sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
- [ec2-user ~]$ sudo yum upgrade

Install Java:

- [ec2-user ~]$ sudo amazon-linux-extras install java-openjdk11 -y

Install Jenkins:

- [ec2-user ~]$ sudo yum install jenkins -y

Enable the Jenkins service to start at boot:

- [ec2-user ~]$ sudo systemctl enable jenkins

Start Jenkins as a service:

- [ec2-user ~]$ sudo systemctl start jenkins

You can check the status of the Jenkins service using the command:

- [ec2-user ~]$ sudo systemctl status jenkins

<H3>Step 4 – Configure Jenkins</H3>

Jenkins is now installed and running on your EC2 instance. To configure Jenkins:

- Connect to http://<your_server_public_DNS>:8080 from your browser. You will be able to access Jenkins through its management interface:

<img src="https://i.imgur.com/9Jzkg1Q.png" height="80%" width="80%" alt="Image 4"/>

Use the following command to display this password:

- [ec2-user ~]$ sudo cat /var/lib/jenkins/secrets/initialAdminPassword

The Jenkins installation script directs you to the Customize Jenkins page. Click Install suggested plugins.
Once the installation is complete, Create First Admin User, click Save and Continue.



<img src="https://i.imgur.com/7Oo0i0y.png" height="80%" width="80%" alt="Image 5"/>


<img src="https://i.imgur.com/y7c7Dau.png" height="80%" width="80%" alt="Image 6"/>

<img src="https://i.imgur.com/tGHagsx.png" height="80%" width="80%" alt="Image 7"/>

On the left-hand side, click Manage Jenkins, and then click Manage Plugins. Click on the Available tab, and then enter Amazon EC2 plugin at the top right.
Select the checkbox next to Amazon EC2 plugin, and then click Install without restart.

<img src="https://i.imgur.com/cYMCPYv.png" height="80%" width="80%" alt="Image 8"/>

Once the installation is done, click Back to Dashboard.
Click on Configure a cloud.



Click Add a new cloud, and select Amazon EC2. A collection of new fields appears.
Fill out all the fields. (Note: You will have to Add Credentials of the kind AWS Credentials.)

<img src="https://i.imgur.com/7syZfaI.png" height="80%" width="80%" alt="Image 9"/>


</p>


