\# Lab 06 – Nmap Network Discovery

🎯 Objective

🖥️ Environment

📚 Concepts Covered

🛠️ Commands Executed

📊 Results

📸 Screenshots

🗺️ Diagram

🎓 Key Learnings

🔒 Security Recommendations

✅ Conclusion



🎯 Objective



Learn the fundamentals of network reconnaissance using Nmap by scanning the local machine and the local network. This lab introduces essential techniques used during the reconnaissance phase of penetration testing and security assessments.



🖥️ Environment



\*\*Operating System\*\*



\- Windows 11



\*\*Tool\*\*



\- Nmap 7.99



\*\*Targets\*\*



\- Localhost (127.0.0.1)

\- Local Network (192.168.1.0/24)



📚 Concepts Covered



\- Host Discovery

\- Port Scanning

\- Service Detection

\- Operating System Detection

\- Aggressive Scan

\- Network Discovery

\- Basic Network Topology



🛠️ Commands Executed



1\. Verify Installation



```powershell

nmap --version

```



📌 Purpose Purpose



Verify that Nmap is correctly installed and accessible from PowerShell.



📊 Results



Nmap version 7.99 successfully detected.



\---



2\. Basic Host Scan



```powershell

nmap 127.0.0.1

```



📌 Purpose Purpose



\- Verify that the host is reachable.

\- Identify open TCP ports.



📊 Results



Open ports detected:



\- TCP 135 (MSRPC)

\- TCP 445 (Microsoft-DS)

\- TCP 5357 (WSDAPI)



\---



3\. Service Detection



```powershell

nmap -sV 127.0.0.1

```



📌 Purpose Purpose



Identify the services running on each open port.



📊 Results



Detected services:



\- Microsoft Windows RPC

\- Microsoft HTTPAPI 2.0

\- Microsoft SMB



\---



4\. Operating System Detection



```powershell

nmap -O 127.0.0.1

```



📌 Purpose Purpose



Identify the operating system of the target.



📊 Results



Operating System detected:



\- Microsoft Windows 11

\- Version 24H2–25H2



\---



5\. Aggressive Scan



```powershell

nmap -A 127.0.0.1

```



📌 Purpose Purpose



Perform advanced enumeration including:



\- Service Detection

\- Version Detection

\- Operating System Detection

\- NSE Scripts

\- SMB Information



📊 Results



Additional information collected:



\- HTTP Server Header

\- SMB Security Mode

\- SMB Time

\- Microsoft HTTPAPI



\---



6\. Network Configuration



```powershell

ipconfig

```



📌 Purpose



Identify the local network configuration before scanning the subnet.



📊 Results



\- IP Address: 192.168.1.31

\- Subnet Mask: 255.255.255.0

\- Default Gateway: 192.168.1.1



\---



7\. Network Discovery



```powershell

nmap -sn 192.168.1.0/24

```



📌 Purpose Purpose



Discover active hosts on the local network.



📊 Results



| IP Address | Device |

|------------|---------------------------|

|192.168.1.1|Huawei Router|

|192.168.1.8|Unknown Device|

|192.168.1.31|Windows 11 Laptop|



\---



📸 Screenshots



The following screenshots are available in:



```

Lab-06-Nmap/

└── screenshots/

```



\- 01-nmap-version.png

\- 02-basic-scan.png

\- 03-service-scan.png

\- 04-os-detection.png

\- 05-aggressive-scan.png

\- 06-ipconfig.png

\- 07-network-discovery.png



🗺️ Diagram



Network topology diagram:



```

Lab-06-Nmap/

└── diagrams/

\\\&#x20;   └── network-topology.drawio

```



🎓 Key Learnings



During this lab, I learned how to:



\- Install and verify Nmap.

\- Scan a host.

\- Identify open ports.

\- Detect running services.

\- Detect the operating system.

\- Discover devices on a local network.

\- Create a basic network topology diagram.

\- Interpret Nmap scan results.



🔒 Security Recommendations



\- Disable unnecessary services.

\- Restrict SMB access whenever possible.

\- Regularly scan internal networks to identify exposed services.

\- Keep operating systems and applications fully updated.

\- Monitor newly discovered devices connected to the network.



✅ Conclusion



This lab introduced the core functionalities of Nmap, one of the most widely used network reconnaissance tools in cybersecurity. By performing host discovery, service enumeration, operating system detection, and local network mapping, I gained practical experience with techniques commonly used during vulnerability assessments and penetration testing engagements. 

