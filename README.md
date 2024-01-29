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

- Step 1 : Enable Packet Capturing on Azure VM
- Step 2 : Generate Traffic Between VMs
- Step 3 : Experiment with NSGs
- Step 4 : Test NSG Rules
- Step 5 : Monitor NSG Logs
- Step 6 : Cleanup Resources
<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install Wireshark:

SSH into the Azure VM where you want to capture traffic.
Install Wireshark using the package manager appropriate for your VM's operating system.
</p>

<p>

  Capture Network Traffic:

Start capturing network traffic on the VM using Wireshark. Specify the network interface to capture (e.g., eth0).
</p>

<p>
  Send Traffic:

Generate traffic between VMs by initiating connections (e.g., ping, HTTP requests) from one VM to another.</p>

<p>
  Observe Capture:

In Wireshark, observe the captured packets to analyze source and destination IP addresses, protocols, and payload.
</p>


<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create NSGs:

Go to the Azure Portal and navigate to the NSG section.
Create NSGs to control inbound and outbound traffic for the VMs. Define rules based on source, destination, ports, and protocols.
</p>

<p>
  Associate NSGs:

Associate the created NSGs with the respective network interfaces of the Azure VMs.</p>

<p>
  Test Inbound Rules:

Adjust NSG inbound rules to allow or deny specific traffic.
Observe the impact on the captured traffic in Wireshark.
</p>

<p>
  Test Outbound Rules:

Modify NSG outbound rules to control traffic leaving the VM.
Analyze Wireshark captures to see the effects of outbound rule changes.</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Enable NSG Flow Logs:

Enable NSG flow logs to capture information about allowed and denied traffic.
</p>

  <p>
  Analyze Logs:

Review NSG flow logs in Azure Monitor to gain insights into traffic patterns and identify any denied connections.</p>

<p>
  Stop Wireshark Capture:

Stop the Wireshark capture on the Azure VM.</p>

<p>
  Remove Resources:

Optionally, remove the Azure VMs and associated resources to avoid ongoing charges.</p>
<br />
