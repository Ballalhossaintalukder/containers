---

copyright:
  years: 2024, 2025

lastupdated: "2025-07-01"


keywords: change log, version history, 1.31

subcollection: containers

---

{{site.data.keyword.attribute-definition-list}}

<!-- The content in this topic is auto-generated except for reuse-snippets indicated with {[ ]}. -->


# 1.31 version change log
{: #changelog_131}

View information of version changes for major, minor, and patch updates that are available for your {{site.data.keyword.containerlong}} clusters that run this version. Changes include updates to Kubernetes and {{site.data.keyword.cloud_notm}} Provider components.
{: shortdesc}

## Overview
{: #changelog_overview_131}

In Kubernetes, most new beta features are disabled by default. Alpha features, which are subject to change, are disabled in all versions. For more information, see the [Default service settings for Kubernetes components](/docs/containers?topic=containers-service-settings) and the [feature gates](/docs/containers?topic=containers-service-settings#feature-gates) for each version.

For more information about major, minor, and patch versions and preparation actions between minor versions, see [Kubernetes versions](/docs/containers?topic=containers-cs_versions).
{: tip}

Check the [Security Bulletins on {{site.data.keyword.cloud_notm}} Status](https://cloud.ibm.com/status?component=containers-kubernetes&selected=security){: external} for security vulnerabilities that affect {{site.data.keyword.containerlong_notm}}. You can filter the results to view only Kubernetes Cluster security bulletins that are relevant to {{site.data.keyword.containerlong_notm}}. Change log entries that address other security vulnerabilities but don't also refer to an {{site.data.keyword.IBM_notm}} security bulletin are for vulnerabilities that are not known to affect {{site.data.keyword.containerlong_notm}} in normal usage. If you run privileged containers, run commands on the workers, or execute untrusted code, then you might be at risk.

Some change logs are for _worker node fix packs_, and apply only to worker nodes. You must [apply these patches](/docs/containers?topic=containers-kubernetes-service-cli#cs_worker_update) to ensure security compliance for your worker nodes. These worker node fix packs can be at a higher version than the master because some build fix packs are specific to worker nodes. Other change logs are for _master fix packs_, and apply only to the cluster master. Master fix packs might not be automatically applied. You can choose to [apply them manually](/docs/containers?topic=containers-kubernetes-service-cli#cs_cluster_update). For more information about patch types, see [Update types](/docs/containers?topic=containers-cs_versions#update_types).
{: note}



## Version 1.31
{: #131_components}


### Master fix pack 1.31.9_1553, released 18 June 2025
{: #1319_1553_M}

The following table shows the changes that are in the master fix pack 1.31.9_1553. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.28.3 | v3.28.4 | See the [Calico release notes](https://docs.tigera.io/calico/3.28/release-notes/#v3.28.4){: external}. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.5.17 | v2.5.19 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.9-1 | v1.31.9-4 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | d1545bd | 38dc95c | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.13 | v2.10.14 | New version contains updates and security fixes. |
| Tigera Operator | v1.34.8 | v1.34.11 | See the [Tigera Operator release notes](https://github.com/tigera/operator/releases/tag/v1.34.11){: external}. |
{: caption="Changes since version 1.31.9_1550" caption-side="bottom"}



### Worker node fix pack 1.31.9_1551, released 04 June 2025
{: #cl-boms-1319_1551_W}

The following table shows the components included in the worker node fix pack 1.31.9_1551. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-60-generic|Resolves the following CVEs: [CVE-2024-45774](https://nvd.nist.gov/vuln/detail/CVE-2024-45774){: external}, [CVE-2024-45775](https://nvd.nist.gov/vuln/detail/CVE-2024-45775){: external}, [CVE-2024-45776](https://nvd.nist.gov/vuln/detail/CVE-2024-45776){: external}, [CVE-2024-45777](https://nvd.nist.gov/vuln/detail/CVE-2024-45777){: external}, [CVE-2024-45778](https://nvd.nist.gov/vuln/detail/CVE-2024-45778){: external}, [CVE-2024-45779](https://nvd.nist.gov/vuln/detail/CVE-2024-45779){: external}, [CVE-2024-45780](https://nvd.nist.gov/vuln/detail/CVE-2024-45780){: external}, [CVE-2024-45781](https://nvd.nist.gov/vuln/detail/CVE-2024-45781){: external}, [CVE-2024-45782](https://nvd.nist.gov/vuln/detail/CVE-2024-45782){: external}, [CVE-2024-45783](https://nvd.nist.gov/vuln/detail/CVE-2024-45783){: external}, [CVE-2025-0622](https://nvd.nist.gov/vuln/detail/CVE-2025-0622){: external}, [CVE-2025-0624](https://nvd.nist.gov/vuln/detail/CVE-2025-0624){: external}, [CVE-2025-0677](https://nvd.nist.gov/vuln/detail/CVE-2025-0677){: external}, [CVE-2025-0678](https://nvd.nist.gov/vuln/detail/CVE-2025-0678){: external}, [CVE-2025-0684](https://nvd.nist.gov/vuln/detail/CVE-2025-0684){: external}, [CVE-2025-0685](https://nvd.nist.gov/vuln/detail/CVE-2025-0685){: external}, [CVE-2025-0686](https://nvd.nist.gov/vuln/detail/CVE-2025-0686){: external}, [CVE-2025-0689](https://nvd.nist.gov/vuln/detail/CVE-2025-0689){: external}, [CVE-2025-0690](https://nvd.nist.gov/vuln/detail/CVE-2025-0690){: external}, [CVE-2025-1118](https://nvd.nist.gov/vuln/detail/CVE-2025-1118){: external}, [CVE-2025-1125](https://nvd.nist.gov/vuln/detail/CVE-2025-1125){: external}, [CVE-2025-29087](https://nvd.nist.gov/vuln/detail/CVE-2025-29087){: external}, [CVE-2025-29088](https://nvd.nist.gov/vuln/detail/CVE-2025-29088){: external}, [CVE-2025-3277](https://nvd.nist.gov/vuln/detail/CVE-2025-3277){: external}, [CVE-2025-3576](https://nvd.nist.gov/vuln/detail/CVE-2025-3576){: external}, [CVE-2025-4373](https://nvd.nist.gov/vuln/detail/CVE-2025-4373){: external}, [CVE-2025-46836](https://nvd.nist.gov/vuln/detail/CVE-2025-46836){: external}, and [CVE-2025-47273](https://nvd.nist.gov/vuln/detail/CVE-2025-47273){: external}.|
|Kubernetes|1.31.9|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.9).|
|containerd|1.7.27|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.27).|
|HAProxy|978e3c26ee7634e39a940696aaf57d9e374db5ce|N/A|
|GPU Device Plug-in and Installer|9c52a5f3c684d3da2808c70936332fd18493d0c7|N/A|
{: caption="1.31.9_1551 fix pack." caption-side="bottom"}
{: #cl-boms-1319_1551_W-component-table}



### Master fix pack 1.31.9_1550, released 28 May 2025
{: #1319_1550_M}

The following table shows the changes that are in the master fix pack 1.31.9_1550. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.6.8 | v1.6.9 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.7-6 | v1.31.9-1 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} for Classic plug-in and monitor | 449 | 450 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | v1.1.5 | v1.1.6 | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.12 | v2.10.13 | New version contains updates and security fixes. |
| Kubernetes | v1.31.7 | v1.31.9 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.9){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 3232 | 3293 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.26 | v0.13.28 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.28){: external}. |
{: caption="Changes since version 1.31.7_1547" caption-side="bottom"}



### Worker node fix pack 1.31.7_1549, released 19 May 2025
{: #cl-boms-1317_1549_W}

The following table shows the components included in the worker node fix pack 1.31.7_1549. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-60-generic|Resolves the following CVEs: [CVE-2024-36476](https://nvd.nist.gov/vuln/detail/CVE-2024-36476){: external}, [CVE-2024-39282](https://nvd.nist.gov/vuln/detail/CVE-2024-39282){: external}, [CVE-2024-41013](https://nvd.nist.gov/vuln/detail/CVE-2024-41013){: external}, [CVE-2024-45774](https://nvd.nist.gov/vuln/detail/CVE-2024-45774){: external}, [CVE-2024-45775](https://nvd.nist.gov/vuln/detail/CVE-2024-45775){: external}, [CVE-2024-45776](https://nvd.nist.gov/vuln/detail/CVE-2024-45776){: external}, [CVE-2024-45777](https://nvd.nist.gov/vuln/detail/CVE-2024-45777){: external}, [CVE-2024-45778](https://nvd.nist.gov/vuln/detail/CVE-2024-45778){: external}, [CVE-2024-45779](https://nvd.nist.gov/vuln/detail/CVE-2024-45779){: external}, [CVE-2024-45780](https://nvd.nist.gov/vuln/detail/CVE-2024-45780){: external}, [CVE-2024-45781](https://nvd.nist.gov/vuln/detail/CVE-2024-45781){: external}, [CVE-2024-45782](https://nvd.nist.gov/vuln/detail/CVE-2024-45782){: external}, [CVE-2024-45783](https://nvd.nist.gov/vuln/detail/CVE-2024-45783){: external}, [CVE-2024-47408](https://nvd.nist.gov/vuln/detail/CVE-2024-47408){: external}, [CVE-2024-47736](https://nvd.nist.gov/vuln/detail/CVE-2024-47736){: external}, [CVE-2024-49568](https://nvd.nist.gov/vuln/detail/CVE-2024-49568){: external}, [CVE-2024-49571](https://nvd.nist.gov/vuln/detail/CVE-2024-49571){: external}, [CVE-2024-53125](https://nvd.nist.gov/vuln/detail/CVE-2024-53125){: external}, [CVE-2024-53179](https://nvd.nist.gov/vuln/detail/CVE-2024-53179){: external}, [CVE-2024-53685](https://nvd.nist.gov/vuln/detail/CVE-2024-53685){: external}, [CVE-2024-53687](https://nvd.nist.gov/vuln/detail/CVE-2024-53687){: external}, [CVE-2024-53690](https://nvd.nist.gov/vuln/detail/CVE-2024-53690){: external}, [CVE-2024-54193](https://nvd.nist.gov/vuln/detail/CVE-2024-54193){: external}, [CVE-2024-54455](https://nvd.nist.gov/vuln/detail/CVE-2024-54455){: external}, [CVE-2024-54460](https://nvd.nist.gov/vuln/detail/CVE-2024-54460){: external}, [CVE-2024-54683](https://nvd.nist.gov/vuln/detail/CVE-2024-54683){: external}, [CVE-2024-55639](https://nvd.nist.gov/vuln/detail/CVE-2024-55639){: external}, [CVE-2024-55881](https://nvd.nist.gov/vuln/detail/CVE-2024-55881){: external}, [CVE-2024-55916](https://nvd.nist.gov/vuln/detail/CVE-2024-55916){: external}, [CVE-2024-56369](https://nvd.nist.gov/vuln/detail/CVE-2024-56369){: external}, [CVE-2024-56372](https://nvd.nist.gov/vuln/detail/CVE-2024-56372){: external}, [CVE-2024-56652](https://nvd.nist.gov/vuln/detail/CVE-2024-56652){: external}, [CVE-2024-56653](https://nvd.nist.gov/vuln/detail/CVE-2024-56653){: external}, [CVE-2024-56654](https://nvd.nist.gov/vuln/detail/CVE-2024-56654){: external}, [CVE-2024-56656](https://nvd.nist.gov/vuln/detail/CVE-2024-56656){: external}, [CVE-2024-56657](https://nvd.nist.gov/vuln/detail/CVE-2024-56657){: external}, [CVE-2024-56659](https://nvd.nist.gov/vuln/detail/CVE-2024-56659){: external}, [CVE-2024-56660](https://nvd.nist.gov/vuln/detail/CVE-2024-56660){: external}, [CVE-2024-56662](https://nvd.nist.gov/vuln/detail/CVE-2024-56662){: external}, [CVE-2024-56664](https://nvd.nist.gov/vuln/detail/CVE-2024-56664){: external}, [CVE-2024-56667](https://nvd.nist.gov/vuln/detail/CVE-2024-56667){: external}, [CVE-2024-56670](https://nvd.nist.gov/vuln/detail/CVE-2024-56670){: external}, [CVE-2024-56675](https://nvd.nist.gov/vuln/detail/CVE-2024-56675){: external}, [CVE-2024-56709](https://nvd.nist.gov/vuln/detail/CVE-2024-56709){: external}, [CVE-2024-56710](https://nvd.nist.gov/vuln/detail/CVE-2024-56710){: external}, [CVE-2024-56715](https://nvd.nist.gov/vuln/detail/CVE-2024-56715){: external}, [CVE-2024-56716](https://nvd.nist.gov/vuln/detail/CVE-2024-56716){: external}, [CVE-2024-56717](https://nvd.nist.gov/vuln/detail/CVE-2024-56717){: external}, [CVE-2024-56718](https://nvd.nist.gov/vuln/detail/CVE-2024-56718){: external}, [CVE-2024-56758](https://nvd.nist.gov/vuln/detail/CVE-2024-56758){: external}, [CVE-2024-56759](https://nvd.nist.gov/vuln/detail/CVE-2024-56759){: external}, [CVE-2024-56760](https://nvd.nist.gov/vuln/detail/CVE-2024-56760){: external}, [CVE-2024-56761](https://nvd.nist.gov/vuln/detail/CVE-2024-56761){: external}, [CVE-2024-56763](https://nvd.nist.gov/vuln/detail/CVE-2024-56763){: external}, [CVE-2024-56764](https://nvd.nist.gov/vuln/detail/CVE-2024-56764){: external}, [CVE-2024-56767](https://nvd.nist.gov/vuln/detail/CVE-2024-56767){: external}, [CVE-2024-56769](https://nvd.nist.gov/vuln/detail/CVE-2024-56769){: external}, [CVE-2024-56770](https://nvd.nist.gov/vuln/detail/CVE-2024-56770){: external}, [CVE-2024-57791](https://nvd.nist.gov/vuln/detail/CVE-2024-57791){: external}, [CVE-2024-57792](https://nvd.nist.gov/vuln/detail/CVE-2024-57792){: external}, [CVE-2024-57793](https://nvd.nist.gov/vuln/detail/CVE-2024-57793){: external}, [CVE-2024-57801](https://nvd.nist.gov/vuln/detail/CVE-2024-57801){: external}, [CVE-2024-57802](https://nvd.nist.gov/vuln/detail/CVE-2024-57802){: external}, [CVE-2024-57804](https://nvd.nist.gov/vuln/detail/CVE-2024-57804){: external}, [CVE-2024-57806](https://nvd.nist.gov/vuln/detail/CVE-2024-57806){: external}, [CVE-2024-57807](https://nvd.nist.gov/vuln/detail/CVE-2024-57807){: external}, [CVE-2024-57841](https://nvd.nist.gov/vuln/detail/CVE-2024-57841){: external}, [CVE-2024-57879](https://nvd.nist.gov/vuln/detail/CVE-2024-57879){: external}, [CVE-2024-57882](https://nvd.nist.gov/vuln/detail/CVE-2024-57882){: external}, [CVE-2024-57883](https://nvd.nist.gov/vuln/detail/CVE-2024-57883){: external}, [CVE-2024-57884](https://nvd.nist.gov/vuln/detail/CVE-2024-57884){: external}, [CVE-2024-57885](https://nvd.nist.gov/vuln/detail/CVE-2024-57885){: external}, [CVE-2024-57887](https://nvd.nist.gov/vuln/detail/CVE-2024-57887){: external}, [CVE-2024-57888](https://nvd.nist.gov/vuln/detail/CVE-2024-57888){: external}, [CVE-2024-57889](https://nvd.nist.gov/vuln/detail/CVE-2024-57889){: external}, [CVE-2024-57890](https://nvd.nist.gov/vuln/detail/CVE-2024-57890){: external}, [CVE-2024-57892](https://nvd.nist.gov/vuln/detail/CVE-2024-57892){: external}, [CVE-2024-57893](https://nvd.nist.gov/vuln/detail/CVE-2024-57893){: external}, [CVE-2024-57895](https://nvd.nist.gov/vuln/detail/CVE-2024-57895){: external}, [CVE-2024-57896](https://nvd.nist.gov/vuln/detail/CVE-2024-57896){: external}, [CVE-2024-57897](https://nvd.nist.gov/vuln/detail/CVE-2024-57897){: external}, [CVE-2024-57898](https://nvd.nist.gov/vuln/detail/CVE-2024-57898){: external}, [CVE-2024-57899](https://nvd.nist.gov/vuln/detail/CVE-2024-57899){: external}, [CVE-2024-57900](https://nvd.nist.gov/vuln/detail/CVE-2024-57900){: external}, [CVE-2024-57901](https://nvd.nist.gov/vuln/detail/CVE-2024-57901){: external}, [CVE-2024-57902](https://nvd.nist.gov/vuln/detail/CVE-2024-57902){: external}, [CVE-2024-57903](https://nvd.nist.gov/vuln/detail/CVE-2024-57903){: external}, [CVE-2024-57904](https://nvd.nist.gov/vuln/detail/CVE-2024-57904){: external}, [CVE-2024-57906](https://nvd.nist.gov/vuln/detail/CVE-2024-57906){: external}, [CVE-2024-57907](https://nvd.nist.gov/vuln/detail/CVE-2024-57907){: external}, [CVE-2024-57908](https://nvd.nist.gov/vuln/detail/CVE-2024-57908){: external}, [CVE-2024-57910](https://nvd.nist.gov/vuln/detail/CVE-2024-57910){: external}, [CVE-2024-57911](https://nvd.nist.gov/vuln/detail/CVE-2024-57911){: external}, [CVE-2024-57912](https://nvd.nist.gov/vuln/detail/CVE-2024-57912){: external}, [CVE-2024-57913](https://nvd.nist.gov/vuln/detail/CVE-2024-57913){: external}, [CVE-2024-57916](https://nvd.nist.gov/vuln/detail/CVE-2024-57916){: external}, [CVE-2024-57917](https://nvd.nist.gov/vuln/detail/CVE-2024-57917){: external}, [CVE-2024-57925](https://nvd.nist.gov/vuln/detail/CVE-2024-57925){: external}, [CVE-2024-57926](https://nvd.nist.gov/vuln/detail/CVE-2024-57926){: external}, [CVE-2024-57929](https://nvd.nist.gov/vuln/detail/CVE-2024-57929){: external}, [CVE-2024-57931](https://nvd.nist.gov/vuln/detail/CVE-2024-57931){: external}, [CVE-2024-57932](https://nvd.nist.gov/vuln/detail/CVE-2024-57932){: external}, [CVE-2024-57933](https://nvd.nist.gov/vuln/detail/CVE-2024-57933){: external}, [CVE-2024-57938](https://nvd.nist.gov/vuln/detail/CVE-2024-57938){: external}, [CVE-2024-57939](https://nvd.nist.gov/vuln/detail/CVE-2024-57939){: external}, [CVE-2024-57940](https://nvd.nist.gov/vuln/detail/CVE-2024-57940){: external}, [CVE-2024-57945](https://nvd.nist.gov/vuln/detail/CVE-2024-57945){: external}, [CVE-2024-57946](https://nvd.nist.gov/vuln/detail/CVE-2024-57946){: external}, [CVE-2025-0622](https://nvd.nist.gov/vuln/detail/CVE-2025-0622){: external}, [CVE-2025-0624](https://nvd.nist.gov/vuln/detail/CVE-2025-0624){: external}, [CVE-2025-0677](https://nvd.nist.gov/vuln/detail/CVE-2025-0677){: external}, [CVE-2025-0678](https://nvd.nist.gov/vuln/detail/CVE-2025-0678){: external}, [CVE-2025-0684](https://nvd.nist.gov/vuln/detail/CVE-2025-0684){: external}, [CVE-2025-0685](https://nvd.nist.gov/vuln/detail/CVE-2025-0685){: external}, [CVE-2025-0686](https://nvd.nist.gov/vuln/detail/CVE-2025-0686){: external}, [CVE-2025-0689](https://nvd.nist.gov/vuln/detail/CVE-2025-0689){: external}, [CVE-2025-0690](https://nvd.nist.gov/vuln/detail/CVE-2025-0690){: external}, [CVE-2025-1118](https://nvd.nist.gov/vuln/detail/CVE-2025-1118){: external}, [CVE-2025-1125](https://nvd.nist.gov/vuln/detail/CVE-2025-1125){: external}, [CVE-2025-21631](https://nvd.nist.gov/vuln/detail/CVE-2025-21631){: external}, [CVE-2025-21632](https://nvd.nist.gov/vuln/detail/CVE-2025-21632){: external}, [CVE-2025-21634](https://nvd.nist.gov/vuln/detail/CVE-2025-21634){: external}, [CVE-2025-21635](https://nvd.nist.gov/vuln/detail/CVE-2025-21635){: external}, [CVE-2025-21636](https://nvd.nist.gov/vuln/detail/CVE-2025-21636){: external}, [CVE-2025-21637](https://nvd.nist.gov/vuln/detail/CVE-2025-21637){: external}, [CVE-2025-21638](https://nvd.nist.gov/vuln/detail/CVE-2025-21638){: external}, [CVE-2025-21639](https://nvd.nist.gov/vuln/detail/CVE-2025-21639){: external}, [CVE-2025-21640](https://nvd.nist.gov/vuln/detail/CVE-2025-21640){: external}, [CVE-2025-21642](https://nvd.nist.gov/vuln/detail/CVE-2025-21642){: external}, [CVE-2025-21643](https://nvd.nist.gov/vuln/detail/CVE-2025-21643){: external}, [CVE-2025-21645](https://nvd.nist.gov/vuln/detail/CVE-2025-21645){: external}, [CVE-2025-21646](https://nvd.nist.gov/vuln/detail/CVE-2025-21646){: external}, [CVE-2025-21647](https://nvd.nist.gov/vuln/detail/CVE-2025-21647){: external}, [CVE-2025-21648](https://nvd.nist.gov/vuln/detail/CVE-2025-21648){: external}, [CVE-2025-21649](https://nvd.nist.gov/vuln/detail/CVE-2025-21649){: external}, [CVE-2025-21650](https://nvd.nist.gov/vuln/detail/CVE-2025-21650){: external}, [CVE-2025-21651](https://nvd.nist.gov/vuln/detail/CVE-2025-21651){: external}, [CVE-2025-21652](https://nvd.nist.gov/vuln/detail/CVE-2025-21652){: external}, [CVE-2025-21653](https://nvd.nist.gov/vuln/detail/CVE-2025-21653){: external}, [CVE-2025-21654](https://nvd.nist.gov/vuln/detail/CVE-2025-21654){: external}, [CVE-2025-21655](https://nvd.nist.gov/vuln/detail/CVE-2025-21655){: external}, [CVE-2025-21656](https://nvd.nist.gov/vuln/detail/CVE-2025-21656){: external}, [CVE-2025-21658](https://nvd.nist.gov/vuln/detail/CVE-2025-21658){: external}, [CVE-2025-21659](https://nvd.nist.gov/vuln/detail/CVE-2025-21659){: external}, [CVE-2025-21660](https://nvd.nist.gov/vuln/detail/CVE-2025-21660){: external}, [CVE-2025-21662](https://nvd.nist.gov/vuln/detail/CVE-2025-21662){: external}, [CVE-2025-21663](https://nvd.nist.gov/vuln/detail/CVE-2025-21663){: external}, [CVE-2025-21664](https://nvd.nist.gov/vuln/detail/CVE-2025-21664){: external}, [CVE-2025-21971](https://nvd.nist.gov/vuln/detail/CVE-2025-21971){: external}, and [CVE-2025-22247](https://nvd.nist.gov/vuln/detail/CVE-2025-22247){: external}.|
|UBUNTU_20_04|5.4.0-216-generic|Resolves the following CVEs: [CVE-2021-47191](https://nvd.nist.gov/vuln/detail/CVE-2021-47191){: external}, [CVE-2023-52664](https://nvd.nist.gov/vuln/detail/CVE-2023-52664){: external}, [CVE-2023-52741](https://nvd.nist.gov/vuln/detail/CVE-2023-52741){: external}, [CVE-2023-52927](https://nvd.nist.gov/vuln/detail/CVE-2023-52927){: external}, [CVE-2024-26689](https://nvd.nist.gov/vuln/detail/CVE-2024-26689){: external}, [CVE-2024-26982](https://nvd.nist.gov/vuln/detail/CVE-2024-26982){: external}, [CVE-2024-26996](https://nvd.nist.gov/vuln/detail/CVE-2024-26996){: external}, [CVE-2024-50055](https://nvd.nist.gov/vuln/detail/CVE-2024-50055){: external}, [CVE-2024-56599](https://nvd.nist.gov/vuln/detail/CVE-2024-56599){: external}, [CVE-2024-57973](https://nvd.nist.gov/vuln/detail/CVE-2024-57973){: external}, [CVE-2024-57977](https://nvd.nist.gov/vuln/detail/CVE-2024-57977){: external}, [CVE-2024-57979](https://nvd.nist.gov/vuln/detail/CVE-2024-57979){: external}, [CVE-2024-57980](https://nvd.nist.gov/vuln/detail/CVE-2024-57980){: external}, [CVE-2024-57981](https://nvd.nist.gov/vuln/detail/CVE-2024-57981){: external}, [CVE-2024-57986](https://nvd.nist.gov/vuln/detail/CVE-2024-57986){: external}, [CVE-2024-58001](https://nvd.nist.gov/vuln/detail/CVE-2024-58001){: external}, [CVE-2024-58002](https://nvd.nist.gov/vuln/detail/CVE-2024-58002){: external}, [CVE-2024-58007](https://nvd.nist.gov/vuln/detail/CVE-2024-58007){: external}, [CVE-2024-58009](https://nvd.nist.gov/vuln/detail/CVE-2024-58009){: external}, [CVE-2024-58010](https://nvd.nist.gov/vuln/detail/CVE-2024-58010){: external}, [CVE-2024-58014](https://nvd.nist.gov/vuln/detail/CVE-2024-58014){: external}, [CVE-2024-58017](https://nvd.nist.gov/vuln/detail/CVE-2024-58017){: external}, [CVE-2024-58020](https://nvd.nist.gov/vuln/detail/CVE-2024-58020){: external}, [CVE-2024-58051](https://nvd.nist.gov/vuln/detail/CVE-2024-58051){: external}, [CVE-2024-58052](https://nvd.nist.gov/vuln/detail/CVE-2024-58052){: external}, [CVE-2024-58055](https://nvd.nist.gov/vuln/detail/CVE-2024-58055){: external}, [CVE-2024-58058](https://nvd.nist.gov/vuln/detail/CVE-2024-58058){: external}, [CVE-2024-58063](https://nvd.nist.gov/vuln/detail/CVE-2024-58063){: external}, [CVE-2024-58069](https://nvd.nist.gov/vuln/detail/CVE-2024-58069){: external}, [CVE-2024-58071](https://nvd.nist.gov/vuln/detail/CVE-2024-58071){: external}, [CVE-2024-58072](https://nvd.nist.gov/vuln/detail/CVE-2024-58072){: external}, [CVE-2024-58083](https://nvd.nist.gov/vuln/detail/CVE-2024-58083){: external}, [CVE-2024-58085](https://nvd.nist.gov/vuln/detail/CVE-2024-58085){: external}, [CVE-2024-58090](https://nvd.nist.gov/vuln/detail/CVE-2024-58090){: external}, [CVE-2025-21647](https://nvd.nist.gov/vuln/detail/CVE-2025-21647){: external}, [CVE-2025-21704](https://nvd.nist.gov/vuln/detail/CVE-2025-21704){: external}, [CVE-2025-21708](https://nvd.nist.gov/vuln/detail/CVE-2025-21708){: external}, [CVE-2025-21715](https://nvd.nist.gov/vuln/detail/CVE-2025-21715){: external}, [CVE-2025-21718](https://nvd.nist.gov/vuln/detail/CVE-2025-21718){: external}, [CVE-2025-21719](https://nvd.nist.gov/vuln/detail/CVE-2025-21719){: external}, [CVE-2025-21721](https://nvd.nist.gov/vuln/detail/CVE-2025-21721){: external}, [CVE-2025-21722](https://nvd.nist.gov/vuln/detail/CVE-2025-21722){: external}, [CVE-2025-21728](https://nvd.nist.gov/vuln/detail/CVE-2025-21728){: external}, [CVE-2025-21731](https://nvd.nist.gov/vuln/detail/CVE-2025-21731){: external}, [CVE-2025-21735](https://nvd.nist.gov/vuln/detail/CVE-2025-21735){: external}, [CVE-2025-21736](https://nvd.nist.gov/vuln/detail/CVE-2025-21736){: external}, [CVE-2025-21744](https://nvd.nist.gov/vuln/detail/CVE-2025-21744){: external}, [CVE-2025-21749](https://nvd.nist.gov/vuln/detail/CVE-2025-21749){: external}, [CVE-2025-21753](https://nvd.nist.gov/vuln/detail/CVE-2025-21753){: external}, [CVE-2025-21760](https://nvd.nist.gov/vuln/detail/CVE-2025-21760){: external}, [CVE-2025-21761](https://nvd.nist.gov/vuln/detail/CVE-2025-21761){: external}, [CVE-2025-21762](https://nvd.nist.gov/vuln/detail/CVE-2025-21762){: external}, [CVE-2025-21763](https://nvd.nist.gov/vuln/detail/CVE-2025-21763){: external}, [CVE-2025-21764](https://nvd.nist.gov/vuln/detail/CVE-2025-21764){: external}, [CVE-2025-21765](https://nvd.nist.gov/vuln/detail/CVE-2025-21765){: external}, [CVE-2025-21772](https://nvd.nist.gov/vuln/detail/CVE-2025-21772){: external}, [CVE-2025-21776](https://nvd.nist.gov/vuln/detail/CVE-2025-21776){: external}, [CVE-2025-21781](https://nvd.nist.gov/vuln/detail/CVE-2025-21781){: external}, [CVE-2025-21782](https://nvd.nist.gov/vuln/detail/CVE-2025-21782){: external}, [CVE-2025-21785](https://nvd.nist.gov/vuln/detail/CVE-2025-21785){: external}, [CVE-2025-21787](https://nvd.nist.gov/vuln/detail/CVE-2025-21787){: external}, [CVE-2025-21791](https://nvd.nist.gov/vuln/detail/CVE-2025-21791){: external}, [CVE-2025-21806](https://nvd.nist.gov/vuln/detail/CVE-2025-21806){: external}, [CVE-2025-21811](https://nvd.nist.gov/vuln/detail/CVE-2025-21811){: external}, [CVE-2025-21814](https://nvd.nist.gov/vuln/detail/CVE-2025-21814){: external}, [CVE-2025-21823](https://nvd.nist.gov/vuln/detail/CVE-2025-21823){: external}, [CVE-2025-21835](https://nvd.nist.gov/vuln/detail/CVE-2025-21835){: external}, [CVE-2025-21846](https://nvd.nist.gov/vuln/detail/CVE-2025-21846){: external}, [CVE-2025-21848](https://nvd.nist.gov/vuln/detail/CVE-2025-21848){: external}, [CVE-2025-21858](https://nvd.nist.gov/vuln/detail/CVE-2025-21858){: external}, [CVE-2025-21859](https://nvd.nist.gov/vuln/detail/CVE-2025-21859){: external}, [CVE-2025-21862](https://nvd.nist.gov/vuln/detail/CVE-2025-21862){: external}, [CVE-2025-21865](https://nvd.nist.gov/vuln/detail/CVE-2025-21865){: external}, [CVE-2025-21866](https://nvd.nist.gov/vuln/detail/CVE-2025-21866){: external}, [CVE-2025-21871](https://nvd.nist.gov/vuln/detail/CVE-2025-21871){: external}, [CVE-2025-21877](https://nvd.nist.gov/vuln/detail/CVE-2025-21877){: external}, [CVE-2025-21971](https://nvd.nist.gov/vuln/detail/CVE-2025-21971){: external}, [CVE-2025-22247](https://nvd.nist.gov/vuln/detail/CVE-2025-22247){: external}, [CVE-2025-32906](https://nvd.nist.gov/vuln/detail/CVE-2025-32906){: external}, [CVE-2025-32909](https://nvd.nist.gov/vuln/detail/CVE-2025-32909){: external}, [CVE-2025-32910](https://nvd.nist.gov/vuln/detail/CVE-2025-32910){: external}, [CVE-2025-32911](https://nvd.nist.gov/vuln/detail/CVE-2025-32911){: external}, [CVE-2025-32912](https://nvd.nist.gov/vuln/detail/CVE-2025-32912){: external}, [CVE-2025-32913](https://nvd.nist.gov/vuln/detail/CVE-2025-32913){: external}, [CVE-2025-32914](https://nvd.nist.gov/vuln/detail/CVE-2025-32914){: external}, [CVE-2025-46420](https://nvd.nist.gov/vuln/detail/CVE-2025-46420){: external}, and [CVE-2025-46421](https://nvd.nist.gov/vuln/detail/CVE-2025-46421){: external}.|
|Kubernetes|1.31.7|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.7).|
|containerd|1.7.27|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.27).|
|HAProxy|978e3c26ee7634e39a940696aaf57d9e374db5ce|N/A|
|GPU Device Plug-in and Installer|9c52a5f3c684d3da2808c70936332fd18493d0c7|N/A|
{: caption="1.31.7_1549 fix pack." caption-side="bottom"}
{: #cl-boms-1317_1549_W-component-table}



### Worker node fix pack 1.31.7_1548, released 07 May 2025
{: #cl-boms-1317_1548_W}

The following table shows the components included in the worker node fix pack 1.31.7_1548. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-58-generic|Resolves the following CVEs: [CVE-2024-56653](https://nvd.nist.gov/vuln/detail/CVE-2024-56653){: external}, [CVE-2025-1632](https://nvd.nist.gov/vuln/detail/CVE-2025-1632){: external}, [CVE-2025-25724](https://nvd.nist.gov/vuln/detail/CVE-2025-25724){: external}, [CVE-2025-32414](https://nvd.nist.gov/vuln/detail/CVE-2025-32414){: external}, [CVE-2025-32415](https://nvd.nist.gov/vuln/detail/CVE-2025-32415){: external}, and [CVE-2025-32728](https://nvd.nist.gov/vuln/detail/CVE-2025-32728){: external}.|
|UBUNTU_20_04|5.4.0-212-generic|Resolves the following CVEs: [CVE-2023-52664](https://nvd.nist.gov/vuln/detail/CVE-2023-52664){: external}, [CVE-2023-52927](https://nvd.nist.gov/vuln/detail/CVE-2023-52927){: external}, [CVE-2024-26689](https://nvd.nist.gov/vuln/detail/CVE-2024-26689){: external}, [CVE-2025-25724](https://nvd.nist.gov/vuln/detail/CVE-2025-25724){: external}, [CVE-2025-32414](https://nvd.nist.gov/vuln/detail/CVE-2025-32414){: external}, [CVE-2025-32415](https://nvd.nist.gov/vuln/detail/CVE-2025-32415){: external}, and [CVE-2025-32728](https://nvd.nist.gov/vuln/detail/CVE-2025-32728){: external}.|
|Kubernetes|1.31.7|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.7).|
|containerd|1.7.27|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.27).|
|HAProxy|978e3c26ee7634e39a940696aaf57d9e374db5ce|Resolves the following CVEs: [CVE-2024-12243](https://nvd.nist.gov/vuln/detail/CVE-2024-12243){: external}, and [CVE-2024-12133](https://nvd.nist.gov/vuln/detail/CVE-2024-12133){: external}.|
|GPU Device Plug-in and Installer|9c52a5f3c684d3da2808c70936332fd18493d0c7|Resolves the following CVEs: [CVE-2024-12243](https://nvd.nist.gov/vuln/detail/CVE-2024-12243){: external}, and [CVE-2024-12133](https://nvd.nist.gov/vuln/detail/CVE-2024-12133){: external}.|
{: caption="1.31.7_1548 fix pack." caption-side="bottom"}
{: #cl-boms-1317_1548_W-component-table}



### Master fix pack 1.31.7_1547, released 30 April 2025
{: #1317_1547_M}

The following table shows the changes that are in the master fix pack 1.31.7_1547. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.28.2 | v3.28.3 | See the [Calico release notes](https://docs.tigera.io/calico/3.28/release-notes/#v3.28.3){: external}. |
| Cluster health image | v1.6.7 | v1.6.8 | New version contains updates and security fixes. |
| etcd | v3.5.18 | v3.5.21 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.21){: external}. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.7-1 | v1.31.7-6 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | cb4f333 | d1545bd | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.11 | v2.10.12 | New version contains updates and security fixes. |
| Konnectivity agent and server | v0.31.1 | v0.31.3 | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.31.3){: external}. |
| Kubernetes DNS autoscaler | v1.8.9 | v1.9.0 | See the [Kubernetes DNS autoscaler release notes](https://github.com/kubernetes-sigs/cluster-proportional-autoscaler/releases/tag/v1.9.0){: external}. |
| Portieris admission controller | v0.13.25 | v0.13.26 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.26){: external}. |
| Tigera Operator | v1.34.5 | v1.34.8 | See the [Tigera Operator release notes](https://github.com/tigera/operator/releases/tag/v1.34.8){: external}. |
{: caption="Changes since version 1.31.7_1543" caption-side="bottom"}



### Worker node fix pack 1.31.7_1546, released 21 April 2025
{: #cl-boms-1317_1546_W}

The following table shows the components included in the worker node fix pack 1.31.7_1546. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-55-generic|Resolves the following CVEs: [CVE-2024-56406](https://nvd.nist.gov/vuln/detail/CVE-2024-56406){: external}, [CVE-2024-8176](https://nvd.nist.gov/vuln/detail/CVE-2024-8176){: external}, [CVE-2025-1153](https://nvd.nist.gov/vuln/detail/CVE-2025-1153){: external}, [CVE-2025-1176](https://nvd.nist.gov/vuln/detail/CVE-2025-1176){: external}, [CVE-2025-1178](https://nvd.nist.gov/vuln/detail/CVE-2025-1178){: external}, [CVE-2025-1181](https://nvd.nist.gov/vuln/detail/CVE-2025-1181){: external}, [CVE-2025-1182](https://nvd.nist.gov/vuln/detail/CVE-2025-1182){: external}, [CVE-2025-1215](https://nvd.nist.gov/vuln/detail/CVE-2025-1215){: external}, [CVE-2025-26603](https://nvd.nist.gov/vuln/detail/CVE-2025-26603){: external}, and [CVE-2025-32464](https://nvd.nist.gov/vuln/detail/CVE-2025-32464){: external}.|
|UBUNTU_20_04|5.4.0-212-generic|Resolves the following CVEs: [CVE-2021-47119](https://nvd.nist.gov/vuln/detail/CVE-2021-47119){: external}, [CVE-2024-26915](https://nvd.nist.gov/vuln/detail/CVE-2024-26915){: external}, [CVE-2024-26928](https://nvd.nist.gov/vuln/detail/CVE-2024-26928){: external}, [CVE-2024-35864](https://nvd.nist.gov/vuln/detail/CVE-2024-35864){: external}, [CVE-2024-35958](https://nvd.nist.gov/vuln/detail/CVE-2024-35958){: external}, [CVE-2024-46826](https://nvd.nist.gov/vuln/detail/CVE-2024-46826){: external}, [CVE-2024-49974](https://nvd.nist.gov/vuln/detail/CVE-2024-49974){: external}, [CVE-2024-50256](https://nvd.nist.gov/vuln/detail/CVE-2024-50256){: external}, [CVE-2024-53237](https://nvd.nist.gov/vuln/detail/CVE-2024-53237){: external}, [CVE-2024-56651](https://nvd.nist.gov/vuln/detail/CVE-2024-56651){: external}, [CVE-2024-56658](https://nvd.nist.gov/vuln/detail/CVE-2024-56658){: external}, [CVE-2025-1153](https://nvd.nist.gov/vuln/detail/CVE-2025-1153){: external}, [CVE-2025-1176](https://nvd.nist.gov/vuln/detail/CVE-2025-1176){: external}, [CVE-2025-1182](https://nvd.nist.gov/vuln/detail/CVE-2025-1182){: external}, [CVE-2025-21700](https://nvd.nist.gov/vuln/detail/CVE-2025-21700){: external}, [CVE-2025-21702](https://nvd.nist.gov/vuln/detail/CVE-2025-21702){: external}, [CVE-2025-21703](https://nvd.nist.gov/vuln/detail/CVE-2025-21703){: external}, [CVE-2025-26603](https://nvd.nist.gov/vuln/detail/CVE-2025-26603){: external}, [CVE-2025-2784](https://nvd.nist.gov/vuln/detail/CVE-2025-2784){: external}, [CVE-2025-32050](https://nvd.nist.gov/vuln/detail/CVE-2025-32050){: external}, [CVE-2025-32052](https://nvd.nist.gov/vuln/detail/CVE-2025-32052){: external}, and [CVE-2025-32053](https://nvd.nist.gov/vuln/detail/CVE-2025-32053){: external}.|
|Kubernetes|1.31.7|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.7).|
|containerd|1.7.27|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.27) and the [security bulletin for CVE-2024-40635](https://www.ibm.com/support/pages/node/7229615).|
|HAProxy|bb0015364d95e0a2e7ab83d4a659d1541cee183e|Resolves the following CVEs: [CVE-2025-0395](https://nvd.nist.gov/vuln/detail/CVE-2025-0395){: external}, and [CVE-2024-8176](https://nvd.nist.gov/vuln/detail/CVE-2024-8176){: external}.|
|GPU Device Plug-in and Installer|b7d507fd50989efa6ba8a9595d2a5681fc2380bf|Resolves the following CVEs: [CVE-2024-8176](https://nvd.nist.gov/vuln/detail/CVE-2024-8176){: external}, and [CVE-2025-0395](https://nvd.nist.gov/vuln/detail/CVE-2025-0395){: external}.|
{: caption="1.31.7_1546 fix pack." caption-side="bottom"}
{: #cl-boms-1317_1546_W-component-table}



### Worker node fix pack 1.31.7_1545, released 08 April 2025
{: #cl-boms-1317_1545_W}

The following table shows the components included in the worker node fix pack 1.31.7_1545. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-55-generic|Resolves the following CVEs: [CVE-2024-25260](https://nvd.nist.gov/vuln/detail/CVE-2024-25260){: external}, [CVE-2025-1365](https://nvd.nist.gov/vuln/detail/CVE-2025-1365){: external}, [CVE-2025-1371](https://nvd.nist.gov/vuln/detail/CVE-2025-1371){: external}, [CVE-2025-1372](https://nvd.nist.gov/vuln/detail/CVE-2025-1372){: external}, [CVE-2025-1377](https://nvd.nist.gov/vuln/detail/CVE-2025-1377){: external}, [CVE-2025-24014](https://nvd.nist.gov/vuln/detail/CVE-2025-24014){: external}, [CVE-2025-30258](https://nvd.nist.gov/vuln/detail/CVE-2025-30258){: external}, and [CVE-2025-31115](https://nvd.nist.gov/vuln/detail/CVE-2025-31115){: external}.|
|UBUNTU_20_04|5.4.0-212-generic|Resolves the following CVEs: [cve-2018-5803](https://nvd.nist.gov/vuln/detail/cve-2018-5803){: external}, [CVE-2021-47219](https://nvd.nist.gov/vuln/detail/CVE-2021-47219){: external}, [CVE-2024-23848](https://nvd.nist.gov/vuln/detail/CVE-2024-23848){: external}, [CVE-2024-26928](https://nvd.nist.gov/vuln/detail/CVE-2024-26928){: external}, [CVE-2024-35864](https://nvd.nist.gov/vuln/detail/CVE-2024-35864){: external}, [CVE-2024-38588](https://nvd.nist.gov/vuln/detail/CVE-2024-38588){: external}, [CVE-2024-43900](https://nvd.nist.gov/vuln/detail/CVE-2024-43900){: external}, [CVE-2024-44938](https://nvd.nist.gov/vuln/detail/CVE-2024-44938){: external}, [CVE-2024-49925](https://nvd.nist.gov/vuln/detail/CVE-2024-49925){: external}, [CVE-2024-56614](https://nvd.nist.gov/vuln/detail/CVE-2024-56614){: external}, [CVE-2024-56658](https://nvd.nist.gov/vuln/detail/CVE-2024-56658){: external}, [CVE-2025-0938](https://nvd.nist.gov/vuln/detail/CVE-2025-0938){: external}, and [CVE-2025-30258](https://nvd.nist.gov/vuln/detail/CVE-2025-30258){: external}.|
|Kubernetes|1.31.7|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.7).|
|containerd|1.7.27|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.27) and the [security bulletin for CVE-2024-40635](https://www.ibm.com/support/pages/node/7229615).|
|HAProxy|997a4ab1e89a5c8ccf3a6823785d7ab5e34b0c83|N/A|
|GPU Device Plug-in and Installer|c9d9c47b1404651b3a3c022f288a6d90bb5a44b2|N/A|
{: caption="1.31.7_1545 fix pack." caption-side="bottom"}
{: #cl-boms-1317_1545_W-component-table}



### Master fix pack 1.31.7_1543, released 26 March 2025
{: #1317_1543_M}

The following table shows the changes that are in the master fix pack 1.31.7_1543. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.6.4 | v1.6.7 | New version contains updates and security fixes. |
| etcd | v3.5.17 | v3.5.18 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.18){: external}. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.5-3 | v1.31.7-1 | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.10 | v2.10.11 | New version contains updates and security fixes. |
| Kubernetes | v1.31.5 | v1.31.7 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.7){: external}. |
| Kubernetes NodeLocal DNS cache | 1.24.0 | 1.25.0 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.25.0){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 3178 | 3232 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.23 | v0.13.25 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.25){: external}. |
{: caption="Changes since version 1.31.5_1540" caption-side="bottom"}



### Worker node fix pack 1.31.7_1544, released 24 March 2025
{: #cl-boms-1317_1544_W}

The following table shows the components included in the worker node fix pack 1.31.7_1544. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-55-generic|Resolves the following CVEs: [CVE-2024-55549](https://nvd.nist.gov/vuln/detail/CVE-2024-55549){: external}, [CVE-2025-24855](https://nvd.nist.gov/vuln/detail/CVE-2025-24855){: external}, and [CVE-2025-27516](https://nvd.nist.gov/vuln/detail/CVE-2025-27516){: external}.|
|UBUNTU_20_04|5.4.0-208-generic|Resolves the following CVEs: [CVE-2024-55549](https://nvd.nist.gov/vuln/detail/CVE-2024-55549){: external}, [CVE-2024-9287](https://nvd.nist.gov/vuln/detail/CVE-2024-9287){: external}, [CVE-2025-0938](https://nvd.nist.gov/vuln/detail/CVE-2025-0938){: external}, [CVE-2025-24855](https://nvd.nist.gov/vuln/detail/CVE-2025-24855){: external}, [CVE-2025-27363](https://nvd.nist.gov/vuln/detail/CVE-2025-27363){: external}, and [CVE-2025-27516](https://nvd.nist.gov/vuln/detail/CVE-2025-27516){: external}.|
|Kubernetes|1.31.7|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.7).|
|containerd|1.7.27|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.27) and the [security bulletin for CVE-2024-40635](https://www.ibm.com/support/pages/node/7229615).|
|HAProxy|997a4ab1e89a5c8ccf3a6823785d7ab5e34b0c83|Resolves the following CVEs: [CVE-2024-56171](https://nvd.nist.gov/vuln/detail/CVE-2024-56171){: external}, [CVE-2025-24528](https://nvd.nist.gov/vuln/detail/CVE-2025-24528){: external}, and [CVE-2025-24928](https://nvd.nist.gov/vuln/detail/CVE-2025-24928){: external}.|
|GPU Device Plug-in and Installer|c9d9c47b1404651b3a3c022f288a6d90bb5a44b2|Resolves the following CVEs: [CVE-2024-56171](https://nvd.nist.gov/vuln/detail/CVE-2024-56171){: external}, [CVE-2025-24928](https://nvd.nist.gov/vuln/detail/CVE-2025-24928){: external}, and [CVE-2025-24528](https://nvd.nist.gov/vuln/detail/CVE-2025-24528){: external}.|
{: caption="1.31.7_1544 fix pack." caption-side="bottom"}
{: #cl-boms-1317_1544_W-component-table}



### Worker node fix pack 1.31.5_1542, released 11 March 2025
{: #cl-boms-1315_1542_W}

The following table shows the components included in the worker node fix pack 1.31.5_1542. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-52-generic|N/A|
|UBUNTU_20_04|5.4.0-208-generic|Resolves the following CVEs: [CVE-2021-47469](https://nvd.nist.gov/vuln/detail/CVE-2021-47469){: external}, [CVE-2023-52458](https://nvd.nist.gov/vuln/detail/CVE-2023-52458){: external}, [CVE-2023-52917](https://nvd.nist.gov/vuln/detail/CVE-2023-52917){: external}, [CVE-2024-12243](https://nvd.nist.gov/vuln/detail/CVE-2024-12243){: external}, [CVE-2024-13176](https://nvd.nist.gov/vuln/detail/CVE-2024-13176){: external}, [CVE-2024-26458](https://nvd.nist.gov/vuln/detail/CVE-2024-26458){: external}, [CVE-2024-26461](https://nvd.nist.gov/vuln/detail/CVE-2024-26461){: external}, [CVE-2024-35887](https://nvd.nist.gov/vuln/detail/CVE-2024-35887){: external}, [CVE-2024-35896](https://nvd.nist.gov/vuln/detail/CVE-2024-35896){: external}, [CVE-2024-38544](https://nvd.nist.gov/vuln/detail/CVE-2024-38544){: external}, [CVE-2024-38588](https://nvd.nist.gov/vuln/detail/CVE-2024-38588){: external}, [CVE-2024-40911](https://nvd.nist.gov/vuln/detail/CVE-2024-40911){: external}, [CVE-2024-40953](https://nvd.nist.gov/vuln/detail/CVE-2024-40953){: external}, [CVE-2024-40965](https://nvd.nist.gov/vuln/detail/CVE-2024-40965){: external}, [CVE-2024-40982](https://nvd.nist.gov/vuln/detail/CVE-2024-40982){: external}, [CVE-2024-41016](https://nvd.nist.gov/vuln/detail/CVE-2024-41016){: external}, [CVE-2024-41066](https://nvd.nist.gov/vuln/detail/CVE-2024-41066){: external}, [CVE-2024-42252](https://nvd.nist.gov/vuln/detail/CVE-2024-42252){: external}, [CVE-2024-43863](https://nvd.nist.gov/vuln/detail/CVE-2024-43863){: external}, [CVE-2024-44931](https://nvd.nist.gov/vuln/detail/CVE-2024-44931){: external}, [CVE-2024-46731](https://nvd.nist.gov/vuln/detail/CVE-2024-46731){: external}, [CVE-2024-46849](https://nvd.nist.gov/vuln/detail/CVE-2024-46849){: external}, [CVE-2024-46853](https://nvd.nist.gov/vuln/detail/CVE-2024-46853){: external}, [CVE-2024-46854](https://nvd.nist.gov/vuln/detail/CVE-2024-46854){: external}, [CVE-2024-47670](https://nvd.nist.gov/vuln/detail/CVE-2024-47670){: external}, [CVE-2024-47671](https://nvd.nist.gov/vuln/detail/CVE-2024-47671){: external}, [CVE-2024-47672](https://nvd.nist.gov/vuln/detail/CVE-2024-47672){: external}, [CVE-2024-47674](https://nvd.nist.gov/vuln/detail/CVE-2024-47674){: external}, [CVE-2024-47679](https://nvd.nist.gov/vuln/detail/CVE-2024-47679){: external}, [CVE-2024-47684](https://nvd.nist.gov/vuln/detail/CVE-2024-47684){: external}, [CVE-2024-47685](https://nvd.nist.gov/vuln/detail/CVE-2024-47685){: external}, [CVE-2024-47692](https://nvd.nist.gov/vuln/detail/CVE-2024-47692){: external}, [CVE-2024-47696](https://nvd.nist.gov/vuln/detail/CVE-2024-47696){: external}, [CVE-2024-47697](https://nvd.nist.gov/vuln/detail/CVE-2024-47697){: external}, [CVE-2024-47698](https://nvd.nist.gov/vuln/detail/CVE-2024-47698){: external}, [CVE-2024-47699](https://nvd.nist.gov/vuln/detail/CVE-2024-47699){: external}, [CVE-2024-47701](https://nvd.nist.gov/vuln/detail/CVE-2024-47701){: external}, [CVE-2024-47706](https://nvd.nist.gov/vuln/detail/CVE-2024-47706){: external}, [CVE-2024-47709](https://nvd.nist.gov/vuln/detail/CVE-2024-47709){: external}, [CVE-2024-47710](https://nvd.nist.gov/vuln/detail/CVE-2024-47710){: external}, [CVE-2024-47712](https://nvd.nist.gov/vuln/detail/CVE-2024-47712){: external}, [CVE-2024-47713](https://nvd.nist.gov/vuln/detail/CVE-2024-47713){: external}, [CVE-2024-47723](https://nvd.nist.gov/vuln/detail/CVE-2024-47723){: external}, [CVE-2024-47737](https://nvd.nist.gov/vuln/detail/CVE-2024-47737){: external}, [CVE-2024-47740](https://nvd.nist.gov/vuln/detail/CVE-2024-47740){: external}, [CVE-2024-47742](https://nvd.nist.gov/vuln/detail/CVE-2024-47742){: external}, [CVE-2024-47747](https://nvd.nist.gov/vuln/detail/CVE-2024-47747){: external}, [CVE-2024-47749](https://nvd.nist.gov/vuln/detail/CVE-2024-47749){: external}, [CVE-2024-47756](https://nvd.nist.gov/vuln/detail/CVE-2024-47756){: external}, [CVE-2024-47757](https://nvd.nist.gov/vuln/detail/CVE-2024-47757){: external}, [CVE-2024-49851](https://nvd.nist.gov/vuln/detail/CVE-2024-49851){: external}, [CVE-2024-49860](https://nvd.nist.gov/vuln/detail/CVE-2024-49860){: external}, [CVE-2024-49867](https://nvd.nist.gov/vuln/detail/CVE-2024-49867){: external}, [CVE-2024-49868](https://nvd.nist.gov/vuln/detail/CVE-2024-49868){: external}, [CVE-2024-49877](https://nvd.nist.gov/vuln/detail/CVE-2024-49877){: external}, [CVE-2024-49878](https://nvd.nist.gov/vuln/detail/CVE-2024-49878){: external}, [CVE-2024-49879](https://nvd.nist.gov/vuln/detail/CVE-2024-49879){: external}, [CVE-2024-49882](https://nvd.nist.gov/vuln/detail/CVE-2024-49882){: external}, [CVE-2024-49883](https://nvd.nist.gov/vuln/detail/CVE-2024-49883){: external}, [CVE-2024-49892](https://nvd.nist.gov/vuln/detail/CVE-2024-49892){: external}, [CVE-2024-49894](https://nvd.nist.gov/vuln/detail/CVE-2024-49894){: external}, [CVE-2024-49896](https://nvd.nist.gov/vuln/detail/CVE-2024-49896){: external}, [CVE-2024-49900](https://nvd.nist.gov/vuln/detail/CVE-2024-49900){: external}, [CVE-2024-49902](https://nvd.nist.gov/vuln/detail/CVE-2024-49902){: external}, [CVE-2024-49903](https://nvd.nist.gov/vuln/detail/CVE-2024-49903){: external}, [CVE-2024-49924](https://nvd.nist.gov/vuln/detail/CVE-2024-49924){: external}, [CVE-2024-49938](https://nvd.nist.gov/vuln/detail/CVE-2024-49938){: external}, [CVE-2024-49944](https://nvd.nist.gov/vuln/detail/CVE-2024-49944){: external}, [CVE-2024-49948](https://nvd.nist.gov/vuln/detail/CVE-2024-49948){: external}, [CVE-2024-49949](https://nvd.nist.gov/vuln/detail/CVE-2024-49949){: external}, [CVE-2024-49952](https://nvd.nist.gov/vuln/detail/CVE-2024-49952){: external}, [CVE-2024-49955](https://nvd.nist.gov/vuln/detail/CVE-2024-49955){: external}, [CVE-2024-49957](https://nvd.nist.gov/vuln/detail/CVE-2024-49957){: external}, [CVE-2024-49958](https://nvd.nist.gov/vuln/detail/CVE-2024-49958){: external}, [CVE-2024-49959](https://nvd.nist.gov/vuln/detail/CVE-2024-49959){: external}, [CVE-2024-49962](https://nvd.nist.gov/vuln/detail/CVE-2024-49962){: external}, [CVE-2024-49963](https://nvd.nist.gov/vuln/detail/CVE-2024-49963){: external}, [CVE-2024-49965](https://nvd.nist.gov/vuln/detail/CVE-2024-49965){: external}, [CVE-2024-49966](https://nvd.nist.gov/vuln/detail/CVE-2024-49966){: external}, [CVE-2024-49973](https://nvd.nist.gov/vuln/detail/CVE-2024-49973){: external}, [CVE-2024-49975](https://nvd.nist.gov/vuln/detail/CVE-2024-49975){: external}, [CVE-2024-49981](https://nvd.nist.gov/vuln/detail/CVE-2024-49981){: external}, [CVE-2024-49982](https://nvd.nist.gov/vuln/detail/CVE-2024-49982){: external}, [CVE-2024-49985](https://nvd.nist.gov/vuln/detail/CVE-2024-49985){: external}, [CVE-2024-49995](https://nvd.nist.gov/vuln/detail/CVE-2024-49995){: external}, [CVE-2024-49997](https://nvd.nist.gov/vuln/detail/CVE-2024-49997){: external}, [CVE-2024-50006](https://nvd.nist.gov/vuln/detail/CVE-2024-50006){: external}, [CVE-2024-50007](https://nvd.nist.gov/vuln/detail/CVE-2024-50007){: external}, [CVE-2024-50008](https://nvd.nist.gov/vuln/detail/CVE-2024-50008){: external}, [CVE-2024-50024](https://nvd.nist.gov/vuln/detail/CVE-2024-50024){: external}, [CVE-2024-50033](https://nvd.nist.gov/vuln/detail/CVE-2024-50033){: external}, [CVE-2024-50035](https://nvd.nist.gov/vuln/detail/CVE-2024-50035){: external}, [CVE-2024-50039](https://nvd.nist.gov/vuln/detail/CVE-2024-50039){: external}, [CVE-2024-50040](https://nvd.nist.gov/vuln/detail/CVE-2024-50040){: external}, [CVE-2024-50044](https://nvd.nist.gov/vuln/detail/CVE-2024-50044){: external}, [CVE-2024-50045](https://nvd.nist.gov/vuln/detail/CVE-2024-50045){: external}, [CVE-2024-50059](https://nvd.nist.gov/vuln/detail/CVE-2024-50059){: external}, [CVE-2024-50074](https://nvd.nist.gov/vuln/detail/CVE-2024-50074){: external}, [CVE-2024-50082](https://nvd.nist.gov/vuln/detail/CVE-2024-50082){: external}, [CVE-2024-50089](https://nvd.nist.gov/vuln/detail/CVE-2024-50089){: external}, [CVE-2024-50096](https://nvd.nist.gov/vuln/detail/CVE-2024-50096){: external}, [CVE-2024-50099](https://nvd.nist.gov/vuln/detail/CVE-2024-50099){: external}, [CVE-2024-50116](https://nvd.nist.gov/vuln/detail/CVE-2024-50116){: external}, [CVE-2024-50117](https://nvd.nist.gov/vuln/detail/CVE-2024-50117){: external}, [CVE-2024-50127](https://nvd.nist.gov/vuln/detail/CVE-2024-50127){: external}, [CVE-2024-50131](https://nvd.nist.gov/vuln/detail/CVE-2024-50131){: external}, [CVE-2024-50134](https://nvd.nist.gov/vuln/detail/CVE-2024-50134){: external}, [CVE-2024-50142](https://nvd.nist.gov/vuln/detail/CVE-2024-50142){: external}, [CVE-2024-50143](https://nvd.nist.gov/vuln/detail/CVE-2024-50143){: external}, [CVE-2024-50148](https://nvd.nist.gov/vuln/detail/CVE-2024-50148){: external}, [CVE-2024-50150](https://nvd.nist.gov/vuln/detail/CVE-2024-50150){: external}, [CVE-2024-50151](https://nvd.nist.gov/vuln/detail/CVE-2024-50151){: external}, [CVE-2024-50167](https://nvd.nist.gov/vuln/detail/CVE-2024-50167){: external}, [CVE-2024-50168](https://nvd.nist.gov/vuln/detail/CVE-2024-50168){: external}, [CVE-2024-50171](https://nvd.nist.gov/vuln/detail/CVE-2024-50171){: external}, [CVE-2024-50179](https://nvd.nist.gov/vuln/detail/CVE-2024-50179){: external}, [CVE-2024-50180](https://nvd.nist.gov/vuln/detail/CVE-2024-50180){: external}, [CVE-2024-50184](https://nvd.nist.gov/vuln/detail/CVE-2024-50184){: external}, [CVE-2024-50194](https://nvd.nist.gov/vuln/detail/CVE-2024-50194){: external}, [CVE-2024-50195](https://nvd.nist.gov/vuln/detail/CVE-2024-50195){: external}, [CVE-2024-50199](https://nvd.nist.gov/vuln/detail/CVE-2024-50199){: external}, [CVE-2024-50202](https://nvd.nist.gov/vuln/detail/CVE-2024-50202){: external}, [CVE-2024-50205](https://nvd.nist.gov/vuln/detail/CVE-2024-50205){: external}, [CVE-2024-50218](https://nvd.nist.gov/vuln/detail/CVE-2024-50218){: external}, [CVE-2024-50228](https://nvd.nist.gov/vuln/detail/CVE-2024-50228){: external}, [CVE-2024-50229](https://nvd.nist.gov/vuln/detail/CVE-2024-50229){: external}, [CVE-2024-50230](https://nvd.nist.gov/vuln/detail/CVE-2024-50230){: external}, [CVE-2024-50233](https://nvd.nist.gov/vuln/detail/CVE-2024-50233){: external}, [CVE-2024-50234](https://nvd.nist.gov/vuln/detail/CVE-2024-50234){: external}, [CVE-2024-50236](https://nvd.nist.gov/vuln/detail/CVE-2024-50236){: external}, [CVE-2024-50237](https://nvd.nist.gov/vuln/detail/CVE-2024-50237){: external}, [CVE-2024-50251](https://nvd.nist.gov/vuln/detail/CVE-2024-50251){: external}, [CVE-2024-50262](https://nvd.nist.gov/vuln/detail/CVE-2024-50262){: external}, [CVE-2024-50265](https://nvd.nist.gov/vuln/detail/CVE-2024-50265){: external}, [CVE-2024-50267](https://nvd.nist.gov/vuln/detail/CVE-2024-50267){: external}, [CVE-2024-50269](https://nvd.nist.gov/vuln/detail/CVE-2024-50269){: external}, [CVE-2024-50273](https://nvd.nist.gov/vuln/detail/CVE-2024-50273){: external}, [CVE-2024-50278](https://nvd.nist.gov/vuln/detail/CVE-2024-50278){: external}, [CVE-2024-50279](https://nvd.nist.gov/vuln/detail/CVE-2024-50279){: external}, [CVE-2024-50282](https://nvd.nist.gov/vuln/detail/CVE-2024-50282){: external}, [CVE-2024-50287](https://nvd.nist.gov/vuln/detail/CVE-2024-50287){: external}, [CVE-2024-50290](https://nvd.nist.gov/vuln/detail/CVE-2024-50290){: external}, [CVE-2024-50296](https://nvd.nist.gov/vuln/detail/CVE-2024-50296){: external}, [CVE-2024-50299](https://nvd.nist.gov/vuln/detail/CVE-2024-50299){: external}, [CVE-2024-50301](https://nvd.nist.gov/vuln/detail/CVE-2024-50301){: external}, [CVE-2024-50302](https://nvd.nist.gov/vuln/detail/CVE-2024-50302){: external}, [CVE-2024-50349](https://nvd.nist.gov/vuln/detail/CVE-2024-50349){: external}, [CVE-2024-52006](https://nvd.nist.gov/vuln/detail/CVE-2024-52006){: external}, [CVE-2024-53059](https://nvd.nist.gov/vuln/detail/CVE-2024-53059){: external}, [CVE-2024-53061](https://nvd.nist.gov/vuln/detail/CVE-2024-53061){: external}, [CVE-2024-53063](https://nvd.nist.gov/vuln/detail/CVE-2024-53063){: external}, [CVE-2024-53066](https://nvd.nist.gov/vuln/detail/CVE-2024-53066){: external}, [CVE-2024-56171](https://nvd.nist.gov/vuln/detail/CVE-2024-56171){: external}, [CVE-2024-9143](https://nvd.nist.gov/vuln/detail/CVE-2024-9143){: external}, [CVE-2025-0840](https://nvd.nist.gov/vuln/detail/CVE-2025-0840){: external}, [CVE-2025-0927](https://nvd.nist.gov/vuln/detail/CVE-2025-0927){: external}, [CVE-2025-0938](https://nvd.nist.gov/vuln/detail/CVE-2025-0938){: external}, [CVE-2025-1390](https://nvd.nist.gov/vuln/detail/CVE-2025-1390){: external}, [CVE-2025-24528](https://nvd.nist.gov/vuln/detail/CVE-2025-24528){: external}, [CVE-2025-24928](https://nvd.nist.gov/vuln/detail/CVE-2025-24928){: external}, and [CVE-2025-27113](https://nvd.nist.gov/vuln/detail/CVE-2025-27113){: external}.|
|Kubernetes|1.31.5|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.5).|
|containerd|1.7.26|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.26).|
|HAProxy|1d72cc8c7d02da6ba0340191fa8d9a86550e5090|N/A|
|GPU Device Plug-in and Installer|57c31795f069cb17cd235792f3ac21ac0e086360|Resolves the following CVEs: [CVE-2024-1488](https://nvd.nist.gov/vuln/detail/CVE-2024-1488){: external}, [CVE-2020-11023](https://nvd.nist.gov/vuln/detail/CVE-2020-11023){: external}, [CVE-2024-8508](https://nvd.nist.gov/vuln/detail/CVE-2024-8508){: external}, and [CVE-2022-49043](https://nvd.nist.gov/vuln/detail/CVE-2022-49043){: external}.|
{: caption="1.31.5_1542 fix pack." caption-side="bottom"}
{: #cl-boms-1315_1542_W-component-table}



### Worker node fix pack 1.31.5_1541, released 24 February 2025
{: #cl-boms-1315_1541_W}

The following table shows the components included in the worker node fix pack 1.31.5_1541. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-52-generic|Resolves the following CVEs: [CVE-2024-12133](https://nvd.nist.gov/vuln/detail/CVE-2024-12133){: external}, [CVE-2024-12243](https://nvd.nist.gov/vuln/detail/CVE-2024-12243){: external}, [CVE-2024-13176](https://nvd.nist.gov/vuln/detail/CVE-2024-13176){: external}, [CVE-2024-9143](https://nvd.nist.gov/vuln/detail/CVE-2024-9143){: external}, [CVE-2025-0938](https://nvd.nist.gov/vuln/detail/CVE-2025-0938){: external}, [CVE-2025-26465](https://nvd.nist.gov/vuln/detail/CVE-2025-26465){: external}, and [CVE-2025-26466](https://nvd.nist.gov/vuln/detail/CVE-2025-26466){: external}.|
|UBUNTU_20_04|5.4.0-205-generic|Resolves the following CVEs: [CVE-2024-12133](https://nvd.nist.gov/vuln/detail/CVE-2024-12133){: external}, [CVE-2024-12243](https://nvd.nist.gov/vuln/detail/CVE-2024-12243){: external}, [CVE-2024-13176](https://nvd.nist.gov/vuln/detail/CVE-2024-13176){: external}, [CVE-2024-9143](https://nvd.nist.gov/vuln/detail/CVE-2024-9143){: external}, [CVE-2025-0938](https://nvd.nist.gov/vuln/detail/CVE-2025-0938){: external}, [CVE-2025-24014](https://nvd.nist.gov/vuln/detail/CVE-2025-24014){: external}, and [CVE-2025-26465](https://nvd.nist.gov/vuln/detail/CVE-2025-26465){: external}.|
|Kubernetes|1.31.5|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.5).|
|containerd|1.7.25|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.25).|
|HAProxy|1d72cc8c7d02da6ba0340191fa8d9a86550e5090|Resolves the following CVEs: [CVE-2020-11023](https://nvd.nist.gov/vuln/detail/CVE-2020-11023){: external}, and [CVE-2022-49043](https://nvd.nist.gov/vuln/detail/CVE-2022-49043){: external}.|
|GPU Device Plug-in and Installer|e41a0d57a0f7696dfa3698c6af3bcc8765e76cfd|Resolves the following CVEs: [CVE-2024-8508](https://nvd.nist.gov/vuln/detail/CVE-2024-8508){: external}, [CVE-2022-49043](https://nvd.nist.gov/vuln/detail/CVE-2022-49043){: external}, [CVE-2024-1488](https://nvd.nist.gov/vuln/detail/CVE-2024-1488){: external}, and [CVE-2020-11023](https://nvd.nist.gov/vuln/detail/CVE-2020-11023){: external}.|
{: caption="1.31.5_1541 fix pack." caption-side="bottom"}
{: #cl-boms-1315_1541_W-component-table}



### Master fix pack 1.31.5_1540, released 19 February 2025
{: #1315_1540_M}

The following table shows the changes that are in the master fix pack 1.31.5_1540. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.4-3 | v1.31.5-3 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} for Classic plug-in and monitor | 447 | 449 | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.9 | v2.10.10 | New version contains updates and security fixes. |
| Kubernetes NodeLocal DNS cache | 1.23.1 | 1.24.0 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.24.0){: external}. |
{: caption="Changes since version 1.31.5_1537" caption-side="bottom"}



### Worker node fix pack 1.31.5_1539, released 11 February 2025
{: #cl-boms-1315_1539_W}

The following table shows the components included in the worker node fix pack 1.31.5_1539. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-52-generic|Resolves the following CVEs: [CVE-2022-49043](https://nvd.nist.gov/vuln/detail/CVE-2022-49043){: external}, [CVE-2024-11187](https://nvd.nist.gov/vuln/detail/CVE-2024-11187){: external}, [CVE-2024-12705](https://nvd.nist.gov/vuln/detail/CVE-2024-12705){: external}, [CVE-2024-34459](https://nvd.nist.gov/vuln/detail/CVE-2024-34459){: external}, [CVE-2024-3596](https://nvd.nist.gov/vuln/detail/CVE-2024-3596){: external}, [CVE-2024-53103](https://nvd.nist.gov/vuln/detail/CVE-2024-53103){: external}, [CVE-2024-53141](https://nvd.nist.gov/vuln/detail/CVE-2024-53141){: external}, [CVE-2024-53164](https://nvd.nist.gov/vuln/detail/CVE-2024-53164){: external}, [CVE-2024-56201](https://nvd.nist.gov/vuln/detail/CVE-2024-56201){: external}, [CVE-2024-56201](https://nvd.nist.gov/vuln/detail/CVE-2024-56201){: external}, [CVE-2024-56326](https://nvd.nist.gov/vuln/detail/CVE-2024-56326){: external}, [CVE-2024-56326](https://nvd.nist.gov/vuln/detail/CVE-2024-56326){: external}, and [CVE-2025-0395](https://nvd.nist.gov/vuln/detail/CVE-2025-0395){: external}.|
|UBUNTU_20_04|5.4.0-205-generic|Resolves the following CVEs: [CVE-2022-49043](https://nvd.nist.gov/vuln/detail/CVE-2022-49043){: external}, [CVE-2023-21400](https://nvd.nist.gov/vuln/detail/CVE-2023-21400){: external}, [CVE-2024-11187](https://nvd.nist.gov/vuln/detail/CVE-2024-11187){: external}, [CVE-2024-12705](https://nvd.nist.gov/vuln/detail/CVE-2024-12705){: external}, [CVE-2024-34459](https://nvd.nist.gov/vuln/detail/CVE-2024-34459){: external}, [CVE-2024-3596](https://nvd.nist.gov/vuln/detail/CVE-2024-3596){: external}, [CVE-2024-40967](https://nvd.nist.gov/vuln/detail/CVE-2024-40967){: external}, [CVE-2024-53103](https://nvd.nist.gov/vuln/detail/CVE-2024-53103){: external}, [CVE-2024-53141](https://nvd.nist.gov/vuln/detail/CVE-2024-53141){: external}, [CVE-2024-53164](https://nvd.nist.gov/vuln/detail/CVE-2024-53164){: external}, [CVE-2024-56201](https://nvd.nist.gov/vuln/detail/CVE-2024-56201){: external}, [CVE-2024-56201](https://nvd.nist.gov/vuln/detail/CVE-2024-56201){: external}, [CVE-2024-56326](https://nvd.nist.gov/vuln/detail/CVE-2024-56326){: external}, [CVE-2024-56326](https://nvd.nist.gov/vuln/detail/CVE-2024-56326){: external}, and [CVE-2025-0395](https://nvd.nist.gov/vuln/detail/CVE-2025-0395){: external}.|
|Kubernetes|1.31.5|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.5).|
|containerd|1.7.25|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.25).|
|HAProxy|03d1ee01e9241d0e5ec93b9eb8986feb2771a01a|Resolves the following CVEs: [CVE-2019-12900](https://nvd.nist.gov/vuln/detail/CVE-2019-12900){: external}.|
|GPU Device Plug-in and Installer|639e505cf0c0f21d6a0a09d157ac7be7f16a77c8|Resolves the following CVEs: [CVE-2024-1488](https://nvd.nist.gov/vuln/detail/CVE-2024-1488){: external}, and [CVE-2024-8508](https://nvd.nist.gov/vuln/detail/CVE-2024-8508){: external}.|
{: caption="1.31.5_1539 fix pack." caption-side="bottom"}
{: #cl-boms-1315_1539_W-component-table}



### Worker node fix pack 1.31.5_1538, released 29 January 2025
{: #cl-boms-1315_1538_W}

The following table shows the components included in the worker node fix pack 1.31.5_1538. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_20_04|5.4.0-204-generic|Resolves the following CVEs: [CVE-2024-11168](https://nvd.nist.gov/vuln/detail/CVE-2024-11168){: external}, and [CVE-2025-22134](https://nvd.nist.gov/vuln/detail/CVE-2025-22134){: external}.|
|UBUNTU_24_04|6.8.0-51-generic|Resolves the following CVEs: [CVE-2024-12254](https://nvd.nist.gov/vuln/detail/CVE-2024-12254){: external}, [CVE-2024-50349](https://nvd.nist.gov/vuln/detail/CVE-2024-50349){: external}, [CVE-2024-52006](https://nvd.nist.gov/vuln/detail/CVE-2024-52006){: external}, and [CVE-2025-22134](https://nvd.nist.gov/vuln/detail/CVE-2025-22134){: external}.|
|Kubernetes|1.31.5|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.5).|
|containerd|1.7.25|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.25).|
|HAProxy|14daa781a66ca5ed5754656ce53c3cca4af580b5|N/A|
|GPU Device Plug-in and Installer|6563a84c30f22dd511f6e2d80227040a12c3af9a|Resolves the following CVEs: [CVE-2019-12900](https://nvd.nist.gov/vuln/detail/CVE-2019-12900){: external}.|
{: caption="1.31.5_1538 fix pack." caption-side="bottom"}
{: #cl-boms-1315_1538_W-component-table}



### Master fix pack 1.31.5_1537, released 22 January 2025
{: #1315_1537_M}

The following table shows the changes that are in the master fix pack 1.31.5_1537. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.6.3 | v1.6.4 | New version contains updates and security fixes. |
| CoreDNS | 1.11.3 | v1.11.4 | See the [CoreDNS release notes](https://coredns.io/tags/notes/){: external}. |
| etcd | v3.5.16 | v3.5.17 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.17){: external}. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.5.16 | v2.5.17 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.2-4 | v1.31.4-3 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 743ed58 | cb4f333 | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.8 | v2.10.9 | New version contains updates and security fixes. |
| Konnectivity agent and server | v0.30.3 | v0.31.1 | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.31.1){: external}. |
| Kubernetes | v1.31.3 | v1.31.5 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.5){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 3079 | 3178 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.21 | v0.13.23 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.23){: external}. |
{: caption="Changes since version 1.31.3_1530" caption-side="bottom"}



### Worker node fix pack 1.31.3_1535, released 13 January 2025
{: #cl-boms-1313_1535_W}

The following table shows the components included in the worker node fix pack 1.31.3_1535. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_20_04|5.4.0-204-generic|N/A|
|UBUNTU_24_04|6.8.0-51-generic|N/A|
|Kubernetes|1.31.3|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.3).|
|containerd|1.7.23|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.23).|
|HAProxy|14daa781a66ca5ed5754656ce53c3cca4af580b5|N/A|
|GPU Device Plug-in and Installer|dc0ff3ad7a22a45390d050aa7d3ab23968870a14|Resolves the following CVEs: [CVE-2024-35195](https://nvd.nist.gov/vuln/detail/CVE-2024-35195){: external}, [CVE-2024-53088](https://nvd.nist.gov/vuln/detail/CVE-2024-53088){: external}, and [CVE-2024-53122](https://nvd.nist.gov/vuln/detail/CVE-2024-53122){: external}.|
{: caption="1.31.3_1535 fix pack." caption-side="bottom"}
{: #cl-boms-1313_1535_W-component-table}



### Worker node fix pack 1.31.3_1534, released 30 December 2024
{: #1313_1534_W}

The following table shows the changes that are in the worker node fix pack 1.31.3_1534. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages | 5.4.0-202-generic | 5.4.0-204-generic | Worker node kernel & package updates for [CVE-2021-47001](https://nvd.nist.gov/vuln/detail/CVE-2021-47001){: external}, [CVE-2021-47101](https://nvd.nist.gov/vuln/detail/CVE-2021-47101){: external}, [CVE-2022-38096](https://nvd.nist.gov/vuln/detail/CVE-2022-38096){: external}, [CVE-2023-52821](https://nvd.nist.gov/vuln/detail/CVE-2023-52821){: external}, [CVE-2024-11053](https://nvd.nist.gov/vuln/detail/CVE-2024-11053){: external}, [CVE-2024-35963](https://nvd.nist.gov/vuln/detail/CVE-2024-35963){: external}, [CVE-2024-35965](https://nvd.nist.gov/vuln/detail/CVE-2024-35965){: external}, [CVE-2024-35966](https://nvd.nist.gov/vuln/detail/CVE-2024-35966){: external}, [CVE-2024-35967](https://nvd.nist.gov/vuln/detail/CVE-2024-35967){: external}, [CVE-2024-36952](https://nvd.nist.gov/vuln/detail/CVE-2024-36952){: external}, [CVE-2024-38553](https://nvd.nist.gov/vuln/detail/CVE-2024-38553){: external}, [CVE-2024-38597](https://nvd.nist.gov/vuln/detail/CVE-2024-38597){: external}, [CVE-2024-40910](https://nvd.nist.gov/vuln/detail/CVE-2024-40910){: external}, [CVE-2024-43892](https://nvd.nist.gov/vuln/detail/CVE-2024-43892){: external}, [CVE-2024-47606](https://nvd.nist.gov/vuln/detail/CVE-2024-47606){: external}, [CVE-2024-49967](https://nvd.nist.gov/vuln/detail/CVE-2024-49967){: external}, [CVE-2024-50264](https://nvd.nist.gov/vuln/detail/CVE-2024-50264){: external}, [CVE-2024-53057](https://nvd.nist.gov/vuln/detail/CVE-2024-53057){: external}. |
| Ubuntu 24.04 Packages | 6.8.0-50-generic | 6.8.0-51-generic | Worker node kernel & package updates for [CVE-2024-11053](https://nvd.nist.gov/vuln/detail/CVE-2024-11053){: external}, [CVE-2024-47606](https://nvd.nist.gov/vuln/detail/CVE-2024-47606){: external}, [CVE-2024-49967](https://nvd.nist.gov/vuln/detail/CVE-2024-49967){: external}, [CVE-2024-50264](https://nvd.nist.gov/vuln/detail/CVE-2024-50264){: external}, [CVE-2024-53057](https://nvd.nist.gov/vuln/detail/CVE-2024-53057){: external}. |
{: caption="Changes since version 1.31.3_1533" caption-side="bottom"}



### Worker node fix pack 1.31.3_1533, released 16 December 2024
{: #1313_1533_W}

The following table shows the changes that are in the worker node fix pack 1.31.3_1533. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages | 5.4.0-200-generic | 5.4.0-202-generic | Worker node kernel & package updates for [CVE-2021-47076](https://nvd.nist.gov/vuln/detail/CVE-2021-47076){: external}, [CVE-2021-47501](https://nvd.nist.gov/vuln/detail/CVE-2021-47501){: external}, [CVE-2022-48733](https://nvd.nist.gov/vuln/detail/CVE-2022-48733){: external}, [CVE-2022-48938](https://nvd.nist.gov/vuln/detail/CVE-2022-48938){: external}, [CVE-2022-48943](https://nvd.nist.gov/vuln/detail/CVE-2022-48943){: external}, [CVE-2023-52488](https://nvd.nist.gov/vuln/detail/CVE-2023-52488){: external}, [CVE-2023-52497](https://nvd.nist.gov/vuln/detail/CVE-2023-52497){: external}, [CVE-2023-52498](https://nvd.nist.gov/vuln/detail/CVE-2023-52498){: external}, [CVE-2023-52639](https://nvd.nist.gov/vuln/detail/CVE-2023-52639){: external}, [CVE-2024-26947](https://nvd.nist.gov/vuln/detail/CVE-2024-26947){: external}, [CVE-2024-35904](https://nvd.nist.gov/vuln/detail/CVE-2024-35904){: external}, [CVE-2024-35951](https://nvd.nist.gov/vuln/detail/CVE-2024-35951){: external}, [CVE-2024-36938](https://nvd.nist.gov/vuln/detail/CVE-2024-36938){: external}, [CVE-2024-36953](https://nvd.nist.gov/vuln/detail/CVE-2024-36953){: external}, [CVE-2024-36968](https://nvd.nist.gov/vuln/detail/CVE-2024-36968){: external}, [CVE-2024-38538](https://nvd.nist.gov/vuln/detail/CVE-2024-38538){: external}, [CVE-2024-42068](https://nvd.nist.gov/vuln/detail/CVE-2024-42068){: external}, [CVE-2024-42077](https://nvd.nist.gov/vuln/detail/CVE-2024-42077){: external}, [CVE-2024-42156](https://nvd.nist.gov/vuln/detail/CVE-2024-42156){: external}, [CVE-2024-42240](https://nvd.nist.gov/vuln/detail/CVE-2024-42240){: external}, [CVE-2024-44940](https://nvd.nist.gov/vuln/detail/CVE-2024-44940){: external}, [CVE-2024-44942](https://nvd.nist.gov/vuln/detail/CVE-2024-44942){: external}, [CVE-2024-46724](https://nvd.nist.gov/vuln/detail/CVE-2024-46724){: external}, [CVE-2024-47814](https://nvd.nist.gov/vuln/detail/CVE-2024-47814){: external}, [CVE-2024-50602](https://nvd.nist.gov/vuln/detail/CVE-2024-50602){: external}. |
| Ubuntu 24.04 Packages | 6.8.0-48-generic | 6.8.0-50-generic | Worker node kernel & package updates for [CVE-2024-42284](https://nvd.nist.gov/vuln/detail/CVE-2024-42284){: external}, [CVE-2024-42301](https://nvd.nist.gov/vuln/detail/CVE-2024-42301){: external}, [CVE-2024-44987](https://nvd.nist.gov/vuln/detail/CVE-2024-44987){: external}, [CVE-2024-44998](https://nvd.nist.gov/vuln/detail/CVE-2024-44998){: external}, [CVE-2024-46713](https://nvd.nist.gov/vuln/detail/CVE-2024-46713){: external}, [CVE-2024-46722](https://nvd.nist.gov/vuln/detail/CVE-2024-46722){: external}, [CVE-2024-46723](https://nvd.nist.gov/vuln/detail/CVE-2024-46723){: external}, [CVE-2024-46724](https://nvd.nist.gov/vuln/detail/CVE-2024-46724){: external}, [CVE-2024-46725](https://nvd.nist.gov/vuln/detail/CVE-2024-46725){: external}, [CVE-2024-46735](https://nvd.nist.gov/vuln/detail/CVE-2024-46735){: external}, [CVE-2024-46737](https://nvd.nist.gov/vuln/detail/CVE-2024-46737){: external}, [CVE-2024-46738](https://nvd.nist.gov/vuln/detail/CVE-2024-46738){: external}, [CVE-2024-46739](https://nvd.nist.gov/vuln/detail/CVE-2024-46739){: external}, [CVE-2024-46740](https://nvd.nist.gov/vuln/detail/CVE-2024-46740){: external}, [CVE-2024-46741](https://nvd.nist.gov/vuln/detail/CVE-2024-46741){: external}, [CVE-2024-46743](https://nvd.nist.gov/vuln/detail/CVE-2024-46743){: external}, [CVE-2024-46744](https://nvd.nist.gov/vuln/detail/CVE-2024-46744){: external}, [CVE-2024-46745](https://nvd.nist.gov/vuln/detail/CVE-2024-46745){: external}, [CVE-2024-46746](https://nvd.nist.gov/vuln/detail/CVE-2024-46746){: external}, [CVE-2024-46747](https://nvd.nist.gov/vuln/detail/CVE-2024-46747){: external}, [CVE-2024-46749](https://nvd.nist.gov/vuln/detail/CVE-2024-46749){: external}, [CVE-2024-46750](https://nvd.nist.gov/vuln/detail/CVE-2024-46750){: external}, [CVE-2024-46751](https://nvd.nist.gov/vuln/detail/CVE-2024-46751){: external}, [CVE-2024-46752](https://nvd.nist.gov/vuln/detail/CVE-2024-46752){: external}, [CVE-2024-46753](https://nvd.nist.gov/vuln/detail/CVE-2024-46753){: external}, [CVE-2024-46754](https://nvd.nist.gov/vuln/detail/CVE-2024-46754){: external}, [CVE-2024-46755](https://nvd.nist.gov/vuln/detail/CVE-2024-46755){: external}, [CVE-2024-46756](https://nvd.nist.gov/vuln/detail/CVE-2024-46756){: external}, [CVE-2024-46757](https://nvd.nist.gov/vuln/detail/CVE-2024-46757){: external}, [CVE-2024-46758](https://nvd.nist.gov/vuln/detail/CVE-2024-46758){: external}, [CVE-2024-46759](https://nvd.nist.gov/vuln/detail/CVE-2024-46759){: external}, [CVE-2024-46760](https://nvd.nist.gov/vuln/detail/CVE-2024-46760){: external}, [CVE-2024-46761](https://nvd.nist.gov/vuln/detail/CVE-2024-46761){: external}, [CVE-2024-46762](https://nvd.nist.gov/vuln/detail/CVE-2024-46762){: external}, [CVE-2024-46763](https://nvd.nist.gov/vuln/detail/CVE-2024-46763){: external}, [CVE-2024-46765](https://nvd.nist.gov/vuln/detail/CVE-2024-46765){: external}, [CVE-2024-46766](https://nvd.nist.gov/vuln/detail/CVE-2024-46766){: external}, [CVE-2024-46767](https://nvd.nist.gov/vuln/detail/CVE-2024-46767){: external}, [CVE-2024-46768](https://nvd.nist.gov/vuln/detail/CVE-2024-46768){: external}, [CVE-2024-46770](https://nvd.nist.gov/vuln/detail/CVE-2024-46770){: external}, [CVE-2024-46771](https://nvd.nist.gov/vuln/detail/CVE-2024-46771){: external}, [CVE-2024-46772](https://nvd.nist.gov/vuln/detail/CVE-2024-46772){: external}, [CVE-2024-46773](https://nvd.nist.gov/vuln/detail/CVE-2024-46773){: external}, [CVE-2024-46774](https://nvd.nist.gov/vuln/detail/CVE-2024-46774){: external}, [CVE-2024-46775](https://nvd.nist.gov/vuln/detail/CVE-2024-46775){: external}, [CVE-2024-46776](https://nvd.nist.gov/vuln/detail/CVE-2024-46776){: external}, [CVE-2024-46777](https://nvd.nist.gov/vuln/detail/CVE-2024-46777){: external}, [CVE-2024-46778](https://nvd.nist.gov/vuln/detail/CVE-2024-46778){: external}, [CVE-2024-46779](https://nvd.nist.gov/vuln/detail/CVE-2024-46779){: external}, [CVE-2024-46780](https://nvd.nist.gov/vuln/detail/CVE-2024-46780){: external}, [CVE-2024-46781](https://nvd.nist.gov/vuln/detail/CVE-2024-46781){: external}, [CVE-2024-46782](https://nvd.nist.gov/vuln/detail/CVE-2024-46782){: external}, [CVE-2024-46783](https://nvd.nist.gov/vuln/detail/CVE-2024-46783){: external}, [CVE-2024-46784](https://nvd.nist.gov/vuln/detail/CVE-2024-46784){: external}, [CVE-2024-46785](https://nvd.nist.gov/vuln/detail/CVE-2024-46785){: external}, [CVE-2024-46786](https://nvd.nist.gov/vuln/detail/CVE-2024-46786){: external}, [CVE-2024-46787](https://nvd.nist.gov/vuln/detail/CVE-2024-46787){: external}, [CVE-2024-46788](https://nvd.nist.gov/vuln/detail/CVE-2024-46788){: external}, [CVE-2024-46791](https://nvd.nist.gov/vuln/detail/CVE-2024-46791){: external}, [CVE-2024-46792](https://nvd.nist.gov/vuln/detail/CVE-2024-46792){: external}, [CVE-2024-46793](https://nvd.nist.gov/vuln/detail/CVE-2024-46793){: external}, [CVE-2024-46794](https://nvd.nist.gov/vuln/detail/CVE-2024-46794){: external}, [CVE-2024-46795](https://nvd.nist.gov/vuln/detail/CVE-2024-46795){: external}, [CVE-2024-46797](https://nvd.nist.gov/vuln/detail/CVE-2024-46797){: external}, [CVE-2024-46798](https://nvd.nist.gov/vuln/detail/CVE-2024-46798){: external}, [CVE-2024-46822](https://nvd.nist.gov/vuln/detail/CVE-2024-46822){: external}, [CVE-2024-46823](https://nvd.nist.gov/vuln/detail/CVE-2024-46823){: external}, [CVE-2024-46824](https://nvd.nist.gov/vuln/detail/CVE-2024-46824){: external}, [CVE-2024-46825](https://nvd.nist.gov/vuln/detail/CVE-2024-46825){: external}, [CVE-2024-46826](https://nvd.nist.gov/vuln/detail/CVE-2024-46826){: external}, [CVE-2024-46827](https://nvd.nist.gov/vuln/detail/CVE-2024-46827){: external}, [CVE-2024-46828](https://nvd.nist.gov/vuln/detail/CVE-2024-46828){: external}, [CVE-2024-46829](https://nvd.nist.gov/vuln/detail/CVE-2024-46829){: external}, [CVE-2024-46830](https://nvd.nist.gov/vuln/detail/CVE-2024-46830){: external}, [CVE-2024-46831](https://nvd.nist.gov/vuln/detail/CVE-2024-46831){: external}, [CVE-2024-46832](https://nvd.nist.gov/vuln/detail/CVE-2024-46832){: external}, [CVE-2024-46834](https://nvd.nist.gov/vuln/detail/CVE-2024-46834){: external}, [CVE-2024-46835](https://nvd.nist.gov/vuln/detail/CVE-2024-46835){: external}, [CVE-2024-46836](https://nvd.nist.gov/vuln/detail/CVE-2024-46836){: external}, [CVE-2024-46838](https://nvd.nist.gov/vuln/detail/CVE-2024-46838){: external}, [CVE-2024-46840](https://nvd.nist.gov/vuln/detail/CVE-2024-46840){: external}, [CVE-2024-46841](https://nvd.nist.gov/vuln/detail/CVE-2024-46841){: external}, [CVE-2024-46842](https://nvd.nist.gov/vuln/detail/CVE-2024-46842){: external}, [CVE-2024-46843](https://nvd.nist.gov/vuln/detail/CVE-2024-46843){: external}, [CVE-2024-46844](https://nvd.nist.gov/vuln/detail/CVE-2024-46844){: external}, [CVE-2024-46845](https://nvd.nist.gov/vuln/detail/CVE-2024-46845){: external}, [CVE-2024-46846](https://nvd.nist.gov/vuln/detail/CVE-2024-46846){: external}, [CVE-2024-46847](https://nvd.nist.gov/vuln/detail/CVE-2024-46847){: external}, [CVE-2024-46848](https://nvd.nist.gov/vuln/detail/CVE-2024-46848){: external}, [CVE-2024-47663](https://nvd.nist.gov/vuln/detail/CVE-2024-47663){: external}, [CVE-2024-47664](https://nvd.nist.gov/vuln/detail/CVE-2024-47664){: external}, [CVE-2024-47665](https://nvd.nist.gov/vuln/detail/CVE-2024-47665){: external}, [CVE-2024-47666](https://nvd.nist.gov/vuln/detail/CVE-2024-47666){: external}, [CVE-2024-47667](https://nvd.nist.gov/vuln/detail/CVE-2024-47667){: external}, [CVE-2024-47668](https://nvd.nist.gov/vuln/detail/CVE-2024-47668){: external}, [CVE-2024-47669](https://nvd.nist.gov/vuln/detail/CVE-2024-47669){: external}, [CVE-2024-47814](https://nvd.nist.gov/vuln/detail/CVE-2024-47814){: external}, [CVE-2024-50602](https://nvd.nist.gov/vuln/detail/CVE-2024-50602){: external}, [CVE-2024-53008](https://nvd.nist.gov/vuln/detail/CVE-2024-53008){: external}. |
| HAProxy | 55c1488 | 14daa78 | Security fixes for [CVE-2024-10963](https://nvd.nist.gov/vuln/detail/CVE-2024-10963){: external}, [CVE-2024-11168](https://nvd.nist.gov/vuln/detail/CVE-2024-11168){: external}, [CVE-2024-9287](https://nvd.nist.gov/vuln/detail/CVE-2024-9287){: external}, [CVE-2024-10041](https://nvd.nist.gov/vuln/detail/CVE-2024-10041){: external}. |
| GPU Device Plug-in and Installer | 96f9b63 | 8904e33 | Security fixes for [CVE-2024-10963](https://nvd.nist.gov/vuln/detail/CVE-2024-10963){: external}, [CVE-2024-50192](https://nvd.nist.gov/vuln/detail/CVE-2024-50192){: external}, [CVE-2024-27399](https://nvd.nist.gov/vuln/detail/CVE-2024-27399){: external}, [CVE-2024-38564](https://nvd.nist.gov/vuln/detail/CVE-2024-38564){: external}, [CVE-2024-10041](https://nvd.nist.gov/vuln/detail/CVE-2024-10041){: external}, [CVE-2024-50082](https://nvd.nist.gov/vuln/detail/CVE-2024-50082){: external}, [CVE-2024-50099](https://nvd.nist.gov/vuln/detail/CVE-2024-50099){: external}, [CVE-2024-50256](https://nvd.nist.gov/vuln/detail/CVE-2024-50256){: external}, [CVE-2024-50264](https://nvd.nist.gov/vuln/detail/CVE-2024-50264){: external}, [CVE-2024-9287](https://nvd.nist.gov/vuln/detail/CVE-2024-9287){: external}, [CVE-2024-27043](https://nvd.nist.gov/vuln/detail/CVE-2024-27043){: external}, [CVE-2024-49949](https://nvd.nist.gov/vuln/detail/CVE-2024-49949){: external}, [CVE-2024-11168](https://nvd.nist.gov/vuln/detail/CVE-2024-11168){: external}, [CVE-2024-50110](https://nvd.nist.gov/vuln/detail/CVE-2024-50110){: external}, [CVE-2024-50142](https://nvd.nist.gov/vuln/detail/CVE-2024-50142){: external}, [CVE-2024-46858](https://nvd.nist.gov/vuln/detail/CVE-2024-46858){: external}, [CVE-2024-46695](https://nvd.nist.gov/vuln/detail/CVE-2024-46695){: external}. |
{: caption="Changes since version 1.31.3_1532" caption-side="bottom"}



### Worker node fix pack 1.31.3_1532, released 05 December 2024
{: #1313_1532_W}

The following table shows the changes that are in the worker node fix pack 1.31.3_1531. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages | 5.4.0-200-generic | 5.4.0-200-generic| Worker node kernel & package updates for [CVE-2024-41671](https://nvd.nist.gov/vuln/detail/CVE-2024-41671){: external}, [CVE-2024-52530](https://nvd.nist.gov/vuln/detail/CVE-2024-52530){: external}, [CVE-2024-52531](https://nvd.nist.gov/vuln/detail/CVE-2024-52531){: external}, [CVE-2024-52532](https://nvd.nist.gov/vuln/detail/CVE-2024-52532){: external}, [CVE-2024-52533](https://nvd.nist.gov/vuln/detail/CVE-2024-52533){: external}, [CVE-2024-9287](https://nvd.nist.gov/vuln/detail/CVE-2024-9287){: external}. |
| Ubuntu 24.04 Packages | 6.8.0-48-generic | 6.8.0-48-generic | Worker node kernel & package updates for [CVE-2024-10224](https://nvd.nist.gov/vuln/detail/CVE-2024-10224){: external}, [CVE-2024-11003](https://nvd.nist.gov/vuln/detail/CVE-2024-11003){: external}, [CVE-2024-43882](https://nvd.nist.gov/vuln/detail/CVE-2024-43882){: external}, [CVE-2024-46800](https://nvd.nist.gov/vuln/detail/CVE-2024-46800){: external}, [CVE-2024-48990](https://nvd.nist.gov/vuln/detail/CVE-2024-48990){: external}, [CVE-2024-48991](https://nvd.nist.gov/vuln/detail/CVE-2024-48991){: external}, [CVE-2024-48992](https://nvd.nist.gov/vuln/detail/CVE-2024-48992){: external}, [CVE-2024-52533](https://nvd.nist.gov/vuln/detail/CVE-2024-52533){: external}, [CVE-2024-9287](https://nvd.nist.gov/vuln/detail/CVE-2024-9287){: external}, [CVE-2024-9681](https://nvd.nist.gov/vuln/detail/CVE-2024-9681){: external}. |
| HAProxy | N/A | N/A | N/A |
| Containerd | N/A| N/A| N/A |
| Kubernetes | 1.31.2 | 1.31.3 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.3){: external}. |
| GPU Device Plug-in and Installer | 96f9b63 | 995bd7 | Security fixes for [CVE-2024-10041](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-10041){: external}, [CVE-2024-10963](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-10963){: external}, [CVE-2024-27043](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-27043){: external}, [CVE-2024-27399](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-27399){: external}, [CVE-2024-38564](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-38564){: external}, [CVE-2024-46858](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-46858){: external}. |
{: caption="Changes since version 1.31.2_1529" caption-side="bottom"}



### Master fix pack 1.31.3_1530, released 04 December 2024
{: #1313_1530_M}

The following table shows the changes that are in the master fix pack 1.31.3_1530. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.2-2 | v1.31.2-4 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | c4a05b0 | 743ed58 | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.7 | v2.10.8 | New version contains updates and security fixes. |
| Kubernetes | v1.31.2 | v1.31.3 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.3){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 3051 | 3079 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.20 | v0.13.21 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.21){: external}. |
{: caption="Changes since version 1.31.2_1528" caption-side="bottom"}



### Worker node fix pack 1.31.2_1529, released 18 November 2024
{: #1312_1529_W}

The following table shows the changes that are in the worker node fix pack 1.31.2_1529. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages | 5.4.0-200-generic | 5.4.0-200-generic | N/A |
| Ubuntu 24.04 Packages | 6.8.0-48-generic | 6.8.0-48-generic | N/A |
| Containerd | 1.7.23 | 1.7.23 | N/A |
| Kubernetes | 1.31.1 | 1.31.2 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.2){: external}. |
| HAProxy | 885986 | 55c148 | Security fixes for [CVE-2023-45539](https://nvd.nist.gov/vuln/detail/CVE-2023-45539){: external}, [CVE-2024-3596](https://nvd.nist.gov/vuln/detail/CVE-2024-3596){: external}, [CVE-2019-12900](https://nvd.nist.gov/vuln/detail/CVE-2019-12900){: external}, [CVE-2024-50602](https://nvd.nist.gov/vuln/detail/CVE-2024-50602){: external}. |
| GPU Device Plug-in and Installer | 33c70dd | 96f9b63 | Security fixes for [CVE-2022-48773](https://nvd.nist.gov/vuln/detail/CVE-2022-48773){: external}, [CVE-2022-48936](https://nvd.nist.gov/vuln/detail/CVE-2022-48936){: external}, [CVE-2023-52492](https://nvd.nist.gov/vuln/detail/CVE-2023-52492){: external}, [CVE-2024-24857](https://nvd.nist.gov/vuln/detail/CVE-2024-24857){: external}, [CVE-2024-26851](https://nvd.nist.gov/vuln/detail/CVE-2024-26851){: external}, [CVE-2024-26924](https://nvd.nist.gov/vuln/detail/CVE-2024-26924){: external}, [CVE-2024-26976](https://nvd.nist.gov/vuln/detail/CVE-2024-26976){: external}, [CVE-2024-27017](https://nvd.nist.gov/vuln/detail/CVE-2024-27017){: external}, [CVE-2024-27062](https://nvd.nist.gov/vuln/detail/CVE-2024-27062){: external}, [CVE-2024-35839](https://nvd.nist.gov/vuln/detail/CVE-2024-35839){: external}, [CVE-2024-35898](https://nvd.nist.gov/vuln/detail/CVE-2024-35898){: external}, [CVE-2024-35939](https://nvd.nist.gov/vuln/detail/CVE-2024-35939){: external}, [CVE-2024-38540](https://nvd.nist.gov/vuln/detail/CVE-2024-38540){: external}, [CVE-2024-38541](https://nvd.nist.gov/vuln/detail/CVE-2024-38541){: external}, [CVE-2024-38586](https://nvd.nist.gov/vuln/detail/CVE-2024-38586){: external}, [CVE-2024-38608](https://nvd.nist.gov/vuln/detail/CVE-2024-38608){: external}, [CVE-2024-39503](https://nvd.nist.gov/vuln/detail/CVE-2024-39503){: external}, [CVE-2024-40924](https://nvd.nist.gov/vuln/detail/CVE-2024-40924){: external}, [CVE-2024-40961](https://nvd.nist.gov/vuln/detail/CVE-2024-40961){: external}, [CVE-2024-40983](https://nvd.nist.gov/vuln/detail/CVE-2024-40983){: external}, [CVE-2024-40984](https://nvd.nist.gov/vuln/detail/CVE-2024-40984){: external}, [CVE-2024-41009](https://nvd.nist.gov/vuln/detail/CVE-2024-41009){: external}, [CVE-2024-41042](https://nvd.nist.gov/vuln/detail/CVE-2024-41042){: external}, [CVE-2024-41066](https://nvd.nist.gov/vuln/detail/CVE-2024-41066){: external}, [CVE-2024-41092](https://nvd.nist.gov/vuln/detail/CVE-2024-41092){: external}, [CVE-2024-41093](https://nvd.nist.gov/vuln/detail/CVE-2024-41093){: external}, [CVE-2024-42070](https://nvd.nist.gov/vuln/detail/CVE-2024-42070){: external}, [CVE-2024-42079](https://nvd.nist.gov/vuln/detail/CVE-2024-42079){: external}, [CVE-2024-42244](https://nvd.nist.gov/vuln/detail/CVE-2024-42244){: external}, [CVE-2024-42284](https://nvd.nist.gov/vuln/detail/CVE-2024-42284){: external}, [CVE-2024-42292](https://nvd.nist.gov/vuln/detail/CVE-2024-42292){: external}, [CVE-2024-42301](https://nvd.nist.gov/vuln/detail/CVE-2024-42301){: external}, [CVE-2024-43854](https://nvd.nist.gov/vuln/detail/CVE-2024-43854){: external}, [CVE-2024-43880](https://nvd.nist.gov/vuln/detail/CVE-2024-43880){: external}, [CVE-2024-43889](https://nvd.nist.gov/vuln/detail/CVE-2024-43889){: external}, [CVE-2024-43892](https://nvd.nist.gov/vuln/detail/CVE-2024-43892){: external}, [CVE-2024-44935](https://nvd.nist.gov/vuln/detail/CVE-2024-44935){: external}, [CVE-2024-44989](https://nvd.nist.gov/vuln/detail/CVE-2024-44989){: external}, [CVE-2024-44990](https://nvd.nist.gov/vuln/detail/CVE-2024-44990){: external}, [CVE-2024-45018](https://nvd.nist.gov/vuln/detail/CVE-2024-45018){: external}, [CVE-2024-46826](https://nvd.nist.gov/vuln/detail/CVE-2024-46826){: external}, [CVE-2024-47668](https://nvd.nist.gov/vuln/detail/CVE-2024-47668){: external}, [CVE-2024-3596](https://nvd.nist.gov/vuln/detail/CVE-2024-3596){: external}, [CVE-2019-12900](https://nvd.nist.gov/vuln/detail/CVE-2019-12900){: external}, [CVE-2024-50602](https://nvd.nist.gov/vuln/detail/CVE-2024-50602){: external}. |
{: caption="Changes since version 1.31.1_1527" caption-side="bottom"}



### Master fix pack 1.31.2_1528, released 13 November 2024
{: #1312_1528_M}

The following table shows the changes that are in the master fix pack 1.31.2_1528. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.5.15 | v2.5.16 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.1-6 | v1.31.2-2 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 77dac6b | c4a05b0 | New version contains updates and security fixes. |
| Kubernetes | v1.31.1 | v1.31.2 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.2){: external}. |
{: caption="Changes since version 1.31.1_1526" caption-side="bottom"}



### Worker node fix pack 1.31.1_1527, released 04 November 2024
{: #1311_1527_W}

The following table shows the changes that are in the worker node fix pack 1.31.1_1527. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages	| 5.4.0-198-generic	| 5.4.0-200-generic	| Kernel and package updates for [CVE-2021-47212](https://nvd.nist.gov/vuln/detail/CVE-2021-47212){: external}, [CVE-2022-36402](https://nvd.nist.gov/vuln/detail/CVE-2022-36402){: external}, [CVE-2023-52531](https://nvd.nist.gov/vuln/detail/CVE-2023-52531){: external}, [CVE-2023-52614](https://nvd.nist.gov/vuln/detail/CVE-2023-52614){: external}, [CVE-2024-20696](https://nvd.nist.gov/vuln/detail/CVE-2024-20696){: external}, [CVE-2024-26607](https://nvd.nist.gov/vuln/detail/CVE-2024-26607){: external}, [CVE-2024-26640](https://nvd.nist.gov/vuln/detail/CVE-2024-26640){: external}, [CVE-2024-26641](https://nvd.nist.gov/vuln/detail/CVE-2024-26641){: external}, [CVE-2024-26668](https://nvd.nist.gov/vuln/detail/CVE-2024-26668){: external}, [CVE-2024-26669](https://nvd.nist.gov/vuln/detail/CVE-2024-26669){: external}, [CVE-2024-26800](https://nvd.nist.gov/vuln/detail/CVE-2024-26800){: external}, [CVE-2024-26885](https://nvd.nist.gov/vuln/detail/CVE-2024-26885){: external}, [CVE-2024-26891](https://nvd.nist.gov/vuln/detail/CVE-2024-26891){: external}, [CVE-2024-26960](https://nvd.nist.gov/vuln/detail/CVE-2024-26960){: external}, [CVE-2024-27051](https://nvd.nist.gov/vuln/detail/CVE-2024-27051){: external}, [CVE-2024-27397](https://nvd.nist.gov/vuln/detail/CVE-2024-27397){: external}, [CVE-2024-35848](https://nvd.nist.gov/vuln/detail/CVE-2024-35848){: external}, [CVE-2024-37891](https://nvd.nist.gov/vuln/detail/CVE-2024-37891){: external}, [CVE-2024-38602](https://nvd.nist.gov/vuln/detail/CVE-2024-38602){: external}, [CVE-2024-38611](https://nvd.nist.gov/vuln/detail/CVE-2024-38611){: external}, [CVE-2024-38630](https://nvd.nist.gov/vuln/detail/CVE-2024-38630){: external}, [CVE-2024-40929](https://nvd.nist.gov/vuln/detail/CVE-2024-40929){: external}, [CVE-2024-41071](https://nvd.nist.gov/vuln/detail/CVE-2024-41071){: external}, [CVE-2024-41073](https://nvd.nist.gov/vuln/detail/CVE-2024-41073){: external}, [CVE-2024-42229](https://nvd.nist.gov/vuln/detail/CVE-2024-42229){: external}, [CVE-2024-42244](https://nvd.nist.gov/vuln/detail/CVE-2024-42244){: external}, [CVE-2024-45016](https://nvd.nist.gov/vuln/detail/CVE-2024-45016){: external}	|
| Ubuntu 24.04 Packages	| 6.8.0-47-generic	| 6.8.0-48-generic	| Kernel and package updates for [CVE-2024-20696](https://nvd.nist.gov/vuln/detail/CVE-2024-20696){: external}, [CVE-2024-27022](https://nvd.nist.gov/vuln/detail/CVE-2024-27022){: external}, [CVE-2024-37891](https://nvd.nist.gov/vuln/detail/CVE-2024-37891){: external}, [CVE-2024-41022](https://nvd.nist.gov/vuln/detail/CVE-2024-41022){: external}, [CVE-2024-41311](https://nvd.nist.gov/vuln/detail/CVE-2024-41311){: external}, [CVE-2024-42271](https://nvd.nist.gov/vuln/detail/CVE-2024-42271){: external}, [CVE-2024-42280](https://nvd.nist.gov/vuln/detail/CVE-2024-42280){: external}, [CVE-2024-43858](https://nvd.nist.gov/vuln/detail/CVE-2024-43858){: external}, [CVE-2024-45016](https://nvd.nist.gov/vuln/detail/CVE-2024-45016){: external}	|
| GPU Device Plug-in and Installer	| 68e8137	| 33c70dd	| Driver update and security fixes for [CVE-2024-5535](https://nvd.nist.gov/vuln/detail/CVE-2024-5535){: external}, [CVE-2024-6232](https://nvd.nist.gov/vuln/detail/CVE-2024-6232){: external}	|
{: caption="Changes since version 1.31.1_1524" caption-side="bottom"}



### Master fix pack 1.31.1_1526, released 30 October 2024
{: #1311_1526_M}

The following table shows the changes that are in the master fix pack 1.31.1_1526. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.28.1 | v3.28.2 | See the [Calico release notes](https://docs.tigera.io/calico/3.28/release-notes/#v3.28.2){: external}. |
| Cluster health image | v1.6.2 | v1.6.3 | New version contains updates and security fixes. |
| etcd | v3.5.15 | v3.5.16 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.16){: external}. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.1-1 | v1.31.1-6 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 446 | 447 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 5b17dab | 77dac6b | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.5 | v2.10.7 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.18 | v0.13.20 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.20){: external}. |
| Tigera Operator | v1.34.3 | v1.34.5 | See the [Tigera Operator release notes](https://github.com/tigera/operator/releases/tag/v1.34.5){: external}. |
{: caption="Changes since version 1.31.1_1521" caption-side="bottom"}



### Worker node fix pack 1.31.1_1524, released 21 October 2024
{: #1311_1524_W}

The following table shows the changes that are in the worker node fix pack 1.31.1_1524. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages | 5.4.0-196-generic | 5.4.0-198-generic | Kernel and package updates for [CVE-2022-36227](https://nvd.nist.gov/vuln/detail/CVE-2022-36227){: external}, [CVE-2024-26960](https://nvd.nist.gov/vuln/detail/CVE-2024-26960){: external}, [CVE-2024-27397](https://nvd.nist.gov/vuln/detail/CVE-2024-27397){: external}, [CVE-2024-38630](https://nvd.nist.gov/vuln/detail/CVE-2024-38630){: external}, [CVE-2024-45016](https://nvd.nist.gov/vuln/detail/CVE-2024-45016){: external}, [CVE-2024-5742](https://nvd.nist.gov/vuln/detail/CVE-2024-5742){: external}. | 
| Haproxy | 67d03375 | 88598691 | Security fixes for [CVE-2024-5535](https://nvd.nist.gov/vuln/detail/CVE-2024-5535){: external}. |
{: caption="Changes since version 1.31.1_1523" caption-side="bottom"}



### Worker node fix pack 1.31.1_1523, released 09 October 2024
{: #1311_1523_W}

The following table shows the changes that are in the worker node fix pack 1.31.1_1523. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages | N/A | N/A | Package updates for [CVE-2023-26112](https://nvd.nist.gov/vuln/detail/CVE-2023-26112){: external}, [CVE-2024-43802](https://nvd.nist.gov/vuln/detail/CVE-2024-43802){: external}. |
| Ubuntu 24.04 Packages | N/A | N/A | Package updates for [CVE-2024-43802](https://nvd.nist.gov/vuln/detail/CVE-2024-43802){: external}. |
| Haproxy | 546887ab | 67d03375 | Security fixes for [CVE-2024-4032](https://nvd.nist.gov/vuln/detail/CVE-2024-4032){: external}, [CVE-2024-6232](https://nvd.nist.gov/vuln/detail/CVE-2024-6232){: external}, [CVE-2024-6923](https://nvd.nist.gov/vuln/detail/CVE-2024-6923){: external}, [CVE-2024-45490](https://nvd.nist.gov/vuln/detail/CVE-2024-45490){: external}, [CVE-2024-45491](https://nvd.nist.gov/vuln/detail/CVE-2024-45491){: external}, [CVE-2024-45492](https://nvd.nist.gov/vuln/detail/CVE-2024-45492){: external}. |
| GPU Device Plug-in and Installer | a248cf6b | 68e8137 | Driver update and security fixes for [CVE-2024-26880](https://nvd.nist.gov/vuln/detail/CVE-2024-26880){: external}, [CVE-2024-26894](https://nvd.nist.gov/vuln/detail/CVE-2024-26894){: external}, [CVE-2024-39506](https://nvd.nist.gov/vuln/detail/CVE-2024-39506){: external}, [CVE-2024-41040](https://nvd.nist.gov/vuln/detail/CVE-2024-41040){: external}, [CVE-2023-52800](https://nvd.nist.gov/vuln/detail/CVE-2023-52800){: external}, [CVE-2024-40989](https://nvd.nist.gov/vuln/detail/CVE-2024-40989){: external}, [CVE-2024-42090](https://nvd.nist.gov/vuln/detail/CVE-2024-42090){: external}, [CVE-2021-47385](https://nvd.nist.gov/vuln/detail/CVE-2021-47385){: external}, [CVE-2023-52470](https://nvd.nist.gov/vuln/detail/CVE-2023-52470){: external}, [CVE-2023-52683](https://nvd.nist.gov/vuln/detail/CVE-2023-52683){: external}, [CVE-2024-42238](https://nvd.nist.gov/vuln/detail/CVE-2024-42238){: external}, [CVE-2024-42265](https://nvd.nist.gov/vuln/detail/CVE-2024-42265){: external}, [CVE-2021-47384](https://nvd.nist.gov/vuln/detail/CVE-2021-47384){: external}, [CVE-2024-36922](https://nvd.nist.gov/vuln/detail/CVE-2024-36922){: external}, [CVE-2024-42114](https://nvd.nist.gov/vuln/detail/CVE-2024-42114){: external}, [CVE-2024-42228](https://nvd.nist.gov/vuln/detail/CVE-2024-42228){: external}, [CVE-2024-40912](https://nvd.nist.gov/vuln/detail/CVE-2024-40912){: external}, [CVE-2024-40931](https://nvd.nist.gov/vuln/detail/CVE-2024-40931){: external}, [CVE-2024-42124](https://nvd.nist.gov/vuln/detail/CVE-2024-42124){: external}, [CVE-2021-47289](https://nvd.nist.gov/vuln/detail/CVE-2021-47289){: external}, [CVE-2023-52840](https://nvd.nist.gov/vuln/detail/CVE-2023-52840){: external}, [CVE-2024-26595](https://nvd.nist.gov/vuln/detail/CVE-2024-26595){: external}, [CVE-2024-36901](https://nvd.nist.gov/vuln/detail/CVE-2024-36901){: external}, [CVE-2024-6923](https://nvd.nist.gov/vuln/detail/CVE-2024-6923){: external}, [CVE-2024-38558](https://nvd.nist.gov/vuln/detail/CVE-2024-38558){: external}, [CVE-2024-41008](https://nvd.nist.gov/vuln/detail/CVE-2024-41008){: external}, [CVE-2024-41012](https://nvd.nist.gov/vuln/detail/CVE-2024-41012){: external}, [CVE-2024-4032](https://nvd.nist.gov/vuln/detail/CVE-2024-4032){: external}, [CVE-2024-41007](https://nvd.nist.gov/vuln/detail/CVE-2024-41007){: external}, [CVE-2024-41035](https://nvd.nist.gov/vuln/detail/CVE-2024-41035){: external}, [CVE-2021-47527](https://nvd.nist.gov/vuln/detail/CVE-2021-47527){: external}, [CVE-2022-48754](https://nvd.nist.gov/vuln/detail/CVE-2022-48754){: external}, [CVE-2023-6040](https://nvd.nist.gov/vuln/detail/CVE-2023-6040){: external}, [CVE-2024-40978](https://nvd.nist.gov/vuln/detail/CVE-2024-40978){: external}, [CVE-2021-47582](https://nvd.nist.gov/vuln/detail/CVE-2021-47582){: external}, [CVE-2024-38581](https://nvd.nist.gov/vuln/detail/CVE-2024-38581){: external}, [CVE-2024-41090](https://nvd.nist.gov/vuln/detail/CVE-2024-41090){: external}, [CVE-2024-45492](https://nvd.nist.gov/vuln/detail/CVE-2024-45492){: external}, [CVE-2021-47321](https://nvd.nist.gov/vuln/detail/CVE-2021-47321){: external}, [CVE-2024-36920](https://nvd.nist.gov/vuln/detail/CVE-2024-36920){: external}, [CVE-2024-40954](https://nvd.nist.gov/vuln/detail/CVE-2024-40954){: external}, [CVE-2024-40995](https://nvd.nist.gov/vuln/detail/CVE-2024-40995){: external}, [CVE-2024-40998](https://nvd.nist.gov/vuln/detail/CVE-2024-40998){: external}, [CVE-2024-42152](https://nvd.nist.gov/vuln/detail/CVE-2024-42152){: external}, [CVE-2021-46984](https://nvd.nist.gov/vuln/detail/CVE-2021-46984){: external}, [CVE-2023-52817](https://nvd.nist.gov/vuln/detail/CVE-2023-52817){: external}, [CVE-2024-35809](https://nvd.nist.gov/vuln/detail/CVE-2024-35809){: external}, [CVE-2024-35944](https://nvd.nist.gov/vuln/detail/CVE-2024-35944){: external}, [CVE-2024-23848](https://nvd.nist.gov/vuln/detail/CVE-2024-23848){: external}, [CVE-2024-42226](https://nvd.nist.gov/vuln/detail/CVE-2024-42226){: external}, [CVE-2024-42094](https://nvd.nist.gov/vuln/detail/CVE-2024-42094){: external}, [CVE-2021-47101](https://nvd.nist.gov/vuln/detail/CVE-2021-47101){: external}, [CVE-2024-26720](https://nvd.nist.gov/vuln/detail/CVE-2024-26720){: external}, [CVE-2024-26923](https://nvd.nist.gov/vuln/detail/CVE-2024-26923){: external}, [CVE-2024-41005](https://nvd.nist.gov/vuln/detail/CVE-2024-41005){: external}, [CVE-2023-52798](https://nvd.nist.gov/vuln/detail/CVE-2023-52798){: external}, [CVE-2024-42096](https://nvd.nist.gov/vuln/detail/CVE-2024-42096){: external}, [CVE-2024-40988](https://nvd.nist.gov/vuln/detail/CVE-2024-40988){: external}, [CVE-2024-42084](https://nvd.nist.gov/vuln/detail/CVE-2024-42084){: external}, [CVE-2024-42240](https://nvd.nist.gov/vuln/detail/CVE-2024-42240){: external}, [CVE-2024-41014](https://nvd.nist.gov/vuln/detail/CVE-2024-41014){: external}, [CVE-2024-41041](https://nvd.nist.gov/vuln/detail/CVE-2024-41041){: external}, [CVE-2024-41065](https://nvd.nist.gov/vuln/detail/CVE-2024-41065){: external}, [CVE-2024-42322](https://nvd.nist.gov/vuln/detail/CVE-2024-42322){: external}, [CVE-2022-48760](https://nvd.nist.gov/vuln/detail/CVE-2022-48760){: external}, [CVE-2024-26600](https://nvd.nist.gov/vuln/detail/CVE-2024-26600){: external}, [CVE-2024-26939](https://nvd.nist.gov/vuln/detail/CVE-2024-26939){: external}, [CVE-2024-40972](https://nvd.nist.gov/vuln/detail/CVE-2024-40972){: external}, [CVE-2024-40997](https://nvd.nist.gov/vuln/detail/CVE-2024-40997){: external}, [CVE-2024-43830](https://nvd.nist.gov/vuln/detail/CVE-2024-43830){: external}, [CVE-2024-38559](https://nvd.nist.gov/vuln/detail/CVE-2024-38559){: external}, [CVE-2024-38619](https://nvd.nist.gov/vuln/detail/CVE-2024-38619){: external}, [CVE-2024-39501](https://nvd.nist.gov/vuln/detail/CVE-2024-39501){: external}, [CVE-2024-42131](https://nvd.nist.gov/vuln/detail/CVE-2024-42131){: external}, [CVE-2021-47393](https://nvd.nist.gov/vuln/detail/CVE-2021-47393){: external}, [CVE-2022-48836](https://nvd.nist.gov/vuln/detail/CVE-2022-48836){: external}, [CVE-2023-52809](https://nvd.nist.gov/vuln/detail/CVE-2023-52809){: external}, [CVE-2024-26638](https://nvd.nist.gov/vuln/detail/CVE-2024-26638){: external}, [CVE-2021-47609](https://nvd.nist.gov/vuln/detail/CVE-2021-47609){: external}, [CVE-2024-26855](https://nvd.nist.gov/vuln/detail/CVE-2024-26855){: external}, [CVE-2024-36902](https://nvd.nist.gov/vuln/detail/CVE-2024-36902){: external}, [CVE-2021-47287](https://nvd.nist.gov/vuln/detail/CVE-2021-47287){: external}, [CVE-2024-40960](https://nvd.nist.gov/vuln/detail/CVE-2024-40960){: external}, [CVE-2024-41064](https://nvd.nist.gov/vuln/detail/CVE-2024-41064){: external}, [CVE-2024-41071](https://nvd.nist.gov/vuln/detail/CVE-2024-41071){: external}, [CVE-2024-42225](https://nvd.nist.gov/vuln/detail/CVE-2024-42225){: external}, [CVE-2024-45490](https://nvd.nist.gov/vuln/detail/CVE-2024-45490){: external}, [CVE-2021-47352](https://nvd.nist.gov/vuln/detail/CVE-2021-47352){: external}, [CVE-2024-26769](https://nvd.nist.gov/vuln/detail/CVE-2024-26769){: external}, [CVE-2024-36939](https://nvd.nist.gov/vuln/detail/CVE-2024-36939){: external}, [CVE-2024-40977](https://nvd.nist.gov/vuln/detail/CVE-2024-40977){: external}, [CVE-2024-42154](https://nvd.nist.gov/vuln/detail/CVE-2024-42154){: external}, [CVE-2024-35989](https://nvd.nist.gov/vuln/detail/CVE-2024-35989){: external}, [CVE-2024-36919](https://nvd.nist.gov/vuln/detail/CVE-2024-36919){: external}, [CVE-2024-38579](https://nvd.nist.gov/vuln/detail/CVE-2024-38579){: external}, [CVE-2024-41076](https://nvd.nist.gov/vuln/detail/CVE-2024-41076){: external}, [CVE-2024-26645](https://nvd.nist.gov/vuln/detail/CVE-2024-26645){: external}, [CVE-2024-40958](https://nvd.nist.gov/vuln/detail/CVE-2024-40958){: external}, [CVE-2024-41023](https://nvd.nist.gov/vuln/detail/CVE-2024-41023){: external}, [CVE-2024-43871](https://nvd.nist.gov/vuln/detail/CVE-2024-43871){: external}, [CVE-2021-47441](https://nvd.nist.gov/vuln/detail/CVE-2021-47441){: external}, [CVE-2022-48804](https://nvd.nist.gov/vuln/detail/CVE-2022-48804){: external}, [CVE-2023-52478](https://nvd.nist.gov/vuln/detail/CVE-2023-52478){: external}, [CVE-2023-52605](https://nvd.nist.gov/vuln/detail/CVE-2023-52605){: external}, [CVE-2024-26665](https://nvd.nist.gov/vuln/detail/CVE-2024-26665){: external}, [CVE-2024-40904](https://nvd.nist.gov/vuln/detail/CVE-2024-40904){: external}, [CVE-2024-40911](https://nvd.nist.gov/vuln/detail/CVE-2024-40911){: external}, [CVE-2024-41044](https://nvd.nist.gov/vuln/detail/CVE-2024-41044){: external}, [CVE-2024-41039](https://nvd.nist.gov/vuln/detail/CVE-2024-41039){: external}, [CVE-2024-41060](https://nvd.nist.gov/vuln/detail/CVE-2024-41060){: external}, [CVE-2024-42246](https://nvd.nist.gov/vuln/detail/CVE-2024-42246){: external}, [CVE-2024-45491](https://nvd.nist.gov/vuln/detail/CVE-2024-45491){: external}, [CVE-2021-47338](https://nvd.nist.gov/vuln/detail/CVE-2021-47338){: external}, [CVE-2021-47432](https://nvd.nist.gov/vuln/detail/CVE-2021-47432){: external}, [CVE-2021-47560](https://nvd.nist.gov/vuln/detail/CVE-2021-47560){: external}, [CVE-2024-27042](https://nvd.nist.gov/vuln/detail/CVE-2024-27042){: external}, [CVE-2021-47383](https://nvd.nist.gov/vuln/detail/CVE-2021-47383){: external}, [CVE-2024-36953](https://nvd.nist.gov/vuln/detail/CVE-2024-36953){: external}, [CVE-2024-40959](https://nvd.nist.gov/vuln/detail/CVE-2024-40959){: external}, [CVE-2021-47097](https://nvd.nist.gov/vuln/detail/CVE-2021-47097){: external}, [CVE-2024-26717](https://nvd.nist.gov/vuln/detail/CVE-2024-26717){: external}, [CVE-2024-37356](https://nvd.nist.gov/vuln/detail/CVE-2024-37356){: external}, [CVE-2024-41038](https://nvd.nist.gov/vuln/detail/CVE-2024-41038){: external}, [CVE-2024-39471](https://nvd.nist.gov/vuln/detail/CVE-2024-39471){: external}, [CVE-2021-47497](https://nvd.nist.gov/vuln/detail/CVE-2021-47497){: external}, [CVE-2022-48619](https://nvd.nist.gov/vuln/detail/CVE-2022-48619){: external}, [CVE-2022-48866](https://nvd.nist.gov/vuln/detail/CVE-2022-48866){: external}, [CVE-2023-52476](https://nvd.nist.gov/vuln/detail/CVE-2023-52476){: external}, [CVE-2021-47466](https://nvd.nist.gov/vuln/detail/CVE-2021-47466){: external}, [CVE-2023-52522](https://nvd.nist.gov/vuln/detail/CVE-2023-52522){: external}, [CVE-2024-41097](https://nvd.nist.gov/vuln/detail/CVE-2024-41097){: external}, [CVE-2024-42237](https://nvd.nist.gov/vuln/detail/CVE-2024-42237){: external}, [CVE-2021-47412](https://nvd.nist.gov/vuln/detail/CVE-2021-47412){: external}, [CVE-2024-26649](https://nvd.nist.gov/vuln/detail/CVE-2024-26649){: external}, [CVE-2024-41056](https://nvd.nist.gov/vuln/detail/CVE-2024-41056){: external}, [CVE-2024-41013](https://nvd.nist.gov/vuln/detail/CVE-2024-41013){: external}, [CVE-2024-41055](https://nvd.nist.gov/vuln/detail/CVE-2024-41055){: external}, [CVE-2024-26846](https://nvd.nist.gov/vuln/detail/CVE-2024-26846){: external}, [CVE-2024-35884](https://nvd.nist.gov/vuln/detail/CVE-2024-35884){: external}, [CVE-2024-36883](https://nvd.nist.gov/vuln/detail/CVE-2024-36883){: external}, [CVE-2024-40929](https://nvd.nist.gov/vuln/detail/CVE-2024-40929){: external}, [CVE-2024-40901](https://nvd.nist.gov/vuln/detail/CVE-2024-40901){: external}, [CVE-2024-40941](https://nvd.nist.gov/vuln/detail/CVE-2024-40941){: external}, [CVE-2024-41091](https://nvd.nist.gov/vuln/detail/CVE-2024-41091){: external}, [CVE-2021-47386](https://nvd.nist.gov/vuln/detail/CVE-2021-47386){: external}, [CVE-2024-27013](https://nvd.nist.gov/vuln/detail/CVE-2024-27013){: external}, [CVE-2024-35877](https://nvd.nist.gov/vuln/detail/CVE-2024-35877){: external}, [CVE-2024-39499](https://nvd.nist.gov/vuln/detail/CVE-2024-39499){: external}, [CVE-2021-47455](https://nvd.nist.gov/vuln/detail/CVE-2021-47455){: external}, [CVE-2024-38570](https://nvd.nist.gov/vuln/detail/CVE-2024-38570){: external}, [CVE-2024-6232](https://nvd.nist.gov/vuln/detail/CVE-2024-6232){: external}. |
{: caption="Changes since version 1.31.1_1522" caption-side="bottom"}



### Master fix pack 1.31.1_1521, released 25 September 2024
{: #1311_1521_M}

The following table shows the changes that are in the master fix pack 1.31.1_1521. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.5.14 | v2.5.15 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.31.0-3 | v1.31.1-1 | New version contains updates and security fixes. |
| Key Management Service provider | v2.10.4 | v2.10.5 | New version contains updates and security fixes. |
| Kubernetes | v1.31.0 | v1.31.1 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.1){: external}. |
{: caption="Changes since version 1.31.0_1520" caption-side="bottom"}



### Worker node fix pack 1.31.1_1522, released 23 September 2024
{: #1311_1522_W}

The following table shows the changes that are in the worker node fix pack 1.31.1_1522. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages | 5.4.0-193-generic | 5.4.0-196-generic | Worker node kernel & package updates for [CVE-2016-1585](https://nvd.nist.gov/vuln/detail/CVE-2016-1585){: external}, [CVE-2021-46926](https://nvd.nist.gov/vuln/detail/CVE-2021-46926){: external}, [CVE-2021-47188](https://nvd.nist.gov/vuln/detail/CVE-2021-47188){: external}, [CVE-2022-48791](https://nvd.nist.gov/vuln/detail/CVE-2022-48791){: external}, [CVE-2022-48863](https://nvd.nist.gov/vuln/detail/CVE-2022-48863){: external}, [CVE-2023-27043](https://nvd.nist.gov/vuln/detail/CVE-2023-27043){: external}, [CVE-2023-52629](https://nvd.nist.gov/vuln/detail/CVE-2023-52629){: external}, [CVE-2023-52760](https://nvd.nist.gov/vuln/detail/CVE-2023-52760){: external}, [CVE-2024-2201](https://nvd.nist.gov/vuln/detail/CVE-2024-2201){: external}, [CVE-2024-24860](https://nvd.nist.gov/vuln/detail/CVE-2024-24860){: external}, [CVE-2024-26677](https://nvd.nist.gov/vuln/detail/CVE-2024-26677){: external}, [CVE-2024-26787](https://nvd.nist.gov/vuln/detail/CVE-2024-26787){: external}, [CVE-2024-26830](https://nvd.nist.gov/vuln/detail/CVE-2024-26830){: external}, [CVE-2024-26921](https://nvd.nist.gov/vuln/detail/CVE-2024-26921){: external}, [CVE-2024-26929](https://nvd.nist.gov/vuln/detail/CVE-2024-26929){: external}, [CVE-2024-27012](https://nvd.nist.gov/vuln/detail/CVE-2024-27012){: external}, [CVE-2024-36901](https://nvd.nist.gov/vuln/detail/CVE-2024-36901){: external}, [CVE-2024-38570](https://nvd.nist.gov/vuln/detail/CVE-2024-38570){: external}, [CVE-2024-39484](https://nvd.nist.gov/vuln/detail/CVE-2024-39484){: external}, [CVE-2024-39494](https://nvd.nist.gov/vuln/detail/CVE-2024-39494){: external}, [CVE-2024-42160](https://nvd.nist.gov/vuln/detail/CVE-2024-42160){: external}, [CVE-2024-42228](https://nvd.nist.gov/vuln/detail/CVE-2024-42228){: external}, [CVE-2024-45490](https://nvd.nist.gov/vuln/detail/CVE-2024-45490){: external}, [CVE-2024-45491](https://nvd.nist.gov/vuln/detail/CVE-2024-45491){: external}, [CVE-2024-45492](https://nvd.nist.gov/vuln/detail/CVE-2024-45492){: external}, [CVE-2024-6232](https://nvd.nist.gov/vuln/detail/CVE-2024-6232){: external}, [CVE-2024-6345](https://nvd.nist.gov/vuln/detail/CVE-2024-6345){: external}, [CVE-2024-6923](https://nvd.nist.gov/vuln/detail/CVE-2024-6923){: external}, [CVE-2024-7592](https://nvd.nist.gov/vuln/detail/CVE-2024-7592){: external}, [CVE-2024-8088](https://nvd.nist.gov/vuln/detail/CVE-2024-8088){: external}, [CVE-2024-8096](https://nvd.nist.gov/vuln/detail/CVE-2024-8096){: external}
| Ubuntu 24.04 packages | 6.8.0-41-generic | 6.8.0-45-generic | Worker node package updates for [CVE-2023-27043](https://nvd.nist.gov/vuln/detail/CVE-2023-27043){: external}, [CVE-2024-39292](https://nvd.nist.gov/vuln/detail/CVE-2024-39292){: external}, [CVE-2024-39484](https://nvd.nist.gov/vuln/detail/CVE-2024-39484){: external}, [CVE-2024-41009](https://nvd.nist.gov/vuln/detail/CVE-2024-41009){: external}, [CVE-2024-42154](https://nvd.nist.gov/vuln/detail/CVE-2024-42154){: external}, [CVE-2024-42159](https://nvd.nist.gov/vuln/detail/CVE-2024-42159){: external}, [CVE-2024-42160](https://nvd.nist.gov/vuln/detail/CVE-2024-42160){: external}, [CVE-2024-42224](https://nvd.nist.gov/vuln/detail/CVE-2024-42224){: external}, [CVE-2024-42228](https://nvd.nist.gov/vuln/detail/CVE-2024-42228){: external}, [CVE-2024-45490](https://nvd.nist.gov/vuln/detail/CVE-2024-45490){: external}, [CVE-2024-45491](https://nvd.nist.gov/vuln/detail/CVE-2024-45491){: external}, [CVE-2024-45492](https://nvd.nist.gov/vuln/detail/CVE-2024-45492){: external}, [CVE-2024-6232](https://nvd.nist.gov/vuln/detail/CVE-2024-6232){: external}, [CVE-2024-6345](https://nvd.nist.gov/vuln/detail/CVE-2024-6345){: external}, [CVE-2024-6923](https://nvd.nist.gov/vuln/detail/CVE-2024-6923){: external}, [CVE-2024-7006](https://nvd.nist.gov/vuln/detail/CVE-2024-7006){: external}, [CVE-2024-7592](https://nvd.nist.gov/vuln/detail/CVE-2024-7592){: external}, [CVE-2024-8088](https://nvd.nist.gov/vuln/detail/CVE-2024-8088){: external}, [CVE-2024-8096](https://nvd.nist.gov/vuln/detail/CVE-2024-8096){: external}. |
| Containerd | 1.7.21 | 1.7.22 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.22){: external} and [security bulletin for CVE-2024-45310](https://www.ibm.com/support/pages/node/7172017){: external}. |
| Kubernetes | 1.31.0 | 1.31.1 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.1){: external}. |
| Haproxy | N/A | N/A | N/A |
| GPU Device Plug-in and Installer | 91f881a3 | a248cf6b | Security fixes for [CVE-2024-6119](https://exchange.xforce.ibmcloud.com/vulnerabilities/352483){: external}, [CVE-2024-45490](https://exchange.xforce.ibmcloud.com/vulnerabilities/352411){: external}, [CVE-2024-45491](https://exchange.xforce.ibmcloud.com/vulnerabilities/352412){: external}, [CVE-2024-45492](https://exchange.xforce.ibmcloud.com/vulnerabilities/352413){: external}, [CVE-2024-34397](https://exchange.xforce.ibmcloud.com/vulnerabilities/290032){: external}. |
{: caption="Changes since version 1.31.0_1517" caption-side="bottom"}



### Master fix pack 1.31.0_1520 and worker node fix pack 1.31.0_1518, released 18 September 2024
{: #1310_1520M_and_1310_1518W}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.27.4 | v3.28.1 | See the [Calico release notes](https://docs.tigera.io/calico/3.28/release-notes/){: external}. |
| Cluster health image | v1.5.8 | v1.6.2 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.5.13 | v2.5.14 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.30.4-1 | v1.31.0-3 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} File Storage for Classic plug-in and monitor | 445 | 446 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | v1.1.4 | v1.1.5 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 897f067 | 5b17dab | New version contains updates and security fixes. |
| Konnectivity agent and server | v0.30.2 | v0.30.3 | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.30.3){: external}. |
| Kubernetes | v1.30.4 | v1.31.0 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.0){: external}. |
| Kubernetes add-on resizer | 1.8.20 | 1.8.22 | See the [Kubernetes add-on resizer release notes](https://github.com/kubernetes/autoscaler/releases/tag/addon-resizer-1.8.22){: external}. |
| Kubernetes configuration | N/A | N/A | See [Default service settings for Kubernetes components](https://cloud.ibm.com/docs/containers?topic=containers-service-settings){: external}. |
| Kubernetes Metrics Server | v0.7.1 | v0.7.2 | See the [Kubernetes Metrics Server release notes](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.7.2){: external}. |
| Kubernetes snapshot controller | v6.3.3 | v8.0.1 | See the [Kubernetes snapshot controller release notes](https://github.com/kubernetes-csi/external-snapshotter/releases/tag/v8.0.1){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 3022 | 3051 | New version contains updates and security fixes. |
| Pause container image | 3.9 | 3.10 | See the [pause container image release notes](https://github.com/kubernetes/kubernetes/blob/master/build/pause/CHANGELOG.md){: external}. |
| Tigera Operator | v1.32.10-124-iks | v1.34.3 | See the [Tigera Operator release notes](https://github.com/tigera/operator/releases/tag/v1.34.3){: external}. |
{: caption="Changes since version 1.30." caption-side="bottom"}







### Worker node fix pack 1.31.9_1554, released 16 June 2025
{: #cl-boms-1319_1554_W}

The following table shows the components included in the worker node fix pack 1.31.9_1554. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Version | Description |
| ---- | ---- | ---- |
|UBUNTU_24_04|6.8.0-60-generic|Resolves the following CVEs: [CVE-2025-4598](https://nvd.nist.gov/vuln/detail/CVE-2025-4598){: external}.|
|Kubernetes|1.31.9|For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.31.9).|
|containerd|1.7.27|For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.27).|
|HAProxy|951efd90b46e95a54751966c644ac37c4c901f92|Resolves the following CVEs: [CVE-2025-4802](https://nvd.nist.gov/vuln/detail/CVE-2025-4802){: external}, [CVE-2025-32414](https://nvd.nist.gov/vuln/detail/CVE-2025-32414){: external}, and [CVE-2025-3576](https://nvd.nist.gov/vuln/detail/CVE-2025-3576){: external}.|
|GPU Device Plug-in and Installer|cbca3eaad7d585c0d1181e478f39bab25579fb9a|Resolves the following CVEs: [CVE-2025-32414](https://nvd.nist.gov/vuln/detail/CVE-2025-32414){: external}, [CVE-2025-4802](https://nvd.nist.gov/vuln/detail/CVE-2025-4802){: external}, and [CVE-2025-3576](https://nvd.nist.gov/vuln/detail/CVE-2025-3576){: external}.|
{: caption="1.31.9_1554 fix pack." caption-side="bottom"}
{: #cl-boms-1319_1554_W-component-table}
