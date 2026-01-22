# Automated Incident Response Workflow

This document describes the end-to-end automated incident response workflow
implemented in the SOC environment using SIEM, SOAR, and Threat Intelligence tools.
The workflow is designed to minimize manual intervention and accelerate
security incident detection, analysis, and response.

---

## Workflow Overview
The workflow begins with the detection of a security event on a monitored system
and continues through automated alert handling, enrichment, case creation,
and analyst notification.

The automation ensures consistent incident handling and reduces operational
overhead for SOC analysts.

---

## Detailed Workflow Steps

1. **Event Generation**  
   A security-related event occurs on a monitored host or application
   (e.g., failed login attempts, malware execution, unauthorized access).

2. **Detection & Alerting (Wazuh)**  
   Wazuh analyzes logs and system activity, detects suspicious behavior,
   and generates a structured security alert.

3. **Alert Ingestion (Shuffle Automation)**  
   The alert is forwarded to Shuffle Automation via webhook, where it is
   ingested and parsed for severity, source, and event type.

4. **Alert Classification & Routing**  
   Shuffle evaluates the alert context and routes it to the appropriate
   automated response workflow based on predefined logic.

5. **Case Creation (TheHive)**  
   A new incident case is automatically created in TheHive, ensuring
   centralized tracking and structured incident management.

6. **Automated Analysis (Cortex)**  
   Observables such as IP addresses, file hashes, and URLs are analyzed
   using Cortex analyzers to gather additional context.

7. **Threat Intelligence Enrichment (MISP)**  
   Indicators are correlated against known threat intelligence sources
   to identify malicious patterns and known adversaries.

8. **Analyst Notification (Discord)**  
   A real-time notification containing incident details is sent to the
   SOC team via Discord for immediate awareness and action.

---

## Workflow Outcomes
- Faster alert triage and investigation
- Reduced Mean Time to Detect (MTTD)
- Reduced Mean Time to Respond (MTTR)
- Consistent and repeatable incident handling
- Improved analyst efficiency

---

## Automation Benefits
- Eliminates repetitive manual tasks
- Standardizes incident response procedures
- Enables scalable SOC operations
- Improves response accuracy and speed
