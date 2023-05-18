---
layout: post
title: SC-200\: Introduction to Microsoft 365 Threat Protection
---

# Introduction to Microsfot 365 Threat Protection

![365 Defender Products](https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/defend-across-attack-chains.png)

Extended Detection and Response (XDR) combines signals from:
* Endpoints
* Identity
* Email
* Applications

> XDR here refers to the whole ecosystem of products offered by microsoft. These include:
> * Defender for Office 365
> * Defender for IoT (& OT)
> * Defender for Endpoint (MDE)
> * Defender for Identity
> * Azure AD Identity Protection
> * Defender for Cloud Apps
> * Insider risk management
> * Microsoft Sentinel

## Detection Example

![Compromised endpoint steming from a malicious payload sent over email or USB](https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/compromised-endpoint.png)

The above example could result in telemetry, data, and remediation actions needed in:
* MDE
* Microsoft Threat Intelligence
* Microsoft Defender for 365

![Suspending user access during compromise](https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/suspend-access-compromise.png)

During an incident or following an alert risk of compromise could be mitigated by suspending user access. Whilst the device is non-compliant a device/user can be prevented from accessing corperate resources. Access can be restored when MDE signals to Intune to update AAD and CA policies.

## Modern Security Operations

![How Microsoft Defender and Sentinel are integrated into a SOC](https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/security-operations.png)

![Security Operations Model](https://learn.microsoft.com/en-us/training/wwl-sci/introduction-microsoft-365-threat-protection/media/security-operations-model.png)

Triage and Automation
* Called Tier 1 here.
* 90% TP - Base TP ratio for alert tuning.
* Automation for enabling triage teams to reduce time to resolution and effort required for triage/investigation.

Incident Management
* Called Tier 2 here.
* Provides deeper investigation into more complex attacks.
* Pilots new and unfamiliar log sources, documenting them for Tier 1.
* Tier 2 also takes on incident management.

Hunt and Incident Management
* Called Tier 3 here.
* Proactive hunting for undetected threats.
* Building new capability and alerting

## Threat Intelligence

* Provides additional context to alerting.
* Reactive technical research for active incidents.
* Proactive research into attack groups, trends, and emerging techniques.
* Strategic research based on business operations and technology.

## Investigate security incident in Microsoft 365 Defender

> Summary of linked video, video found ![here](https://mslearn.cloudguides.com/guides/Investigate%20security%20incidents%20in%20a%20hybrid%20environment%20with%20Azure%20Sentinel)

* Azure Sentinel is a cloud-native SIEM.
* Connectors for various platforms, systems, and resources.
* Integrations for automations.

Incidents page
* Overview of all open and closed incidents in the enviroment.
* Various severities and filtering options.
* Incident Views link to raw logs and source product.
* Entities are a component of incidents that are populated by the source product and the alerts that make up the incident.
    * e.g. Azure Resource, File, Hash, Malware, IP Address, etc.
    * Populated by threat intelligence and other sources.
* 'Take Action' screen contains some reccomended actions for mitiating the incident. Based on details of the incident and the entities involved.
    * e.g. Reccomendations on restricting public access to storage accounts.
* Assigning an incident, depending on the source product, will reflect that change in the source product.
    * e.g. Assigning an incident in Sentinel will assign the incident in Defender for 365.

Investigation Graph
* Helps to understand the scope of the incident. 
* Sentinel allows customer detection rules, these rules then populate the investigation graph and incident details.
    * e.g. 'Linked malicious storage artifacts'.
    * Custom Detections and Indicators can assist in linking incidents together.
* Playbooks can be actioned from here.

Defender 365 Incidents & Alerts
* Alert stories show process trees with alerts and context.
* Alert stores show a timeline of activity.

Automation Rules   
* Trigger playbooks based on incident and alert fields.

# Knowledge Check

1 . Microsoft Defender for Identity can help detect an Active Directory Domain compromise.
2. Microsoft Defender for Office 365 can help in detecting a phishing email.
3. Microsoft defender for Endpoint can help in detecting a malicious file on a device.

# Additional Reading

You should now be able to:
* Understand Microsoft 365 Defender solution by domain
* Understand Microsoft 365 Defender role in a Modern SOC

* https://learn.microsoft.com/en-us/security/cybersecurity-reference-architecture/mcra#
