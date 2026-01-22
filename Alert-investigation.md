High-Severity Process Alert Investigation – True Positive



1. Alert Overview

Field: Details
Alert Type: Suspicious Parent-Child Relationship
Severity: High
Data Source :Sysmon
Event Code: 1 (Process Create)
Hostname: win-3450
Date/Time: 01/22/2026
Status: Under Investigation



2. Process Details

Entity: Value
Parent Process: powershell.exe
Child Process: nslookup.exe
Process Path: C:\Windows\System32\nslookup.exe
Working Directory: C:\Windows\System32
Event Action: Process Create
Detection Rule: ProcessCreate



3. Activity Description

The system detected "powershell.exe" spawning "nslookup.exe", indicating potential use of a network discovery utility through a scripting engine. This behavior is commonly associated with reconnaissance and post-exploitation activity.


4. Classification Decision

Final Classification: True Positive – Suspicious Reconnaissance Activity



5. Reason for True Positive Classification

- High-Risk Parent Process
PowerShell is frequently abused by threat actors for stealthy execution and remote command delivery.

- Reconnaissance Tool Execution
nslookup.exe is commonly used to enumerate DNS and test external or internal network connectivity.

- Behavioral Pattern Match
The execution chain aligns with MITRE ATT&CK Discovery techniques.

- Severity Justification
This activity may indicate post-compromise behavior or attacker presence in the environment.



6. Risk Assessment

Potential risks include:

- Internal network mapping
- Command-and-control testing
- Preparation for lateral movement



7. Recommended Actions

Immediate

- Identify and isolate the affected host if additional malicious indicators are found
- Identify the user account that launched PowerShell

Investigation

- Review PowerShell command-line arguments
- Check DNS query logs
- Search for similar activity across the environment

Preventative

- Enable PowerShell script block logging
- Restrict PowerShell usage via Group Policy
- Deploy EDR behavioral rules for reconnaissance tools



8. Indicators of Activity

Type: Value
Parent Process: powershell.exe
Child Process:nslookup.exe
Host :win-3450
Path: C:\Windows\System32\nslookup.exe
Data Source: Sysmon



Analyst Conclusion
This alert represents suspicious discovery activity consistent with reconnaissance behavior. While the tools involved are legitimate Windows utilities, their execution chain warrants escalation and further investigation.

Status: Escalated to Tier 2
Confidence Level: Medium–High
