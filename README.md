<h1>VPN, Honeypots, and Defenses Against IP Spoofing Lab</h1>


<h2>Description</h2>
This lab delves into critical elements of network security, emphasizing the role of Virtual Private Networks (VPNs), honeypots, and defenses against IP spoofing. We analyze the functionality, deployment, and effectiveness of these tools in bolstering network security. Understanding their strengths and limitations aids in constructing robust network defense strategies, crucial for safeguarding sensitive data in today's cyber threat landscape.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Kali Terminal</b> 
- <b>Windows Network and Sharing Center</b>
- <b>Wireshark</b>
- <b>Putty Terminal</b>
- <b>nmap</b>

<h2>VPNs:</h2>
VPNs create encrypted tunnels over public networks, securing data transmission between endpoints. Encrypted data packets ensure confidentiality and integrity, mitigating eavesdropping risks. VPNs are deployed through dedicated hardware or software solutions. Tunneling protocols like IPsec, PPTP, L2TP, and SSL/TLS are commonly used. Configuration involves authentication, encryption settings, and choosing appropriate tunneling protocols. Benefits include secure remote access, privacy preservation, and circumventing geographical restrictions. However, potential limitations encompass increased latency and potential vulnerabilities in VPN protocols. 



<h2>IP Spoofing:</h2>
IP spoofing is the creation of Internet Protocol packets with a false source IP address. This is used to impersonate another computer. Implementing ingress and egress filtering at network boundaries helps in detecting and blocking spoofed IP packets, ensuring legitimate packet flow. Utilizing strong authentication methods, like multi-factor authentication (MFA), prevents unauthorized access and reduces the risk of IP spoofing attempts. Frequent audits and active monitoring of network traffic help in identifying abnormal patterns and potential IP spoofing activities, allowing for timely mitigation. 

<h2>VPN walk-through:</h2>

<p align="center">
Open Network and Sharing Center: <br/>
<img src="https://i.imgur.com/ynIaEQU.png" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
Click Set up a new connection or network link:  <br/>
<img src="https://i.imgur.com/ynIaEQU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Choose a connection option by selecting Connect to workplace and click next: <br/>
<img src="https://i.imgur.com/0ZI65yr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select Use my Internet Connection (VPN):  <br/>
<img src="https://i.imgur.com/DJ6qbmH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Type the Internet address to connect to the step, type the Internet address and click Create:  <br/>
<img src="https://i.imgur.com/QazketM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Under the network pane, you will see the network as VPN Connection:  <br/>
<img src="https://i.imgur.com/8pF1CDi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the Network Sharing Center window click the Change adapter settings link to view VPN Connection on the Network Connection Window:  <br/>
<img src="https://i.imgur.com/v8hgynC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>


<h2>Honeypots:</h2>
Honeypots are decoy systems designed to attract and analyze malicious activities. They mimic vulnerable systems to gather insights into attack techniques, aiding in threat intelligence. Deployment involves configuring and placing honeypots strategically within a network. Different types of honeypots, including low-interaction and high-interaction, can be utilized based on specific goals and risk tolerance. Benefits encompass threat intelligence gathering, early threat detection, and behavior analysis. However, challenges include resource consumption, maintenance efforts, and potential misuse by malicious actors.  

<h2>Setting Up a Honeypot walk-through:</h2>

<p align="center">
Open Terminal: <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
<p align="center">
Open Run command ipconfig  
- Write down the Io int IP address: <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
Run command cd pentbox-1.8/  <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
Run command ./pentbox.rb <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
<p align="center">
In Terminal type 2 and enter to select network tool option: <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
In Terminal type 3 and enter to select Honeypot option:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In Terminal type 2 and enter to select manual config option: <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In Terminal type 443 and enter to select to open port:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In Terminal "Caught You!!” and enter to enter false message:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In Terminal type y and enter twice to save log:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In Terminal type n and enter to deactivate beep sound:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
You will see that the honeypot is on port 443: <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In Terminal type 443 and enter to select to open port:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Open Firefox and type http:// the IP address from earlier:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In this window you will see secure connection failed:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the terminal, you will see a message of Intrusion Attempt Detection:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Press Ctrl+C to stop:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

 <h2>IP Spoofing:</h2>
IP spoofing is the creation of Internet Protocol packets with a false source IP address. This is used to impersonate another computer. Implementing ingress and egress filtering at network boundaries helps in detecting and blocking spoofed IP packets, ensuring legitimate packet flow. Utilizing strong authentication methods, like multi-factor authentication (MFA), prevents unauthorized access and reduces the risk of IP spoofing attempts. Frequent audits and active monitoring of network traffic help in identifying abnormal patterns and potential IP spoofing activities, allowing for timely mitigation. 

<h2>Setting Up a Honeypot walk-through:</h2>

<p align="center">
Open Wireshark and select the Ethernet0 and start capturing packets: <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
<p align="center">
Open PuTTY terminal in the configuration dialog box in the Host Name type 192.168.1.130 and open: <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
Click yes to PuTTY Security Alert prompt:  <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
Login in to the PuTTY Security Alert Prompt <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
<p align="center">
In the terminal execute these commands separately 
   - nmap -iflist 
   - nmap -e ens192 -S 192.168.1.1 192.168.1.250 
Nmap is used by ethical hackers to reform vital scans: <br/>
<img src="" height="80%" width="80%" alt="hello this is reed"/>
<br />
<br />
In Wireshark stop capturing packets:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the display filter box type arp and click the arrow icon: <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Look at the information section for Destination as Broadcast:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the menu bar click the file and save and save as ip_spoof:  <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
