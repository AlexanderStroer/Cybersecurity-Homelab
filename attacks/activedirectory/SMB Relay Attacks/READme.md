<h1>SMB Relay Attacks</h1>

<h2>Description</h2>
<p>This attack leverages open connections on ports 139 and 445 to exploit vulnerabilities in the Server Message Block (SMB) protocol. SMB is a network file-sharing protocol used for providing shared access to files, printers, and other resources on a network.</p>

<p>SMB Relay Attacks take advantage of legitimate user authentication to compromise systems. When an attacker intercepts SMB traffic, they can redirect it to another target system, tricking it into believing that the attacker is a legitimate user. This can lead to unauthorized access, data theft, and various other security breaches.</p>

<p align="center">
<h2>Utilities Used</h2>

- <b>Responder</b>
- <b>Windows Server 2019 (as Active Directory)</b>


<h2>Environments Used </h2>

- <b>Windows Server 2019</b>
- <b>Windows 10</b>
- <b>Kali Linux</b>

<h2>Mitigation</h2>
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

<h2>Attack</h2>

You may need to run the setup for impacket in order to get the python script to run. <br />
Do this by navigating to the impacket directory and running <code>python setup.py install</code>

<br />
<br />

1. The first step involved creating a file share to open ports 139 and 445. I have documented how to do that on my own notes page; if employers would like to see it they can always ask.<br />

![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/e37fd2ea-ec8e-4a0f-8957-91ac7452fa58)
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/e8f4f31f-0110-4536-b964-c6aa065ceee3)
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/35a525c0-7996-4f35-8d78-cb988016a59b)
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/4bbaa509-143a-4472-b074-9794cb66549a)
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/f178b1e3-3586-4ca6-9fcf-80704b853aa5)
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/9421421e-31c9-446e-9783-18bccbcc7f25)

1. Spawn an interactive shell
![image](https://github.com/AlexanderStroer/Cybersecurity-Homelab/assets/122342684/d9f6f1dc-6661-4187-a916-4c30b6baebe1)

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

