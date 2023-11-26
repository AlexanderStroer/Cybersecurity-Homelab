<h1>SMB Relay Attacks</h1>
<b>

<h2>Description</h2>
<p>This attack leverages open connections on ports 139 and 445 to exploit vulnerabilities in the Server Message Block (SMB) protocol. SMB is a network file-sharing protocol used for providing shared access to files, printers, and other resources on a network.</p>

<p>SMB Relay Attacks take advantage of legitimate user authentication to compromise systems. When an attacker intercepts SMB traffic, they can redirect it to another target system, tricking it into believing that the attacker is a legitimate user. This can lead to unauthorized access, data theft, and various other security breaches.</p>


<h2>Prevention and Mitigation</h2>
<p>To defend against SMB Relay Attacks, organizations should implement the following security measures:</p>
<ul>
   <li><strong>Network Segmentation:</strong> Isolate critical systems from less secure parts of the network to minimize the impact of potential attacks.</li>
   <li><strong>Encryption:</strong> Use encrypted communication channels, such as SMB over VPN, to protect data from interception.</li>
   <li><strong>Disable Unused SMB Versions:</strong> Disable older and less secure versions of SMB and use the latest secure versions.</li>
   <li><strong>Strong Authentication:</strong> Implement multi-factor authentication to enhance user authentication security.</li>
   <li><strong>Regular Audits:</strong> Conduct regular security audits and monitor network traffic for suspicious activities.</li>
</ul>

<p>By implementing these measures, organizations can significantly reduce the risk of SMB Relay Attacks and enhance the overall security posture of their network.</p>

</b>
<p align="center">
<h2>Utilities Used</h2>

- <b>VMware Workstation</b>
- <b>Security Onion</b>
- <b>Kali Linux</b>
- <b>Windows Server 2019 (as Active Directory)</b>
- <b>Ubuntu Server (as Splunk)</b>
- <b>Splunk Universal Forwarder</b>

<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Linux</b>
<h2>Attack overview:</h2>
The first step involved creating a file share to open ports 139 and 445. I have documented how to do that on my own notes page; if employers would like to see it they can always ask.

![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/4bbaa509-143a-4472-b074-9794cb66549a)

</b>



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

