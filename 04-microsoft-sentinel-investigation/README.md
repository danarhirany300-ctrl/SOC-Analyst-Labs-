# 🛡️ Lab 4 – Microsoft Sentinel Incident Investigation

## Objective

Investigate a security incident using Microsoft Sentinel by analyzing incidents, reviewing entities, executing KQL queries, and documenting investigation findings.

## Environment

- Microsoft Sentinel
- Azure Portal
- Log Analytics Workspace

## Tasks Completed

- Opened and reviewed a Sentinel incident
- Examined incident severity and related alerts
- Investigated associated entities
- Executed KQL queries to analyze security events
- Reviewed successful and failed authentication events
- Investigated PowerShell activity
- Reviewed external network connections
- Documented findings and closed the incident

## Sample KQL Queries

### Successful Logons

```kusto
SecurityEvent
| where EventID == 4624
| project TimeGenerated, Computer, Account, LogonType
```

### Failed Logons

```kusto
SecurityEvent
| where EventID == 4625
| summarize FailedAttempts=count() by Account
```

### PowerShell Activity

```kusto
DeviceProcessEvents
| where FileName == "powershell.exe"
```

## Investigation Scenario

Investigated a Sentinel alert involving suspicious PowerShell execution by identifying the affected user, reviewing authentication activity, examining network connections, and determining appropriate incident classification.

## Skills Demonstrated

- Microsoft Sentinel
- SIEM Investigation
- KQL
- Entity Analysis
- Threat Hunting
- Incident Triage
- Incident Documentation

## Key Takeaway

Microsoft Sentinel enables centralized investigation of security events from multiple data sources. Combining KQL with incident and entity analysis allows analysts to efficiently detect, investigate, and respond to security threats.

## ## Screenshots

### Sentinel Dashboard
![Sentinel Dashboard](sentinel-dashboard.png)

### Incident Overview
![Incident Overview](./incident-overview.png)

### Entities
![Entities](./entities.png)

### KQL Query Results
![KQL Query Results](./kql-query-results.png)

### Incident Closure
![Incident Closure](./incident-closure.png)
