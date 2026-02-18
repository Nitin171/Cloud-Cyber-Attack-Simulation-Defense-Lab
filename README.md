# Cloud Cyber Attack Simulation & Defense Lab (Azure & Microsoft Sentinel)

## Project Overview
This project demonstrates an end-to-end cloud security workflow where cyber attacks are simulated, detected, investigated, and automatically mitigated using Microsoft Azure and Microsoft Sentinel.

A controlled attack environment was built to simulate SSH brute-force attacks on Azure virtual machines, followed by automated detection and response actions that dynamically block attacker access in real time.

The lab replicates real-world SOC (Security Operations Center) workflows including threat detection, incident generation, investigation, and automated response.

---

## Objectives
- Simulate real-world attacker behavior in a cloud environment.
- Detect unauthorized login attempts using SIEM analytics.
- Generate security incidents automatically.
- Automate response actions to prevent further compromise.
- Demonstrate end-to-end SOC incident handling workflow.

---

## Environment Architecture
The lab environment consists of:

- Azure Virtual Network with public and private subnets.
- Public VM acting as attacker machine.
- Private VM acting as internal target server.
- Log Analytics Workspace for log collection.
- Microsoft Sentinel for SIEM detection.
- Azure Logic Apps for automated response.
- Network Security Groups for access control.

Workflow:

Attacker VM  
→ SSH Brute Force Attack  
→ Logs Generated  
→ Sentinel Detection  
→ Incident Creation  
→ Automation Playbook Triggered  
→ NSG Rule Updated  
→ Attacker IP Blocked  

---

## Attack Simulation
SSH brute-force attacks were simulated using the Hydra tool from an attacker VM targeting an internal VM.

Multiple failed login attempts generated authentication logs, which were collected and analyzed by Sentinel to detect suspicious behavior.

---

## Detection & Incident Creation
Microsoft Sentinel analytics rules were configured to:

- Detect repeated failed login attempts.
- Identify brute-force attack patterns.
- Automatically generate security incidents.
- Enable monitoring and investigation workflows.

---

## Automated Incident Response
An Azure Logic App playbook was implemented to:

- Extract attacker IP from incident data.
- Automatically create NSG deny rules.
- Block attacker access in real time.
- Prevent further unauthorized login attempts.

This removes the need for manual intervention and reduces response time.

---

## Key Security Capabilities Demonstrated
✔ Attack simulation  
✔ Log collection & monitoring  
✔ SIEM-based threat detection  
✔ Incident generation  
✔ Automated response  
✔ Dynamic network defense  
✔ Cloud SOC workflow implementation  

---

## Technologies Used
- Microsoft Azure
- Microsoft Sentinel (SIEM)
- Azure Logic Apps
- Log Analytics Workspace
- Azure Virtual Machines
- Network Security Groups
- Linux Syslog
- Hydra brute-force tool
- KQL (Kusto Query Language)

---

## Project Outcome
The lab successfully demonstrated real-time detection and automated defense against SSH brute-force attacks in a cloud environment, simulating real SOC incident response operations.

Attack attempts were automatically detected, incidents generated, and attacker IPs blocked without manual action.

---

## Skills Demonstrated
- SOC Operations
- Incident Detection & Response
- Threat Monitoring
- Cloud Security Implementation
- SIEM Analytics
- Security Automation
- Log Analysis
- Attack Simulation
- Network Security Enforcement

---

## Screenshots
Screenshots of incidents, detections, and automated blocking can be found in the `/screenshots` directory.

---

## Author
Cybersecurity Student & SOC Analyst Aspirant  
Hands-on practitioner in cloud security and incident response.
