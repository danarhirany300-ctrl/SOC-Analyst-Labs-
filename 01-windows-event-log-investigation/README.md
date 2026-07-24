# 🛡️ Lab 1 – Windows Event Log Investigation

## Objective

Investigate Windows Security Event Logs to understand how authentication, account activity, and process creation are recorded. Practice identifying common security events used in daily SOC operations.

## Environment

- Windows 11
- Event Viewer
- Windows Security Logs

## Tasks Completed

- Opened Event Viewer and navigated to the Security log
- Filtered events by Event ID
- Reviewed successful and failed logons
- Investigated account management events
- Reviewed process creation events
- Exported Security logs as `.evtx`
- Practiced a basic authentication investigation

## Event IDs Investigated

| Event ID | Description |
|----------|-------------|
|4624|Successful logon|
|4625|Failed logon|
|4634|Logoff|
|4672|Special privileges assigned|
|4688|Process created|
|4697|Service installed|
|4720|User account created|
|4723|Password change attempt|
|4726|User account deleted|
|4732|User added to privileged group|
|1102|Security log cleared|

## Investigation Scenario

Simulated an investigation into repeated failed login attempts by reviewing authentication events, identifying affected accounts, and checking for subsequent successful logons.

## Skills Demonstrated

- Windows Event Viewer
- Windows Security Log Analysis
- Authentication Investigation
- Event ID Analysis
- Incident Documentation
- Evidence Preservation

## Key Takeaway

Windows Security Event Logs provide essential visibility into authentication, account management, privilege changes, and process execution. Understanding common Event IDs is a fundamental skill for Security Operations Center (SOC) analysts.

## Screenshots

- Event Viewer Security Log
- Event ID 4624
- Event ID 4625
- Event ID 4688 (if available)
- Exported Security.evtx
