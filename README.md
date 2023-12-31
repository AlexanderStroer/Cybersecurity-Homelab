<h1>Cybersecurity Homelab</h1>

<h2>Description</h2>
In this homelab, VMware Workstation was installed as the hypervisor, serving as the virtualization platform. The next generation firewall, pfSense, was configured to utilize multiple network adapters to implement network segmentation. Security Onion, an integrated solution for IDS, Security Monitoring, and Log Management, was implemented to fortify the defensive capabilities of the lab. Kali Linux was set up to function as the designated attack machine. A Windows Server was configured as a secure Domain Controller, establishing an Active Directory environment. A Windows desktop was integrated into the domain and configured for efficient network communication. Additionally, Splunk was installed and configured on a Ubuntu Server for centralized log aggregation, and the Splunk Universal Forwarder was deployed on a Windows Server to facilitate log forwarding.
<br /><br />
  
My current goal with this project is to invest time into researching and learning to perform common attack methods and then using Splunk and Security Onion to accurately diagnose the issues. I will then demonstrate the understanding I have of these techniques by creating documenting my findings here.<br /><br />

<h2>Attacks Perfomed (so far)</h2>

- <b>Active Directory</b>
  - [LLMNP Poisoning](https://github.com/AlexanderStroer/Cybersecurity-Homelab/tree/main/attacks/activedirectory/LLMNR%20Poisoning)
  - [SMB Relay Attacks](https://github.com/AlexanderStroer/Cybersecurity-Homelab/tree/main/attacks/activedirectory/SMB%20Relay%20Attacks)<br />
<h2>Project overview:</h2>
<p align="center">
  
<b>🎯 Objectives:</b>

  - Establish a comprehensive Cybersecurity Homelab for Detection & Monitoring.
  - Continue progessing my knowledge by performing and monitoring common attacks.

<b>🏆 Key Achievements:</b>

  - Successfully installed VMware Workstation as the hypervisor for virtualization.
  - Configured pfSense firewall for network segmentation and security, utilizing multiple network adapters.
  - Implemented Security Onion as an all-in-one IDS, Security Monitoring, and Log Management solution.
  - Set up Kali Linux as an attack machine with specific network configurations.
  - Configured a Windows Server as a Domain Controller, creating a secure Active Directory environment.
  - Added a Windows desktop to the domain and configured it for network communication.
  - Installed and configured Splunk on a Ubuntu Server for log aggregation.
  - Deployed the Splunk Universal Forwarder on a Windows Server for forwarding logs to the Splunk instance.

<b>🔧 Infrastructure:</b>

  - Installed VMware Workstation 16 Pro for virtualization, providing a scalable and robust environment.
  - Created Virtual Machines for pfSense, Security Onion, Kali Linux, Windows Server, Windows desktops and Ubuntu Server for Splunk.

<b>🌐 Homelab Network Design & Topology:</b>
<br/><br />

<img width="800" height="500" alt="" src="https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/27c5ff48-2f6d-4b1d-87bd-9ed527600e13">
<p align="right">
credit to day cyberwox at cyberwoxacademy.com
</p>

<br />

</b>
<h2>Utilities Used</h2>

- <b>VMware Workstation</b>
- <b>pfSense</b>
- <b>Security Onion</b>
- <b>Kali Linux</b>
- <b>Active Directory</b>
- <b>Ubuntu Server (as Splunk)</b>
- <b>Splunk Universal Forwarder</b>
- <b>Impacket's Responder</b>
- <b>netcat</b>
- <b>HashCat</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Windows Server 2019</b>
- <b>Linux</b>
  - <b>Ubuntu</b>
  - <b>Ubuntu Server</b>
  - <b>Kali</b>

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
