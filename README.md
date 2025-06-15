# siem-internship-phase3

🛡️ APT Detection Simulation Lab (Wazuh + Sysmon + Windows Event Logs)

🎯 Objective
To simulate complex attack scenarios mimicking Advanced Persistent Threats (APT) and train candidates to detect, analyze, and respond using a layered defense strategy.

⚔️ Simulated Scenarios
1- Fileless Malware with PowerShell
A spear-phishing attack leads to remote PowerShell execution without writing payloads to disk.

2- Lateral Movement via RDP Brute Force
A low-privilege user attempts to brute-force RDP access to other servers using stolen credentials.

3- Persistence via Registry Run Keys
An attacker adds a script to the Windows registry to establish persistence after reboot.

4- Credential Dumping and Exfiltration
Simulated credential dumping using access to lsass.exe and exfiltration of credentials.

🧪 Lab Setup
This lab simulates realistic APT activities in a safe and monitored environment using a set of virtual machines.

🔧 Infrastructure Overview

Component|     Role|    	OS/Platform
-------------------------------------------------------------------------
Wazuh Manager|   	Central SIEM and rule engine|  	Kali Linux / Ubuntu
Wazuh Dashboard|	Visual interface for alerts/logs|	  Web UI (Kibana-based)
Windows Victim|  	Target of simulated APT attacks which have sysmon+wazuh agent installed|	 Windows 10/11
Attacker Machine|	Simulates attacker actions|	Kali Linux+windows vm 
