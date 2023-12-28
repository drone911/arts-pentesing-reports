# Pentesting Reports For Arts Tailor Shop (using [Latex](https://www.latex-project.org/))

The agreement template signed by Art's Tailor Shop for the penetration test can be found [here](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex00-PenetrationTestAgreement.pdf).

| Report Link | Summary | Findings | CVSS Base Ratings |
| --- | ----------- | ------- |  -------- |
| [Ex10_Responder.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex10_Responder.pdf) | Perform a man-in-the-middle attack using fake responses from [Responder](https://github.com/SpiderLabs/Responder) for Web Proxy Auto-Discover Protocol (WPAD) queries. | WPAD discovery does not authenticate Server | ``4.9`` _AV:A AC:L PR:L UI:R S:U C:L I:L A:L_ |  
| [Ex0f_LinuxIsBroken.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex0f_LinuxIsBroken.pdf) | Exploit vulnerable configurations compounded with a sudo vulnerability ([CVE-2019-14287](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2019-14287)) to escalate privilege to a root user  | Exploitable sudo version (≤1.28) to gain elevated privileges | ``7.8`` _AV:L AC:L PR:L UI:N S:U C:H I:H A:H_ |  
| [Ex0e_SSLStrip.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex0d_SSLStrip.pdf) | Conduct a Man-in-the-Midde attack using [dssniff's](https://www.kali.org/tools/dsniff/) ``arpspoof`` and [sslstrip](https://github.com/moxie0/sslstrip) to get Basic Auth credentials. | 1. Web Server serving same pages over both HTTP and HTTPS.<br><br>2. No mitigation for spoofed ARP packets.  | a. ``6.1`` _AV:L AC:L PR:L UI:R S:U C:L I:L A:H_ <br><br>b. ``5.3`` _AV:L AC:L PR:L UI:N S:U C:L I:L A:L_ | 
| [Ex0d_BookIsBreached.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex0d_BookIsBreached.pdf) | Use exposed ``utilman.exe`` configuration to create a local system administrative user. | SYSTEM Privilege RCE due to a modified accessibility registry. | ``9.8`` _V:N AC:L PR:N UI:N S:U C:H I:H A:H_ | 
| [Ex0c_SliverOfHope.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex0c_SliverOfHope.pdf) | Generate a [Sliver](https://github.com/BishopFox/sliver) payload/beacon and schedule to run on a victim machine using Windows ``schtask``  | None | None | 
| [Ex0b_Pivot.pdt](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex0b_Pivot.pdf) | Use [Chisel](https://github.com/jpillora/chisel) and ``Proxychains`` to scan the internal network through a compromised machine while bypassing a firewall. | None | None |
| [Ex0a_Hashtag.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex0a_Hashtag.pdf) | Use John-the-Ripper to crack LM and NTLMv1 hashes exfiltrated in previous exercise. | 1. Weak LM and NTLMv1 Authentication Enabled.<br><br>2. Weak Encryption standard allowed for Kerberos. | a. ``8.1`` _AV:N AC:H PR:N UI:N S:U C:H I:H A:H_ <br><br>b. ``8.1`` _AV:N AC:H PR:N UI:N S:U C:H I:H A:H_ | 
| [Ex09_PowerUp.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex09_PowerUp.pdf) | Use Powersploit to exploit a priviledge escalation vulnerability in Windows Volume Shadow Service. Use the elevated privileges to run Mimikatz and dump LSA secrets and SAM database. | Privilege escalation vulnerability with Volume Shadow Service | ``8.4`` _AV:L AC:L PR:N UI:N S:U C:H I:H A:H_) |
| [Ex08_ThroughTheGate.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex08_ThroughTheGate.pdf) | Perform password spraying on Microsoft Outlook to get domain credentials. Use compromised network firewall to expose an internal RDP service using port forwarding. | 1. No rate limit on login attempts in Outlook. <br><br> 2. Default credentials in web facing firewall configurator. | a. ``7.3`` _AV:N AC:L PR:N UI:N S:U C:L I:L A:L_ <br><br>b. ``9.8`` _AV:A AC:L PR:N UI:N S:U C:H I:H A:H_ |
| [Ex07_BriansService.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex07_BriansService.pdf) | Exploit a buffer overflow to inject commands in a developer utility service and gain a reverse shell. | Arbitrary Code Execution in Brian’s Service | ``7.3`` _AV:N AC:L PR:N UI:N S:U C:L I:L A:L_ |
| [Ex06_VulnScan.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex06_VulnScan.pdf) | Use Nessus's advanced scan with custom options to uncover vulnerabilities hidden from a basic scan. Use Metasploit to exploit the compiled backdoor. | Remote Code Execution Vulneriblity in vsFTPD | ``7.3`` _AV:N AC:L PR:N UI:N S:U C:L I:L A:L_ |
| [Ex05_Nmap_SearchSploit.pdf](https://github.com/drone911/arts-pentesing-reports/blob/main/Ex05_Nmap_SearchSploit.pdf) | Use Nmap to gather TCP and UDP service names & versions running on businesses public web server. Use the data gathered to run queries in Searchsploit. | None | None |
