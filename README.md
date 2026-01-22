# SOC Environment Implementation with Shuffle Automation

##  Project Summary
This project presents an **advanced Security Operations Center (SOC) implementation**
built using **open-source SIEM, SOAR, and Threat Intelligence tools**.  
The primary goal is to **automate alert ingestion, incident analysis, and response workflows**
to reduce analyst workload and improve security response efficiency.

---

## SOC Architecture Components
The SOC environment is composed of the following integrated tools:

- **Wazuh (SIEM)**  
  Collects logs, detects security events, and generates alerts.

- **Shuffle Automation (SOAR)**  
  Orchestrates automated workflows triggered by Wazuh alerts.

- **TheHive (Incident Response Platform)**  
  Manages security cases and incident lifecycle.

- **Cortex (Analysis Engine)**  
  Enriches observables and performs automated threat analysis.

- **MISP (Threat Intelligence Platform)**  
  Correlates Indicators of Compromise (IOCs) and threat data.

- **Discord (Alerting Channel)**  
  Provides real-time notifications to SOC analysts.

---

## Automated Incident Workflow
1. Security event detected by **Wazuh**
2. Alert forwarded to **Shuffle Automation** via webhook
3. Shuffle parses and classifies alert severity
4. **TheHive** automatically creates an incident case
5. **Cortex** analyzes observables (IP, hash, URL)
6. **MISP** enriches the incident with threat intelligence
7. **Discord** notification sent to SOC team

---

## Key Features
- End-to-end automated SOC workflow
- Reduced **MTTD (Mean Time to Detect)**
- Reduced **MTTR (Mean Time to Respond)**
- Automated case creation and enrichment
- Centralized incident visibility
- Real-time analyst notifications

---

##  Security Use Cases Implemented
- SSH brute-force attack detection
- Malware hash analysis
- Unauthorized access detection
- IOC correlation using threat intelligence
- Automated alert escalation

---

## Repository Structure
```text
SOC-Environment-Shuffle-Automation/
├── docs/                  # Technical documentation
├── diagrams/              # Architecture and workflow diagrams
├── configs/               # Sanitized configuration samples
├── shuffle-workflows/     # SOAR workflow exports
└── README.md              # Project overview

