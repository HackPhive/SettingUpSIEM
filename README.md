<h1>Phishing Analysis</h1>

<h2>Introduction</h2>
Phishing analysis is the process of examining suspicious emails, messages, websites, or files to determine whether they are part of a phishing attack. Phishing itself is a type of cyberattack in which attackers impersonate trusted organizations or individuals to trick victims into revealing sensitive information such as passwords, credit card numbers, or personal data. Because phishing is one of the most common forms of social engineering, analyzing these threats is an important task in cybersecurity.
The goal of phishing analysis is to identify malicious indicators, understand how the attack works, and prevent further compromise. Analysts typically investigate elements such as email headers, sender addresses, embedded links, attachments, and the language used in the message. They may also examine domain registrations, website behavior, and malware that might be delivered through phishing campaigns.

By performing phishing analysis, security professionals can detect threats early, warn potential victims, and improve organizational defenses. The insights gained from analysis also help in developing better email filtering systems, user awareness programs, and incident response strategies to reduce the impact of phishing attacks.
<br />


<h2>Tools Used</h2>

- <b>VMware Workstation Pro</b> 
- <b>MXToolbox</b>
- <b>VirusTotal</b>
- <b>WHOIS</b>
- <b>urlscan.io</b>
- <b>Thunderbird</b>

<h2>Environments Used </h2>

- <b>Windows 11 OS</b>

<h2>Project Snapshots:</h2>

<p align="center">
Taking a Snapshot of the VM is necessary as it allows me to restore my VM to clean state in the event the attachment executes a malicious code: <br/>
<img src="https://i.postimg.cc/90QN2SCp/1_VM_Snapshot.png" height="80%" width="80%"/>
<br />
<br />
Page containt Phishing email attachements .eml for analysis:  <br/>
<img src="https://i.postimg.cc/K4XLfkqM/Screenshot-2026-03-08-at-9-40-21-PM.png" height="80%" width="80%" alt="Email"/>
<br />
<br />
After Downloading the attachment, I used Thunderbird to view the content of the email: <br/>
<img src="https://i.postimg.cc/T2jDvw4S/Screenshot-2026-03-09-at-12-03-14-PM.png" height="80%" width="80%" alt="Thunderbird"/>
<br />
<br />
Extracted the email header and analyzed it using MX ToolBox:  <br/>
<img src="https://i.postimg.cc/PxHThtCV/Screenshot_2026_03_09_at_12_05_50_PM.png" height="80%" width="80%" alt="MxToolBox"/>
<img src="https://i.postimg.cc/sXzsyVM0/Screenshot_2026_03_09_at_12_09_54_PM.png" height="80%" width="80%" alt="MxToolBox"/>
<br />
<br />
Investigated Sender's IP Using Virustotal 1 vendor flagged IP as Malware:
<br />
<br/>
<img src="https://i.postimg.cc/t7QLdkFM/Screenshot-2026-03-09-at-12-06-11-PM.png" height="80%" width="80%" alt="Virustotal"/>
<br />
I extracted the Phishing Link in the attachment and Scanned with URLS scan, as at the time of scanning the domain could not be resolved this is also common with domains used for phishing as most of them gets taken down after being flagged by multiple vendors:  <br/>
<img src="https://i.postimg.cc/bJng0hLG/Screenshot-2026-03-09-at-12-09-46-PM.png" height="80%" width="80%" alt="URLscan"/>
<br />
<br />
As expected, checking the reputation of the Link using Virustotal, 1 vendor flagged it as Phishing:  <br/>
<img src="https://i.postimg.cc/bvxd1Vb4/Screenshot-2026-03-09-at-12-08-08-PM.png" height="80%" width="80%" alt="Virustotal"/>
<br />
</p>


<h2>IOCs</h2>

- <b>Spoofed Email Sender: sues[@]nnwifi[.]com</b> 
- <b>Subject : Warning [Threat]</b>
- <b>Attachment : Present</b>
- <b>Link : Present</b>

<h2>Skills Demonstrated </h2>

- <b>Email header analysis</b>
- <b>Threat intelligence lookups</b>
- <b>URL reputation analysis</b>
- <b>Attachment malware analysis</b>
- <b>OSINT investigation</b>
- <b>Incident reporting</b>

<h2>Summary </h2>
<p>
This project simulated a real-world SOC investigation of a phishing email within a controlled virtual environment using VMware Workstation Pro. The email was analyzed by reviewing its content, extracting and examining the header using MXToolbox, and investigating the embedded URL with threat intelligence tools such as VirusTotal and urlscan.io.
The analysis identified multiple Indicators of Compromise (IOCs), including a spoofed sender domain and a malicious phishing link designed to harvest user credentials. The attack was mapped to T1566.002 – Spearphishing Link within the MITRE ATT&CK framework, demonstrating practical SOC analyst skills in phishing detection, threat intelligence analysis, and incident documentation.
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
