---
layout: default
---

-Audit users and groups in active directory. Important groups are domain admins or any admin group. You can check the membership of an individual user by checking memberof tab.

-Change all admin passwords

-download sysinternals suite

-apply patches (if updates are to much download the specific service pack needed. Doing this will avoid downloading useless service packs)

-check server manager roles

-open DNS and DHCP and configure as needed

-apply group policy ( golden security templates can be downloaded from online ) use a verified source such as Microsoft technet or hey scripting guy

-set execution policy in powershell remote signed. Be weary of setting anything else otherwise unsined scripts can run on your system.

-Audit DNS records

-Audit DHCP scope

-check if datadepulication is on ( data will be replicated to any DC's) this can be good or bad. Good because it saves time bad because if one DC is corrupted the other one will be to

-change file explorer view to view hidden files as well as show extensions

-additonal views in file explorer can be shown to customize view

-update group policy for folder auditing

-study event viewer codes to quickly search logs

-Hey, Scripting Guy! Blog – Learn about Windows PowerShell

   [blogs.technet.microsoft.com](https://blogs.technet.microsoft.com/heyscriptingguy/)

   Learn about Windows PowerShell

   Excellent blog for powershell Everything

-Microsoft Virtual Academy

   [Windows Security & Forensics](https://mva.microsoft.com/en-us/training-courses/windows-security-forensics-14383?l=YCKufUQsB_5105244527)

   Virtual Academy

   Learn from an expert team about what it takes to become a digital forensics professional, how to prevent cybercrime, and how to respond if it occurs.

-Channel 9

   [Channel 9](https://channel9.msdn.com/)

   Channel 9 provides videos for developers, delivered by the people who work behind the scenes at Microsoft.

   Channel 9 is a community. We bring forward the people behind our products and connect them with those who use them. We think there is a great future in software and we're excited about it. We want the community to participate in the ongoing conversation. This is the heart of Channel 9. We talk about our work but listen to the customer.

-Windows Security Baselines

   [docs.microsoft.comdocs.microsoft.com](https://docs.microsoft.com/en-us/windows/security/threat-protection/windows-security-baselines)

   This article, and the articles it links to, describe how to use Windows Security Baselines in your organization

-check for scheduled tasks

-audit choco if installed

-check start up tasks

-audit system32

-check .ps1s on the desktop

-nsacyber/Windows-Secure-Host-Baseline

   [nsacyber/Windows-Secure-Host-Baseline](https://github.com/nsacyber/Windows-Secure-Host-Baseline)

   Configuration guidance for implementing the Windows 10 and Windows Server 2016 DoD Secure Host Baseline settings. #nsacyber - nsacyber/Windows-Secure-Host-Baseline

-nsacyber/Windows-Event-Log-Messages

   [nsacyber/Windows-Event-Log-Messages](https://github.com/nsacyber/Windows-Event-Log-Messages)

   Retrieves the definitions of Windows Event Log messages embedded in Windows binaries and provides them in discoverable formats. #nsacyber - nsacyber/Windows-Event-Log-Messages


-change krbrgt password to mitigate golden tickets

-create two accounts for domain for each windows admin and use non admin account for logging into servers. Avoid using domain admin accounts for logins and instead use admin escalation with those accounts when logged into non admin accounts

-powershell constrained language (edited)

-check smb versions

-check smb share permissions

-GPP passwords in SYSVOL

-lockdown SYSVOL

-Utilman

-rundll32.exe is malicious most likely

-LAPS

-create individual accounts for everyone

-search for senitive data in files and shares

-Encrypt sensitive data and remove from database if not needed.
