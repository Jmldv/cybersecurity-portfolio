# OpenCTI Threat Intelligence Integration Lab

## Overview
This project demonstrates the deployment of OpenCTI and its integration with multiple threat intelligence sources, including AlienVault OTX, MalwareBazaar, and AbuseIPDB.

The goal was to collect, transform, and import threat intelligence data into OpenCTI using API-based integrations and Python scripts.

## Tools Used
- OpenCTI
- Docker Desktop
- Git
- Python
- AlienVault OTX API
- MalwareBazaar API
- AbuseIPDB API
- STIX indicators

## What I Implemented
- Deployed OpenCTI locally using Docker
- Configured OpenCTI environment variables and API tokens
- Created test indicators for IP addresses, domains, and URLs
- Exported indicators from OpenCTI to AlienVault OTX
- Imported malware data from MalwareBazaar into OpenCTI
- Imported AbuseIPDB blacklist data into OpenCTI
- Created and linked 500 IP indicators to an OpenCTI report

## Problems Solved
- Fixed Docker virtualization and WSL2 issues
- Resolved invalid UUID token errors in OpenCTI
- Troubleshot OpenCTI login and visibility issues
- Fixed OpenCTI indicator creation errors
- Linked AbuseIPDB indicators to OpenCTI reports for visibility

## Skills Demonstrated
- Threat intelligence platform deployment
- API integration
- Python scripting
- Docker troubleshooting
- IOC management
- STIX indicator creation
- SOC-style documentation
- Threat intelligence workflow automation

[View Full PDF Report](./OpenCTI-Threat-Intelligence-Integration-Report.pdf)
