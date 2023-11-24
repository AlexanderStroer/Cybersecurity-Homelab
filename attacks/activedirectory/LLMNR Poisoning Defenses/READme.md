<h1>LLMNP Poisoning</h1>
<b>
<h2>Description</h2>
This attack takes advantage of the way Windows systems perform name resolution. Impacket's Repsonder can intercept authentication requests to capture plaintext credentials or hashes.
<br />
<br />

<h2>Attack overview:</h2>
## Mitigation

- **Disabling LLMNR** – LLMNR can be turned-off through
the group policy editor, under the “policy setting” menu under Local Computer Policy > Computer Configuration > Administrative Templates > Network > DNS Client.
- **Disabling NBT-NS** – NBT-NS can be turned off through the Network Connection Settings. Navigate to Network Connections > Internet Protocol Version 4 > Properties > General > Advanced > WINS, then select “Disable NetBIOS over TCP/IP”.
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

