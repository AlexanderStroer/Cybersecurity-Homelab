<h1>IPv6 Attacks</h1>

<h2>Description</h2>
<p>This attack leverages open connections on ports 139 and 445 to exploit vulnerabilities in the Server Message Block (SMB) protocol. SMB is a network file-sharing protocol used for providing shared access to files, printers, and other resources on a network.</p>

<p>This attack was performed with mitm6, which is a pentesting tool that exploits the default configuration of Windows to take over the default DNS server. It does this by replying to DHCPv6 messages, providing victims with a link-local IPv6 address and setting the attackers host as default DNS server. As DNS server, mitm6 will selectively reply to DNS queries of the attackers choosing and redirect the victims traffic to the attacker machine instead of the legitimate server. </p>



<p align="center">
<h2>Utilities Used</h2>

- <b>Active Directory</b>
- <b>mitm6</b>


<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10</b>
- <b>Kali Linux</b>

<h2>Mitigation</h2>
<p>To defend against SMB Relay Attacks, organizations should implement the following security measures:</p>
<ul>
   <li><strong>Enable SMB Signing on all devices:</strong> This will completely stop the attacks but can cause performance issues with file copies.</li>
   <li><strong>Local Admin Restriction:</strong> Another strong recommendation is not giving a computer local admin rights. This can prevent lateral movement but has the potential to increase the amount of service desk tickets.</li>
   <li><strong>Best Practices:</strong> Account tiering (though it may be hard to enforce), Disabling NTLM authentication on network (but if kerberos stops working, windows defaults back to NLTM.</li>

</ul>

<p>By implementing these measures, organizations can significantly reduce the risk of SMB Relay Attacks and enhance the overall security posture of their network.</p>

</b>

<h2>Attack</h2>

### This attack requires Active Directory Certificate Services to be enabled on the domain controller!

<br />
<br />

1. First, spin up a mitm6 session by providing the domain.<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/9320c16d-dd6b-4a80-9580-4dca8db205c8)<br />


1. Secondly, spin up a ntlmrelay attack.<br />
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/0ef286e3-4d4f-417b-ac0d-ecb6e90d287e)<br />




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


