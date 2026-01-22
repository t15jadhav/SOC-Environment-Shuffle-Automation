# SOC Architecture

This document describes the architecture of the Security Operations Center (SOC)
implemented using open-source SIEM, SOAR, and Threat Intelligence platforms.
The architecture is designed to support automated detection, analysis, and response
to security incidents.

---

## Architecture Overview
The SOC architecture follows a **modular, scalable, and automation-driven design**.
Each component performs a specialized security function and communicates through
APIs and webhooks to enable real-time alert processing and response orchestration.

The design supports integration of additional tools and use cases without major
architectural changes, making it suitable for modern SOC environments.

---

## Core Components

### Wazuh (SIEM)
- Centralized log collection from monitored systems
- Real-time security event detection
- Alert generation based on predefined rules

### Shuffle Automation (SOAR)
- Orchestrates automated incident response workflows
- Receives alerts from Wazuh via webhooks
- Integrates with incident response and threat intelligence platforms

### TheHive (Incident Response Platform)
- Manages the full incident lifecycle
- Automatically creates cases based on alerts
- Provides structured incident tracking for SOC analysts

### Cortex (Analysis Engine)
- Performs automated analysis of observables
- Enriches alerts with contextual information
- Reduces manual investigation effort

### MISP (Threat Intelligence Platform)
- Correlates Indicators of Compromise (IOCs)
- Enriches incidents with external threat intelligence
- Improves detection accuracy and response decisions

### Discord (Notification Channel)
- Sends real-time alerts to SOC analysts
- Provides quick visibility into active incidents

---

## Architectural Design Principles
- **Automation-first SOC operations**
- **Reduced Mean Time to Detect (MTTD)**
- **Reduced Mean Time to Respond (MTTR)**
- **Scalable and modular integration**
- **Centralized visibility across incidents**

---

## Security Considerations
- All inter-component communication is performed using secured APIs
- Sensitive configuration values are masked or stored securely
- No credentials or secrets are exposed in this repository
