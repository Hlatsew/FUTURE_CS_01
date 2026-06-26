Browser Developer Tools
purpose: Inspect HTTP security header and cookies configurations.
Evidance: [Browser Developer Tools] (evidence/missing headers using browser developer tools)

Nmap port scan
purpose: perform basic network exposure analysis by scannong the target website for publicly accessible TCP ports.
Evidence:[Nmap scan](Evidence/Nmap output)
Starting Nmap 7.99 ( https://nmap.org ) at 2026-06-25 16:44 +0200
NSE: Loaded 158 scripts for scanning.
NSE: Script Pre-scanning.
Initiating NSE at 16:44
Completed NSE at 16:44, 0.00s elapsed
Initiating NSE at 16:44
Completed NSE at 16:44, 0.00s elapsed
Initiating NSE at 16:44
Completed NSE at 16:44, 0.00s elapsed
Initiating Parallel DNS resolution of 2 hosts. at 16:44
Completed Parallel DNS resolution of 2 hosts. at 16:44, 0.50s elapsed
Initiating System DNS resolution of 1 host. at 16:44
Completed System DNS resolution of 1 host. at 16:44, 2.72s elapsed
Failed to resolve "nmap".
Initiating Ping Scan at 16:44
Scanning testphp.vulnweb.com (44.228.249.3) [4 ports]
Completed Ping Scan at 16:44, 0.02s elapsed (1 total hosts)
Initiating Parallel DNS resolution of 1 host. at 16:44
Completed Parallel DNS resolution of 1 host. at 16:45, 0.41s elapsed
Initiating SYN Stealth Scan at 16:45
Scanning testphp.vulnweb.com (44.228.249.3) [1000 ports]
Completed SYN Stealth Scan at 16:45, 4.39s elapsed (1000 total ports)
Initiating Service scan at 16:45
Initiating OS detection (try #1) against testphp.vulnweb.com (44.228.249.3)
Retrying OS detection (try #2) against testphp.vulnweb.com (44.228.249.3)
Initiating Traceroute at 16:45
Completed Traceroute at 16:45, 0.05s elapsed
Initiating Parallel DNS resolution of 2 hosts. at 16:45
Completed Parallel DNS resolution of 2 hosts. at 16:45, 0.51s elapsed
NSE: Script scanning 44.228.249.3.
Initiating NSE at 16:45
Completed NSE at 16:45, 5.02s elapsed
Initiating NSE at 16:45
Completed NSE at 16:45, 0.00s elapsed
Initiating NSE at 16:45
Completed NSE at 16:45, 0.00s elapsed
Nmap scan report for testphp.vulnweb.com (44.228.249.3)
Host is up (0.036s latency).
rDNS record for 44.228.249.3: ec2-44-228-249-3.us-west-2.compute.amazonaws.com
All 1000 scanned ports on testphp.vulnweb.com (44.228.249.3) are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: power-device|firewall|WAP|router|print server|general purpose
Running (JUST GUESSING): APC embedded (96%), Cisco ASA 9.X (96%), Cisco embedded (96%), Synology embedded (96%), HP embedded (93%), D-Link embedded (89%), Microsoft Windows 2000|2003 (87%)
OS CPE: cpe:/o:cisco:asa:9.2 cpe:/h:synology:rt1900ac cpe:/h:hp:2101nw cpe:/h:dlink:di-524 cpe:/o:microsoft:windows_2000::sp4 cpe:/o:microsoft:windows_server_2003::sp2
Aggressive OS guesses: APC Network Management Card 3 (96%), Cisco Adaptive Security Appliance (ASA 9.2) (96%), Cisco Aironet 3800-series WAP (96%), Synology RT1900ac router (96%), HP 2101nw wireless print server (93%), D-Link DI-524 wireless broadband router (89%), Microsoft Windows 2000 SP4 (87%), Microsoft Windows Server 2003 SP2 (87%)
No exact OS matches for host (test conditions non-ideal).
Network Distance: 3 hops

TRACEROUTE (using port 80/tcp)
HOP RTT      ADDRESS
1   6.00 ms  192.168.0.1
2   49.00 ms 172.16.103.254
3   50.00 ms ec2-44-228-249-3.us-west-2.compute.amazonaws.com (44.228.249.3)

NSE: Script Post-scanning.
Initiating NSE at 16:45
Completed NSE at 16:45, 0.00s elapsed
Initiating NSE at 16:45
Completed NSE at 16:45, 0.00s elapsed
Initiating NSE at 16:45
Completed NSE at 16:45, 0.00s elapsed
Read data files from: C:\Program Files (x86)\Nmap
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 17.94 seconds
           Raw packets sent: 2062 (95.092KB) | Rcvd: 13 (552B)
results: the scan found no open TCP ports. All 1000 scanned ports were filtered, indicating firewall or network filtering controls.


OWASP ZAP passive scan
purpose: identify security configuration u=issues without attacking the website.
Evidence: [ OWSAP ZAP] (evidence/ zap-request-responce & zap_alert-details)
results: the passive scan identified missing HTTP security hearders, including content security policy (CSP) and strict-transport-security (HSTS) along with other low-risk configuration issues.
