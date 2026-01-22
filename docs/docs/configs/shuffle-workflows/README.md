# Shuffle Automation Workflows

This directory contains exported Shuffle Automation workflow definitions
used to automate incident response actions within the SOC environment.

The workflows define the orchestration logic that processes security alerts,
performs enrichment, creates incidents, and notifies SOC analysts.

---

## Workflow Purpose
- Automate alert handling and response
- Integrate SIEM, incident response, and threat intelligence platforms
- Reduce manual intervention by SOC analysts
- Ensure consistent and repeatable incident response

---

## Workflow Capabilities
- Alert ingestion from Wazuh via webhooks
- Conditional routing based on alert severity
- Automated case creation in TheHive
- Observable analysis using Cortex
- Threat intelligence enrichment via MISP

---

## Usage Note
The workflows provided here are exported for reference and learning purposes.
They may require environment-specific customization before deployment.
