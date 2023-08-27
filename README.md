<h1>SIEM Cybersecurity Project</h1>

<h2>Description</h2>
Project consists of utilizing an Azure Virtual Machine, Log Analytics Workspace, and Azure Sentinel. The virtual machine I used was then exposed to the internet for attackers to try and get in to. Log Analytics Workspace and Azure sentinel are then utilized to ingest custom logs and create a workbook that displays global attack data (RDP brute force) on world map according to physical location and magnitude of attacks.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Azure Virtual Machine</b>
- <b>Log Analytics Workspace</b>
- <b>Azure Sentinel</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (22H2)

<h2>Program walk-through:</h2>

<p align="center">
Create the Virtual Machine: <br/>
<img src="https://i.imgur.com/N3uWAR7.png" height="80%" width="80%" alt="Creating Virtual Machine"/>
<br />
<br />
Reconfigure firewall to let all traffic in:  <br/>
<img src="https://i.imgur.com/AbXnYET.png" height="80%" width="80%" alt="Allow all in firewall"/>
<br />
<br />
Launch the VM and run PowerShell Script (Make sure Windows defender is off): <br/>
<img src="https://i.imgur.com/xbH8JMp.png" height="80%" width="80%" alt="Launch VM and run PowerShell script"/>
<br />
<br />
Create Log Analytics Workspace and configure Azure Sentinel:  <br/>
<img src="https://i.imgur.com/jH21t4g.png" height="80%" width="80%" alt="Create LAW and Azure Sentinel"/><img src="https://i.imgur.com/e5d36qq.png" height="80%" width="80%" alt="Create LAW and Azure Sentinel"/>
<br />
<br />
Let script run for at least a couple hours, and then filter data using KQL and Azure Sentinel:  <br/>
<img src="https://i.imgur.com/rOPwbn2.jpeg" height="80%" width="80%" alt="Filter Data"/> 
<br />
<br />
Create a world map using workbooks in Azure Sentinel:  <br/>
<img src="https://i.imgur.com/hdyNvdZ.jpeg" height="80%" width="80%" alt="Create World Map"/>
<br />
<br />
Customize the map to your liking and observe the final results:  <br/>
<img src="https://i.imgur.com/UsDDYYD.jpeg" height="80%" width="80%" alt="Final Results"/>
</p>

<h2>Final Thoughts</h2>
This project was very fun and incredibly eye opening. I let this script run overnight for roughly 6 hours or so, and there was nearly 10,000 attack attempts on my VM by the time I woke up. Even within the first 30 minutes my VM was already getting attacked. The VM mainly ended up getting attacked from India and China. I was very surprised to see over 9.3K attack attempts from India alone. This goes to show you how important it is to implement sound authentication controls like MFA. This was very useful for me to get hands on experience with SIEM tools as well as becoming more comfortable with Azure.

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
