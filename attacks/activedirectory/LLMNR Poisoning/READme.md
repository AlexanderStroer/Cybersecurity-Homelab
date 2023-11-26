<h1>LLMNP Poisoning</h1>

<h2>Description</h2>
LLMNR (Link-Local Multicast Name Resolution) poisoning is an attack that exploits the default behavior of Windows systems in resolving hostnames. In this attack, tools like Impacket's Responder are employed to intercept name resolution requests.

When a Windows system is unable to resolve a hostname using traditional methods such as DNS, it sends out LLMNR requests to the local network. LLMNR poisoning involves responding to these requests with fraudulent information, redirecting the target system to an attacker-controlled system.

Impacket's Responder, a popular tool for LLMNR poisoning, captures authentication requests sent by the target system. This interception allows the attacker to obtain plaintext credentials or hashed passwords, depending on the authentication protocols in use.

By manipulating the name resolution process, LLMNR poisoning creates a stealthy avenue for attackers to harvest sensitive credentials, posing a significant security risk to Windows-based networks. Organizations must be vigilant in implementing countermeasures to mitigate the impact of LLMNR poisoning, such as disabling LLMNR where it is unnecessary and implementing secure authentication practices.<br />
 
<p align="center">
<h2>Utilities Used</h2>
 
- <b>Responder</b>
- <b>Hashcat</b>
- <b>VMware Workstation</b>
- <b>Security Onion</b>
- <b>Kali Linux</b>
- <b>Windows Server 2019 (as Active Directory)</b>
- <b>Ubuntu Server (as Splunk)</b>
- <b>Splunk Universal Forwarder</b>


<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10</b>
- <b>Linux</b>

<h2>Mitigation</h2>
<p>Effectively mitigating SMB Relay Attacks involves implementing security measures to address specific vulnerabilities. Two critical measures include:</p>

<ol>
  <li><strong>Disabling LLMNR:</strong> LLMNR (Link-Local Multicast Name Resolution) can be a potential vulnerability and is recommended to be disabled. Follow these steps to turn it off through the Group Policy Editor:</li>

  <ul>
    <li>Open the Group Policy Editor by navigating to <code>Local Computer Policy &gt; Computer Configuration &gt; Administrative Templates &gt; Network &gt; DNS Client</code>.</li>
    <li>Locate the "Turn Off Multicast Name Resolution" policy setting.</li>
    <li>Enable the policy setting to disable LLMNR.</li>
  </ul>
  <br />

  <li><strong>Disabling NBT-NS:</strong> NBT-NS (NetBIOS Name Service) can pose security risks and should be disabled. Follow these steps to turn it off through the Network Connection Settings:</li>

  <ul>
    <li>Navigate to <code>Network Connections &gt; [Your Network Connection] &gt; Properties &gt; Internet Protocol Version 4 &gt; Properties &gt; General &gt; Advanced &gt; WINS</code>.</li>
    <li>Select "Disable NetBIOS over TCP/IP."</li>
  </ul>
</ol>

<p>By implementing these measures, you can significantly reduce the attack surface and strengthen your defenses against SMB Relay Attacks.</p>


<b>
 
<h2>Attack</h2>

 
You’ll need to install impacket for kali linux, you can find it here: 
[Impacket](https://github.com/fortra/impacket)<br />
<br /><br />


1. Identify the name of your NIC (usually eth0) by typing ifconfig. For me it was eth1
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/851ba128-52e2-4a1c-bc58-475fdd58ea28)<br />
1. Run Responder with the command <i> responder -I eth1 -wd </i>(ignorantly put, this will act almost like a DNS except it will wait the source to fail to resolve a destination upon which responder will falsely claim that it has the requested information and receive the traffic illegitimately)<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/d8ee2913-92dc-4fde-83da-23b5d970338b)<br />
1. Now you'll need to wait for a user to make a mistake; alternatively I can feed that mistake by taking the network path straight to the attacker. Open up file explorer and type \\\ATTACK_MACHINES_IP_HERE<br /> <br />You'll see something like this appear on the victims side.<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/8626effd-5e38-4573-bd08-9c67e9290afe)<br />
<br />And something like this on the attackers side.<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/3581fa7e-7ea4-4391-957b-aa49f2d7a291)
1. Save the the entire hash output into a txt file and move into a directory with a word list. I created a new directory and moved a copy of rockyou.txt into it.<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/1d70574a-ec55-4bbf-8f41-cfd9a2ee16d1)<br />
1. Run the appropriate HashCat command (hint: hashcat --help | grep NTLM)<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/1f8fa93a-3ad1-4243-b07b-c716ef05f281)
1. Hopefully you see success! If not consider using a list from [SecList](https://github.com/danielmiessler/SecLists) on github
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/432f5775-c881-41dc-bac0-a545833cbfd1)


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

