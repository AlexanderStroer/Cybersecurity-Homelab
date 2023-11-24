<h1>LLMNP Poisoning</h1>
<b>
<h2>Description</h2>
This attack takes advantage of the way Windows systems perform name resolution. Impacket's Repsonder can intercept authentication requests to capture plaintext credentials or hashes.
<br />
<br />

<h2>Attack overview:</h2>

 - Mitigation</b>
   - Disabling LLMNR – LLMNR can be turned-off through
the group policy editor, under the “policy setting” menu under<br /> Local Computer Policy > Computer Configuration > Administrative Templates > Network > DNS Client.
   - Disabling NBT-NS – NBT-NS can be turned off through the Network Connection Settings. Navigate to Network Connections > Internet Protocol Version 4 > Properties > General > Advanced > WINS, then select “Disable NetBIOS over TCP/IP”.
<br />

<b>
 
 - Attack
1. </b>Identify the name of your NIC (usually eth0) by typing ifconfig. For me it was eth1
     ![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/851ba128-52e2-4a1c-bc58-475fdd58ea28)
1. Run Responder with the command <i> responder -I eth1 -wd </i>(ignorantly put, this will act almost like a DNS except it will wait the source to fail to resolve a destination upon which responder will falsely claim that it has that information and receive the traffic illegitimately)
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/d8ee2913-92dc-4fde-83da-23b5d970338b)


<b>
You’ll need to install impacket for kali linux, you can find it here: <br />
[Impacket](https://github.com/fortra/impacket)
<br />


</b>

<p align="center">
<h2>Utilities Used</h2>

- <b>VMware Workstation</b>
- <b>Security Onion</b>
- <b>Kali Linux</b>
- <b>Windows Server</b>
- <b>Ubuntu Server (as Splunk)</b>
- <b>Splunk Universal Forwarder</b>
- <b>Responder</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10</b>
- <b>Linux</b>

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

