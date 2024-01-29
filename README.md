<h1>RDP brute force attempts on VM acting as a honeypot</h1>

<h2>Description</h2>
In this project, my focus is on demonstrating the implementation of a cloud-based SIEM solution. Additionally, I will set up a virtual machine in the cloud to serve as a honeypot, deliberately exposing vulnerabilities to the internet. My objective is to monitor and log attacks originating from different IP addresses across the globe. Subsequently, I plan to extract the data related to failed logins and integrate it into Azure Sentinel. The final step involves presenting this information on a world map, allowing for a visual representation of the diverse geographical sources of these attacks.
<br />


<h2>Services Used</h2>

- <b>Log Analytics Workspace</b>
- <b>Azure Sentinel SIEM</b>
- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Azure</b>

<h2>Utilities Used</h2>
ipgeolocation.io: IP Address to Geolocation API

<h2>Attacks from South  Korea coming in; Custom logs being output with geodata </h2>

<img src="https://i.imgur.com/x3mLIuG.png" height="80%" width="80%" alt="Image 13"/>

<h2>YouTube Demonstration </h2>

[Cyber attacks demonstration using Azure Sentinel SIEM](https://youtu.be/sivRjWpcwpw)

<H3>Map of incoming attacks after 6 hours</H3>

<img src="https://i.imgur.com/iYGlutN.png" height="80%" width="80%" alt="Image 14"/>

<h2>Learning Outcome</h2>
From completing this project I was  able to understand how Azure Sentinel works and the benefits from using it in your environment.

Azure Sentinel is a scalable, cloud-native security information event management (SIEM) and security orchestration automated response (SOAR) solution. 
Azure Sentinel collects data from different data sources, performs data correlation, data visualization and processed the data in a single dashboard. It helps to collect, detect, investigate and respond to security threats and incidents.



</p>


