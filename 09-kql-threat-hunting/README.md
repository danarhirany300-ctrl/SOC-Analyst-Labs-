# 🛡️ Lab 9 – KQL Threat Hunting

## Objective

Perform proactive threat hunting using Kusto Query Language (KQL) to identify suspicious endpoint activity, authentication anomalies, and potential attacker techniques.

## Environment

- Microsoft Sentinel
- Microsoft Defender XDR Advanced Hunting

## Tasks Completed

- Hunted for PowerShell execution
- Identified encoded PowerShell commands
- Reviewed Command Prompt activity
- Investigated privileged logons
- Analyzed failed authentication attempts
- Reviewed public network connections
- Searched for Living-Off-the-Land Binaries (LOLBins)
- Completed a simulated threat hunting exercise

## KQL Queries Used

### PowerShell Activity

```kusto
DeviceProcessEvents
| where FileName =~ "powershell.exe"
| project Timestamp, DeviceName, AccountName, ProcessCommandLine
```

### Encoded PowerShell

```kusto
DeviceProcessEvents
| where ProcessCommandLine has "-enc"
   or ProcessCommandLine has "-EncodedCommand"
```

### Failed Logons

```kusto
SecurityEvent
| where EventID == 4625
| summarize FailedAttempts=count() by Account
```

### Public Network Connections

```kusto
DeviceNetworkEvents
| where RemoteIPType == "Public"
```

### LOLBins

```kusto
DeviceProcessEvents
| where FileName in ("certutil.exe","bitsadmin.exe","mshta.exe","rundll32.exe","regsvr32.exe")
```

## Investigation Scenario

Conducted a proactive hunt for suspicious PowerShell activity across enterprise endpoints by reviewing process execution, encoded commands, parent-child process relationships, network activity, and authentication events.

## Skills Demonstrated

- Kusto Query Language (KQL)
- Threat Hunting
- Microsoft Defender XDR
- Microsoft Sentinel
- Process Investigation
- Authentication Analysis
- Network Investigation
- Detection Engineering

## Key Takeaway

Threat hunting allows SOC analysts to identify malicious behavior before it escalates into confirmed incidents. Combining KQL with endpoint and authentication telemetry improves detection capabilities and supports proactive defense.

## Screenshots

- PowerShell Hunt
- Encoded PowerShell Hunt
- Failed Logons
- Public Network Connections
- LOLBins Query
- Threat Hunting Summary
