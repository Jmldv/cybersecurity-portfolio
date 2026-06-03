# FortiGate to CrowdStrike Falcon SIEM Integration Research

## Overview
This research project documents how FortiGate firewall logs can be forwarded into CrowdStrike Falcon Next-Gen SIEM.

The goal was to understand the required architecture, log forwarding method, connector usage, and validation steps needed to make FortiGate firewall events visible and searchable inside CrowdStrike Falcon.

## Research Scope
This is a research and integration design project, not a fully deployed hands-on lab. It focuses on the planned workflow, required components, and expected validation steps for forwarding FortiGate logs into CrowdStrike Falcon Next-Gen SIEM.

## Architecture
- FortiGate Firewall generates security logs
- FortiGate exports logs using remote syslog
- CEF format is used for structured log forwarding
- Falcon Log Collector receives the syslog events
- Falcon Log Collector forwards logs into CrowdStrike Falcon using the correct ingest configuration
- Fortinet FortiGate Data Connector helps normalize and parse the logs inside Falcon

## Tools and Technologies
- FortiGate Firewall
- CrowdStrike Falcon Next-Gen SIEM
- Falcon Log Collector
- Fortinet FortiGate Data Connector
- Remote syslog
- CEF log format
- TCP/UDP log forwarding

## Integration Flow
1. Configure FortiGate to export logs using remote syslog.
2. Select CEF format to improve log structure and normalization.
3. Use Falcon Log Collector as the syslog receiver.
4. Configure FortiGate to send logs to the Falcon Log Collector IP address and port.
5. Ensure the protocol and port match between FortiGate and the receiver.
6. Configure Falcon Log Collector with the correct CrowdStrike ingest token and ingest URL.
7. Enable or configure the Fortinet FortiGate Data Connector in CrowdStrike.
8. Validate log visibility inside Falcon Next-Gen SIEM.

## Why CEF Format
CEF provides a more structured log format, which helps CrowdStrike normalize firewall events and make key fields easier to search and use in detections.

Examples of useful parsed fields:
- Source IP
- Destination IP
- Action
- Severity
- Event type
- Device vendor
- Device product

## Validation Steps
Inside CrowdStrike Falcon Next-Gen SIEM, validation should include:
- Confirming source activity
- Checking ingestion health
- Reviewing data volume
- Searching for FortiGate-related events
- Confirming the Fortinet FortiGate source or connector is visible
- Verifying parsed fields such as source IP, destination IP, action, severity, and event type

## Skills Demonstrated
- SIEM log onboarding research
- Firewall log forwarding design
- Syslog and CEF understanding
- CrowdStrike Falcon SIEM architecture
- Data connector planning
- Log normalization concepts
- SOC data ingestion workflow
- Security monitoring architecture documentation

## Report
The full research report is included in this folder.
