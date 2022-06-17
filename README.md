# Zena - Stored XSS to RCE Exploit POC

**Exploit POC for Rocket Software's Zena application 4.2.1 - Stored XSS to RCE**

[CVE-2021-45025](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-45025)

[CVE-2021-45026](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-45026)

POC Process:
- Logs into Zena's webconfig page using default credentials
- Drops Stored XSS payload
- Payload needs to be triggered by someone navigating to the webconfig page
- Triggered payload uses REST API backend of Zena to find an agent and build a Task for that agent
- Task is then triggered for agent thus executing the specified command

**To Run:**
- python CookieMonster.py <hostname/ip> <TLS/SSL - True or False> <cmd.exe command>
  - **Example: python3 CookieMonster.py 127.0.0.1 False "/c whoami > c:/out.txt"**


**Credits:** James Barnett and Jeff Green
