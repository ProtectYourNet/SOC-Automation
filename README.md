## SOC Automation

## Objective
This project is a SOC automation lab designed to integrate Wazuh (SIEM/XDR), Shuffle (SOAR), Sysmon, and The Hive (Case Management) into a fully functional security operations workflow through cloud imstance and local/cloud vr machines. The goal is to automate threat detection, incident response, and case management while providing hands-on experience in security operations.

### Skills Learned
✅ SIEM & Log Analysis – Configuring Wazuh to ingest logs, analyze security events, and create custom detection rules.
✅ SOAR Automation – Implementing Shuffle workflows to automate security alerting and incident response.
✅ Case Management – Using The Hive for alert triage, case tracking, and incident documentation.
✅ Threat Detection – Creating custom rules to detect attacks like Mimikatz execution and malicious process activity.
✅ Security Telemetry Collection – Configuring Sysmon to generate logs and monitor Windows security events.
✅ Incident Response – Automating responses such as blocking IPs, alerting analysts, and enriching threat data.
✅ Threat Intelligence Integration – Using VirusTotal API for hash reputation lookups.
✅ Firewall & Access Control – Configuring cloud-based firewalls and securing virtual machines.
✅ Data Flow & Network Security – Mapping security event flows using draw.io diagrams.
✅ Cloud Infrastructure – Deploying Ubuntu VMs on DigitalOcean for Wazuh and The Hive.

### Tools Used
Security Information & Event Management (SIEM)
* Wazuh – Open-source SIEM and XDR platform for log analysis, intrusion detection, and incident response.

## Security Orchestration, Automation, and Response (SOAR)
* Shuffle – Open-source SOAR platform used to automate security workflows and integrate with security tools.

## Case Management & Threat Intelligence
* The Hive – Incident response and case management platform for handling security alerts.
* VirusTotal API – Threat intelligence service used to check file hashes against a database of known malware.

## Endpoint Detection & Telemetry Collection
* Sysmon (System Monitor) – Windows logging tool for capturing detailed telemetry, such as process execution and network connections.
* Windows Event Viewer – Native Windows tool for analyzing system and security logs.

## Attack Simulation & Threat Emulation
* Mimikatz – Penetration testing tool used to simulate credential theft attacks and test detection capabilities.

## Infrastructure & Virtualization
* VirtualBox – Virtualization platform used to create Windows 10 and other virtual machines.
* DigitalOcean – Cloud service provider used to host Wazuh and The Hive servers.

## Networking & Security
* Firewalls (DigitalOcean & Local) – Used to restrict access and secure cloud-based virtual machines.
* SSH (Secure Shell) – Remote access protocol used to manage cloud-based Linux servers.

## Log Parsing & Configuration
* PowerShell – Scripting language used to install and configure security tools on Windows.
* Nano & Vim – Command-line text editors used to modify configuration files in Linux.

## Automation & Workflow Tools
* Webhook (Shuffle) – Used to receive and process alerts from Wazuh into SOAR workflows.
* Regex (Regular Expressions) – Used for parsing security event data, such as extracting SHA-256 hashes.

## Diagramming & Documentation
* draw.io (diagrams.net) – Tool used to create network and data flow diagrams for lab architecture.

## Steps

## Phase 1: Planning & Architecture

1. Define Objectives – Establish goals for SIEM, SOAR, and case management integration.

2. Create a Network Diagram – Design system architecture with data flow visualization.

## Phase 2: Setting Up Infrastructure

Deploy Virtual Machines

Install VirtualBox (or use DigitalOcean for cloud servers).

Create a Windows 10 VM for telemetry collection.

Deploy Wazuh Manager, The Hive, and Shuffle servers on DigitalOcean.

Configure Firewalls & Secure Access

Restrict VM access using DigitalOcean Firewalls.

Allow only trusted IPs for SSH and web dashboards.

## Phase 3: Installing & Configuring Security Tools

Set Up Wazuh SIEM

Install Wazuh Manager on Ubuntu.

Configure firewall rules for agent communication.

Verify dashboard access.

Install & Configure The Hive

Install Cassandra, Elasticsearch, and The Hive.

Configure settings for web accessibility.

Install & Configure Windows Telemetry

Install Sysmon for advanced event logging.

Configure Wazuh Agent for log forwarding.

## Phase 4: Generating & Detecting Security Events

Simulate Attacks for Detection

Run Mimikatz to generate credential theft logs.

Verify Sysmon logs in Windows Event Viewer.

Ingest & Analyze Logs in Wazuh

Modify osc.conf file to enable telemetry collection.

Create custom Wazuh rules for threat detection.

## Phase 5: Automating Incident Response

Integrate Shuffle SOAR

Configure Wazuh to send alerts to Shuffle via webhooks.

Debug connectivity issues.

Create an Automation Workflow

Extract SHA-256 hashes from alerts.

Query VirusTotal API for reputation analysis.

Create incidents in The Hive.

Send email notifications to SOC analysts.

Implement Active Response Actions

Automate blocking of suspicious IPs based on alerts.

Final Steps: Testing & Optimization

Test End-to-End Workflow

Validate event ingestion, alerting, and case creation.

Ensure automation workflows execute correctly.

Optimize & Document

Fine-tune detection rules and responses.

Document configurations and troubleshooting steps.

Share project details on GitHub.
