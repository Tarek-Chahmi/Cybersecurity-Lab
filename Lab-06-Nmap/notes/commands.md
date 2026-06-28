🛠️ Commands Reference


This file contains all Nmap commands executed during Lab 06.



\---



📌 Check Nmap Version



```powershell

nmap --version

```



Purpose:

\- Verify that Nmap is installed correctly.



\---



📌 Basic Host Scan



```powershell

nmap 127.0.0.1

```



Purpose:

\- Discover open TCP ports.

\- Verify that the host is reachable.



\---



📌 Service Detection



```powershell

nmap -sV 127.0.0.1

```



Purpose:

\- Identify services running on open ports.



\---



📌 Operating System Detection



```powershell

nmap -O 127.0.0.1

```



Purpose:

\- Detect the operating system.



\---



📌 Aggressive Scan



```powershell

nmap -A 127.0.0.1

```



Purpose:

\- Version detection

\- OS detection

\- Default NSE scripts

\- Traceroute



\---



📌 Display Network Configuration



```powershell

ipconfig

```



Purpose:

\- Display the local IP address.

\- Identify the subnet mask.

\- Identify the default gateway.



\---



📌 Network Discovery



```powershell

nmap -sn 192.168.1.0/24

```



Purpose:

\- Discover active hosts on the local network.



\---



💾 Save Scan Results



```powershell

nmap 127.0.0.1 > localhost-scan.txt

```



```powershell

nmap -sV 127.0.0.1 > service-detection.txt

```



```powershell

nmap -O 127.0.0.1 > os-detection.txt

```



```powershell

nmap -A 127.0.0.1 > aggressive-scan.txt

```



```powershell

nmap -sn 192.168.1.0/24 > network-discovery.txt

```





🎯 Summary



These commands demonstrate the fundamental reconnaissance capabilities of Nmap:



\- Host discovery

\- Port scanning

\- Service enumeration

\- Operating system detection

\- Network discovery

\- Output redirection

