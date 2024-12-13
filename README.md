<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create a Resource Group
- Create a Windows 10 Virtual Machine
- Create a Linux Virtual Machine
- Ensure both VM's are in the same Virtual Network/Subnet

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/mp4wCOY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Within Microsoft Azure, we need to create a resource group called NSG (Network Security Groups) Once that resource group is created we need to creat two Azure Virtual Machines.
</p>
<br />

<p>
<img src="https://i.imgur.com/3dGUO9p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will be creating two VM's, first one named DC-1 using Windows Server 2022, second VM will be named Client-1 using Windows 10. Create a username and password for each VM and make sure the region is the same as well. Next, we will login to both VM's using remote desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/cKyCp0A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once we are logged in to both VM's, we will run PowerShell on Client-1 and attempt to ping DC-1's private IP address. Open PowerShell and run ipconfig /all  the output for the DNS settings should show DC-1's private IP address.
</p>
<br />
