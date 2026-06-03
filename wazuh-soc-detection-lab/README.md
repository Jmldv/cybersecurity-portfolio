# Wazuh SOC Detection Lab

## Overview
This project demonstrates the deployment of a small SOC-style monitoring lab using Wazuh, Ubuntu, DVWA, auditd, Telegram alerts, and Suricata IDS.

The goal was to collect logs from a vulnerable web application, detect simulated web attacks, monitor a honeytoken file, and generate real-time notifications through Telegram.

## Lab Architecture
- VM 1: Wazuh SIEM Server
- VM 2: DVWA Target System with Wazuh Agent
- VM 3: Suricata IDS with Wazuh Agent

## Tools Used
- Wazuh
- Ubuntu
- DVWA
- Apache
- MariaDB
- auditd
- Suricata IDS
- Telegram Bot API
- Nmap
- Linux command line

## What I Implemented
- Deployed Wazuh SIEM server on an Ubuntu virtual machine
- Deployed DVWA vulnerable web application on a second Ubuntu machine
- Installed and configured Wazuh Agent on the DVWA machine
- Forwarded Apache access logs, Apache error logs, and audit logs to Wazuh
- Simulated SQL injection and XSS attacks against DVWA
- Created custom Wazuh detection rules for SQL injection and XSS activity
- Created a honeytoken file and monitored access using auditd
- Configured Telegram bot notifications for Wazuh alerts
- Added a third Ubuntu VM running Suricata IDS
- Generated Nmap traffic and confirmed Suricata alerts were visible in Wazuh

## Attack Scenarios Tested
- SQL Injection
- Reflected Cross-Site Scripting
- Honeytoken file access
- Nmap scanning activity

## Problems Solved
- Increased VM disk space to complete Wazuh installation
- Configured Wazuh agent connectivity between DVWA and Wazuh server
- Forwarded Apache and audit logs to Wazuh
- Created and tested custom Wazuh rules
- Integrated Telegram alert notifications
- Connected Suricata IDS logs to Wazuh

## Skills Demonstrated
- SIEM deployment and configuration
- SOC-style alert monitoring
- Linux system administration
- Endpoint log forwarding
- Web attack detection
- Custom detection engineering
- Honeytoken monitoring
- IDS integration
- Telegram alert automation
- Incident investigation documentation

## Report
The full PDF report with screenshots is included in this folder.
