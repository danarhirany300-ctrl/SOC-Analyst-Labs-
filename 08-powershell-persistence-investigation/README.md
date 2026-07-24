# 🛡️ Lab 8 – PowerShell & Persistence Investigation

## Objective

Investigate PowerShell execution and identify common Windows persistence mechanisms using Event Viewer, Sysmon, and Microsoft Defender XDR.

## Environment

- Windows 11
- Sysmon
- Microsoft Defender XDR
- Event Viewer

## Tasks Completed

- Generated PowerShell activity
- Investigated PowerShell process execution
- Reviewed parent-child process relationships
- Examined Scheduled Tasks
- Inspected Registry Run Keys
- Reviewed Startup folders
- Analyzed Windows Services
- Completed a persistence investigation scenario

## Persistence Techniques Reviewed

| Technique | Description |
|-----------|-------------|
|Scheduled Tasks|Automatic execution of programs|
|Registry Run Keys|Programs launched at user logon|
|Startup Folder|Applications started automatically|
|Windows Services|Background services that can persist across reboots|

## Investigation Scenario

Investigated suspicious PowerShell activity by reviewing process execution details, command-line arguments, parent processes, and common Windows persistence mechanisms to determine whether unauthorized persistence was established.

## Skills Demonstrated

- PowerShell Investigation
- Sysmon Analysis
- Persistence Detection
- Windows Registry Analysis
- Scheduled Task Investigation
- Windows Service Investigation
- Incident Documentation

## Key Takeaway

PowerShell and persistence mechanisms are frequently abused by attackers. Understanding how to investigate these techniques is essential for identifying compromised systems and supporting incident response.

## Screenshots

- PowerShell Event
- Sysmon Process Details
- Task Scheduler
- Registry Run Keys
- Startup Folder
- Windows Services
