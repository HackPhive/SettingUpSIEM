<h1>Install SIEM</h1>

<h2>Description</h2>
A Centralised security monitoring pipeline ingestings Windows Event Logs and Linux Authentication Logs into a Unified Splunk Instance for Threat visibility
<br />


<h2>Tools Used</h2>

- <b>Vmware Fusion Pro</b> 
- <b>Splunk Server and Forwarder</b>

<h2>Environments Used </h2>

- <b>Windows 11 OS</b>
- <b>Kali Linux</b>

<h2>Project Snapshots:</h2>

<p align="center">
Download and Set-up Splunk Server: <br/>
<img src="https://i.postimg.cc/7ZY7HC9k/img1.png" height="80%" width="80%"/>
<br />
<br />
Download and Set-Up Splunk Forwarder on Windows OS:  <br/>
<img src="https://i.postimg.cc/SRhdDSh0/img2.png" height="80%" width="80%" alt="Splunk Forwarder"/>
<br />
<br />
Restart Forwarder after Settings and Creating Username & Password: <br/>
<img src="https://i.postimg.cc/rwK1G0rN/img3.png" height="80%" width="80%" alt="Splunk Forwarder"/>
<br />
<br />
Added Logs Data:  <br/>
<img src="https://i.postimg.cc/V6C1XRfk/img4.png" height="80%" width="80%" alt="Logs Data"/>
<br />
<br />
Configure (C:\Program Files\SplunkUniversalForwarder\etc\system\local\inputs.conf):  <br/>
<img src="https://i.postimg.cc/8PDDrMx2/img5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm Splunk Server receives Logs:  <br/>
<img src="https://i.postimg.cc/hv1k0ZHR/img6.png" height="80%" width="80%" alt="Splunk Server"/>
<br />
<br />
Allow Inbound Traffic on port 9997 to enable Splunk Server receive Logs from other Source:  <br/>
<img src="https://i.postimg.cc/Prc4RQTn/img7.png" height="80%" width="80%" alt="Port Forwarding"/>
<br />
Install and configure Splunk Forwarder on Linux OS:  <br/>
<img src="https://i.postimg.cc/YSJjcjjK/img8.png" height="80%" width="80%" alt="Linux Forwarder"/>
<br />
Confirm Splunk Server Successfully ingested Linux Authentication Logs and Windows Event Logs:  <br/>
<img src="https://i.postimg.cc/B60scFXP/img9.png" height="80%" width="80%" alt="Log Data"/>
<br />
Creating Dashboard for Logs Overview:  <br/>
<img src="https://i.postimg.cc/Qx52SCZW/img10.png" height="80%" width="80%" alt="Dashboard"/>
<br />
Dashboard Overview(Failed Logins, Successful Logins, Admin Login):  <br/>
<img src="https://i.postimg.cc/6QHgTGnh/img11.png" height="80%" width="80%" alt="Dashboard Overview"/>
</p>

<p>
  Summary: In this project I was able to install Splunk Enterprise on Windows OS as both Indexer and search head. I encountered Web User Interface errors during configurations but I was able to fix  it through manual configuration of the inputs.conf. When trying to integrate Linux OS I also encountered error due to the Linux version I was operating, I was able to identify the architecture mismatch (ARM64, not x64).  I enabled the system service for a reliable startup and persistence. 

Data was Successfully collected from Windows OS Event Logs and Linux Authentication showing a real-time cross platform security visibility.
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
