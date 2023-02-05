<h1>JActive Directory Lab</h1>


<h2>Description</h2>
In this step-by-step guide, I went through the process of setting up a laboratory environment for Active Directory using Oracle VirtualBox. By configuring and running this lab, I was able to gain a deeper understanding of how Active Directory and Windows networking operates.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Server 2019</b>

<h2>Lab Overviewh:</h2>

<p align="center">
This is the guide im going to go by: <br/>
<img src="https://i.imgur.com/xPc5Vp2.png[/img" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
1. I downloaded Oracle VM to host my virtual machines. I had two different operating matchines within Oracle (Windows 10 ISO and Windows Server 2019 ISO) 
2. The first VM I created was the Domain Controller where it housed the Active Directory. This VM had two network adapters, one for the outside internet and the other was for my virtualbox private network where the clients are going to connect to.
3. After it's installed Im going to connect that VM to Server 2019 and assigned it with IP addresses for my internal network, the external network got a automatic IP address from my home network. 
After I got the Server set up and named, I downloaded and installed Active Directory and created a domain.
After finishing that I configured NAT and routing so the clients on the private network can reach the internet throught the domain controller.
Last step in the Server 2019 VM I set up a DHCP on the Domain Controller so when I create my Windows 10 Machine it can automataclly get an IP address.
The last thing to do on the Domain Matchine is to run a Powershell Strip that will automatcally create users in Active Directory. 

After all of that was finished I created my client vm and installed Windows 10 on it and this VM will be connected to the private vm network and then im going to 
