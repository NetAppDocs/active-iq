## Copilot instructions for Active IQ Digital Advisor documentation

### Repository overview
Product: NetApp Active IQ Digital Advisor

*Active IQ Digital Advisor* (also called *Digital Advisor*) is a cloud-based service for monitoring and optimizing NetApp storage environments through predictive analytics, proactive support, and operational recommendations. In this repository, the product is presented as a service accessed through *NetApp Console* and driven by *AutoSupport* telemetry, dashboard widgets, and feature-specific workflows such as upgrade planning, config drift analysis, and API-based automation.

### Repository structure
- – Primary AsciiDoc topics for Digital Advisor concepts, tasks, references, and landing-page content, including watchlists, wellness, upgrades, sustainability, API services, and support workflows
- `_whatsnew/` – Date-stamped release note topics that describe feature changes and behavior updates for Digital Advisor
- `media/` – Shared images and diagrams used across product topics for dashboards, workflows, widgets, and remediation flows
- `store-redirects/` – Redirect stub pages that preserve legacy or alternate URLs, including earlier naming paths

### Product-specific context
**Architecture and components:**
- *Digital Advisor* is a cloud-based management and support service accessed through *NetApp Console*; users sign in to the Console and then authenticate to Digital Advisor with *NetApp Support Site (NSS)* credentials.
- *AutoSupport* telemetry sends configuration, status, performance, and system-event data to NetApp; Digital Advisor uses that data for risk detection, support insights, and recommendations, while *AutoSupport Upload* is the manual alternative.
- The UI is organized around dashboard *widgets* and feature areas such as *Wellness*, *Planning*, *Upgrades*, *Sustainability*, *Health Check*, *Config Drift*, *Valuable Insights*, *ClusterViewer*, and *API Services*.
- *API Services* includes an *API Catalog* organized by service area for programmatic access to data such as system information, storage efficiency, performance, health, and upgrades.
- Some remediation flows provide *Ansible* content, including firmware-update packages and config-drift playbooks with accompanying inventory data.

**Key concepts:**
- A *watchlist* is a saved collection of systems and is the main scope for dashboards, reports, and many Digital Advisor actions.
- The *Wellness Dashboard* summarizes system risks, unique risks, and corrective actions; risk status is color-coded by severity.
- *Planning* focuses on capacity thresholds and renewals, while *Upgrades* focuses on upgrade visibility and automated ONTAP upgrade-plan generation.
- *Sustainability* provides a sustainability score plus projected power, direct carbon, and heat views for supported platforms.
- *Health Check* provides a point-in-time review of the installed base against recommended best practices.
- Supported platform families referenced across this repo include *ONTAP*, *AFF*, *FAS*, *E-Series*, *StorageGRID*, and *Cloud Volumes ONTAP*; features are platform-dependent and not every feature applies to every system type.

**Naming conventions and terminology:**
- Use *Digital Advisor* as the product names.
- Treat *Watchlist*, *Wellness*, *Health Check*, *Upgrade Advisor*, *Config Drift*, *Valuable Insights*, *ClusterViewer*, and *API Services* as feature names, not generic labels.
- Common platform and integration terms include *NSS* (*NetApp Support Site*), *UM* (*Unified Manager*), *Keystone STaaS*, *MetroCluster*, *AFF*, *FAS*, *ONTAP*, *E-Series*, and *StorageGRID*.
- This repo uses *High*, *Medium*, and *No risks* severity states, and also uses *Ack* and *un-ack* for acknowledge and unacknowledge actions.

### Typical user workflows
**Access and scope systems:** Open *NetApp Console* → authenticate to *Digital Advisor* with *NSS* credentials → search for a customer, cluster, site, group, serial number, or system ID, or create a *watchlist* → work from dashboard widgets and feature pages

**Monitor and remediate health risks:** Select a *watchlist* → review *Wellness*, *Planning*, or *Health Check* widgets → inspect risks and recommended actions → acknowledge or remediate issues with linked tools such as *Unified Manager* or *Ansible* → review history or reports

**Plan upgrades and firmware changes:** Open *Upgrades* or firmware-related risk views → generate an ONTAP upgrade plan or review firmware recommendations → check blockers, warnings, or applicable packages → download provided *Ansible* package content when applicable → validate the completed update

**Automate with APIs:** Open *API Services* → browse the *API Catalog* by service area → generate or use tokens to test endpoints → pull Digital Advisor data into internal dashboards, ticketing, or reporting workflows
