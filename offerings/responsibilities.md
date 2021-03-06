---

copyright:
  years: 2019, 2020
lastupdated: "2020-12-24"

keywords: incident management, operations management, change management, security compliance, regulation compliance, disaster recovery

subcollection: Cloudant

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:external: target="_blank" .external}

<!-- Acrolinx: 2020-10-15 -->

# Understanding your responsibilities when you use {{site.data.keyword.cloudant_short_notm}}
{: #cloudant-responsibilities}

Learn about the management responsibilities, and terms and conditions, that you own when you use {{site.data.keyword.cloudant_short_notm}}. For a high-level view of the service types in {{site.data.keyword.cloud}}, and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for {{site.data.keyword.cloud_notm}} offerings](/docs/overview?topic=overview-shared-responsibilities). 
{: shortdesc}

Review the following sections to understand the specific responsibilities between you and {{site.data.keyword.IBM_notm}} when you use {{site.data.keyword.cloudant_short_notm}}. For the overall terms of use, see [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms). 

## Incident and operations management
{: #incident-and-ops}

Incident and operations management includes tasks such as monitoring, event management, high availability, problem determination, recovery, and full state backup and recovery. 

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|HA/DR (multi-zone region) | {{site.data.keyword.cloudant_short_notm}} stores all documents in triplicate on separate servers that are spread across three separate availability zones by default.  | |
|HA/DR (single-zone region)| {{site.data.keyword.cloudant_short_notm}} stores all documents in triplicate on three separate physical servers within the availability zone by default.  | |
|Back up and restore|   | Customer is responsible for backup and restore of data to roll back to a previous state in the database. See [{{site.data.keyword.cloudant_short_notm}} backup and recovery](/docs/Cloudant?topic=Cloudant-ibm-cloudant-backup-and-recovery) documentation for recommended tooling. |
{: caption="Table 1. Responsibilities for incident and operations" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or {{site.data.keyword.IBM_notm}} might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Change management
{: #change-management-responsibilities}

Change management includes tasks such as deployment, configuration, upgrades, patching, configuration changes, and deletion. 

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|Scaling| {{site.data.keyword.IBM_notm}} scales infrastructure to meet capacity selected by the customer.  | Customer chooses the provisioned throughput capacity for their {{site.data.keyword.cloudant_short_notm}} instances. |
|Upgrades| {{site.data.keyword.IBM_notm}} handles all upgrades and patches of the {{site.data.keyword.cloudant_short_notm}} service for the customer.  | |
{: caption="Table 2. Responsibilities for change management" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or {{site.data.keyword.IBM_notm}} might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Security and regulation compliance
{: #security-compliance-responsibilities}

Security and regulation compliance includes tasks such as security controls implementation and compliance certification. 

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|At-rest encryption| By default, {{site.data.keyword.IBM_notm}} encrypts all disks by using {{site.data.keyword.cloudant_short_notm}}-managed encryption keys.   | If the customer wants bring-your-own-key (BYOK) encryption, then the customer is required to use Key Protect to store the customer-managed encryption key. The customer must select an appropriate key management service instance, and select a disk encryption key option during provisioning of an {{site.data.keyword.cloudant_short_notm}} Dedicated Hardware plan instance. |
{: caption="Table 3. Responsibilities for security and regulation compliance" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or {{site.data.keyword.IBM_notm}} might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Disaster recovery
{: #disaster-recovery-responsibilities}

Disaster recovery includes the following tasks:

- Provide dependencies on disaster recovery sites.
- Provision disaster recovery environments.
- Back up data and configuration.
- Replicate data and configuration to the disaster recovery environment.
- Fail over disaster events.

| Task | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|----------|-----------------------|--------|
|HA/DR (cross-region)|  | Customer is responsible for creating more {{site.data.keyword.cloudant_short_notm}} instances in separate regions and configuring replications to achieve the cross-region HA/DR architecture they want. See [Configuring {{site.data.keyword.cloudant_short_notm}} for cross-region disaster recovery](/docs/Cloudant?topic=Cloudant-configuring-ibm-cloudant-for-cross-region-disaster-recovery) for more details.  |
{: caption="Table 4. Responsibilities for disaster recovery" caption-side="top"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or {{site.data.keyword.IBM_notm}} might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}
