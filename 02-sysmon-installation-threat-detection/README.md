# 🛡️ Lab 2 – Sysmon Installation & Threat Detection

## Objective

Install and configure Microsoft Sysmon to improve endpoint visibility and investigate process creation, network activity, and file creation events commonly used during SOC investigations.

## Environment

- Windows 11
- Microsoft Sysmon
- SwiftOnSecurity Sysmon Configuration
- Event Viewer

## Tasks Completed

- Installed Sysmon using an official Microsoft Sysinternals release
- Applied the SwiftOnSecurity configuration
- Verified successful installation
- Reviewed the Sysmon Operational log
- Generated process creation events
- Generated network connection events
- Created files to trigger file creation events
- Investigated PowerShell activity

## Event IDs Investigated

| Event ID | Description |
|----------|-------------|
|1|Process Creation|
|3|Network Connection|
|11|File Created|

## Investigation Scenario

Simulated a suspicious PowerShell execution by reviewing process creation details, parent-child process relationships, command-line arguments, associated user context, and related network activity.

## Skills Demonstrated

- Sysmon Deployment
- Endpoint Telemetry Analysis
- Process Investigation
- Parent-Child Process Analysis
- Network Connection Investigation
- Threat Detection
- Security Monitoring

## Key Takeaway

Sysmon significantly enhances Windows logging by recording detailed endpoint telemetry such as process creation, command-line arguments, parent-child relationships, and network connections. This information is essential for modern SOC investigations and threat hunting.

## Screenshots

- Sysmon Installation
- Sysmon Operational Log
- Event ID 1
- Event ID 3
- Event ID 11
- PowerShell Investigation
