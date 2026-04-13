\# LOLBIN Detection — rundll32.exe Proxy Execution

\*\*Platform:\*\* Windows 11 | \*\*Tool:\*\* Sysmon v15.15 | \*\*Date:\*\* April 2026



\## Overview

Simulated and detected a Living Off The Land Binary (LOLBIN) attack using 

rundll32.exe on a Windows 11 endpoint. Full detection achieved using Sysmon 

Event ID 1 with parent-child process chain analysis.



\## Attack Chain

powershell.exe → rundll32.exe → payload



\## MITRE ATT\&CK

\- T1218.011 — Signed Binary Proxy Execution: Rundll32

\- T1059.001 — PowerShell



\## Tools Used

\- Sysmon v15.15 (SwiftOnSecurity config)

\- Windows Event Viewer

\- PowerShell



\## Files

| File | Description |

|------|-------------|

| `LOLBIN\_Detection\_Lab\_Report\_Imaad.docx` | Full lab report with SOC alert, IOCs, and MITRE mapping |

| `sysmonconfig.xml` | SwiftOnSecurity Sysmon config used for detection |



\## Key Findings

\- Sysmon Event ID 1 captured the full suspicious process chain

\- PowerShell spawning rundll32.exe = confirmed red flag

\- High integrity level execution detected

\- Traditional antivirus would NOT detect this attack



\---

\*\*Author:\*\* Muhammad Imaad Ul Haq  

\*\*LinkedIn:\*\* linkedin.com/in/imaad-ul-haq  

\*\*GitHub:\*\* github.com/imaadsoc24

