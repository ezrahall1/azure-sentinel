<h1>RDP brute force attempts on VM acting as a honeypot</h1>

<h2>Description</h2>
In this project I will be demonstrating how to set up a cloud based SIEM, as well as virtual machine in the cloud which will be the honeypot. It will be have vulnerabilities to the internet which I will monitor and log the attacks from different ip addresses, from different countries all over the world. I will extract the failed log on data and ingest it into Azure Sentinel and present it on a world map so you can visualize where the attacks are coming from.
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

<h2>YouTube Demonstration </h2>

[Cyber attacks demonstration using Azure Sentinel SIEM](https://youtu.be/sivRjWpcwpw)

<H3>Map of incoming attacks after 6 hours</H3>

<img src="https://i.imgur.com/iYGlutN.png" height="80%" width="80%" alt="Image 14"/>

</p>


