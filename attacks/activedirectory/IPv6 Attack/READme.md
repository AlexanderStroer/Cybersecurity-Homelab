<h1>SMB Relay Attacks</h1>

<h2>Description</h2>
<p>This attack leverages open connections on ports 139 and 445 to exploit vulnerabilities in the Server Message Block (SMB) protocol. SMB is a network file-sharing protocol used for providing shared access to files, printers, and other resources on a network.</p>

<p>SMB Relay Attacks take advantage of legitimate user authentication to compromise systems. When an attacker intercepts SMB traffic, they can redirect it to another target system, tricking it into believing that the attacker is a legitimate user. This can lead to unauthorized access, data theft, and various other security breaches.</p>

<p align="center">
<h2>Utilities Used</h2>

- <b>Responder</b>
- <b>netcat</b>
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

You may need to run the setup for impacket in order to get the python script to run. <br />
Do this by navigating to the impacket directory and running <code>python setup.py install</code>

<br />
<br />

1. The first step involved creating a file share to open ports 139 and 445. I have documented how to do that on my own notes page; if employers would like to see it they can always ask.<br />

![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/e37fd2ea-ec8e-4a0f-8957-91ac7452fa58)



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


