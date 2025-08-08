# Findings Report – Splunk Log Sources Investigation

## Date Started
_August 2025_

## Investigation Objective
Investigate suspicious behavior in log data using Splunk:
- Failed logins
- Suspicious IP addresses
- Privilege escalation
- Correlation across multiple sources

## Queries Used
_(Add SPL queries here as you use them)_

Example:
```spl
index=windows sourcetype="WinEventLog:Security" EventCode=4625
| stats count by src_ip, user
