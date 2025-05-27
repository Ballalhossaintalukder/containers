---

copyright: 
  years: 2023, 2025
lastupdated: "2025-05-27"


keywords: kubernetes, containers, change log, 127 change log, 127 updates

subcollection: containers


---

{{site.data.keyword.attribute-definition-list}}

# Kubernetes version 1.27 change log
{: #changelog_127}

View information about version changes for major, minor, and patch updates that are available for your {{site.data.keyword.containerlong}} clusters that run version 1.27. Changes include updates to Kubernetes and {{site.data.keyword.cloud_notm}} Provider components.
{: shortdesc}



This version is no longer supported. Update your cluster to a [supported version](/docs/containers?topic=containers-cs_versions) as soon as possible.
{: important}



## Overview
{: #changelog_overview_127}

In clusters that run version 1.23 or earlier, the {{site.data.keyword.cloud_notm}} provider version enables Kubernetes APIs and features that are at beta. Most new beta features are disabled by default. Kubernetes alpha features, which are subject to change, are disabled in all versions. For more information, see the [Default service settings for Kubernetes components](/docs/containers?topic=containers-service-settings) and the [feature gates](/docs/containers?topic=containers-service-settings#feature-gates) for each version.

For more information about major, minor, and patch versions and preparation actions between minor versions, see [Kubernetes versions](/docs/containers?topic=containers-cs_versions).
{: tip}

Check the [Security Bulletins on {{site.data.keyword.cloud_notm}} Status](https://cloud.ibm.com/status?component=containers-kubernetes&selected=security){: external} for security vulnerabilities that affect {{site.data.keyword.containerlong_notm}}. You can filter the results to view only Kubernetes Cluster security bulletins that are relevant to {{site.data.keyword.containerlong_notm}}. Change log entries that address other security vulnerabilities but don't also refer to an {{site.data.keyword.IBM_notm}} security bulletin are for vulnerabilities that are not known to affect {{site.data.keyword.containerlong_notm}} in normal usage. If you run privileged containers, run commands on the workers, or execute untrusted code, then you might be at risk.

Some change logs are for _worker node fix packs_, and apply only to worker nodes. You must [apply these patches](/docs/containers?topic=containers-kubernetes-service-cli#cs_worker_update) to ensure security compliance for your worker nodes. These worker node fix packs can be at a higher version than the master because some build fix packs are specific to worker nodes. Other change logs are for _master fix packs_, and apply only to the cluster master. Master fix packs might not be automatically applied. You can choose to [apply them manually](/docs/containers?topic=containers-kubernetes-service-cli#cs_cluster_update). For more information about patch types, see [Update types](/docs/containers?topic=containers-cs_versions#update_types).
{: note}




## Version 1.27 change log
{: #127_changelog}


Review the version 1.27 change log.
{: shortdesc}





### Worker node fix pack 1.27.16_1592, released 10 September 2024
{: #12716_1592_W}

The following table shows the changes that are in the worker node fix pack 1.27.16_1592. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | N/A | N/A | Worker node package updates for [CVE-2016-1585](https://nvd.nist.gov/vuln/detail/CVE-2016-1585){: external}, [CVE-2024-41810](https://nvd.nist.gov/vuln/detail/CVE-2024-41810){: external}, [CVE-2024-41957](https://nvd.nist.gov/vuln/detail/CVE-2024-41957){: external}, [CVE-2024-43374](https://nvd.nist.gov/vuln/detail/CVE-2024-43374){: external}. |
| Kubernetes | N/A | N/A | N/A |
| Containerd | 1.7.20 | 1.7.21 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.21){: external}. |
{: caption="Changes since version 1.27.16_1591" caption-side="bottom"}


### Master fix pack 1.27.16_1590, released 28 August 2024
{: #12716_1590_M}

The following table shows the changes that are in the master fix pack 1.27.16_1590. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.5.7 | v1.5.8 | New version contains updates and security fixes. |
| etcd | v3.5.14 | v3.5.15 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.15){: external}. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.4.23 | v2.4.24 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 312030f | 897f067 | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.12 | v2.8.13 | New version contains updates and security fixes. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2967 | 3022 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.17 | v0.13.18 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.18){: external}. |
{: caption="Changes since version 1.27.16_1587" caption-side="bottom"}


### Worker node fix pack 1.27.16.1591, released 26 August 2024
{: #127161591_W}

The following table shows the changes that are in the worker node fix pack 1.27.16.1591. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 Packages | 5.4.0-192-generic | 5.4.0-193-generic | Worker node kernel & package updates for [CVE-2021-46926](https://nvd.nist.gov/vuln/detail/CVE-2021-46926){: external}, [CVE-2022-48174](https://nvd.nist.gov/vuln/detail/CVE-2022-48174){: external}, [CVE-2023-52629](https://nvd.nist.gov/vuln/detail/CVE-2023-52629){: external}, [CVE-2023-52760](https://nvd.nist.gov/vuln/detail/CVE-2023-52760){: external}, [CVE-2024-2201](https://nvd.nist.gov/vuln/detail/CVE-2024-2201){: external}, [CVE-2024-24860](https://nvd.nist.gov/vuln/detail/CVE-2024-24860){: external}, [CVE-2024-26830](https://nvd.nist.gov/vuln/detail/CVE-2024-26830){: external}, [CVE-2024-26921](https://nvd.nist.gov/vuln/detail/CVE-2024-26921){: external}, [CVE-2024-26929](https://nvd.nist.gov/vuln/detail/CVE-2024-26929){: external}, [CVE-2024-36901](https://nvd.nist.gov/vuln/detail/CVE-2024-36901){: external}, [CVE-2024-39484](https://nvd.nist.gov/vuln/detail/CVE-2024-39484){: external}, CIS benchmark compliance: [1.1.10](https://workbench.cisecurity.org/sections/1985903/recommendations/3181697){: external}, [5.1.3](https://workbench.cisecurity.org/sections/1985916/recommendations/3181709){: external}. |
| Containerd | N/A | N/A | N/A |
| Kubernetes | N/A | N/A | N/A |
| Haproxy | c91c765 | 546887a | Security fixes for [CVE-2024-2398](https://exchange.xforce.ibmcloud.com/vulnerabilities/286430){: external}, [CVE-2024-37370](https://exchange.xforce.ibmcloud.com/vulnerabilities/296012){: external}, [CVE-2024-37371](https://exchange.xforce.ibmcloud.com/vulnerabilities/296013){: external}, [CVE-2024-6345](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-6345){: external}. |
{: caption="Changes since version 1.27.16_1589" caption-side="bottom"}


### Worker node fix pack 1.27.16_1589, released 12 August 2024
{: #12716_1589_W}

The following table shows the changes that are in the worker node fix pack 1.27.16_1589. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-190-generic | 5.4.0-192-generic | Worker node kernel & package updates for [CVE-2022-48655](https://nvd.nist.gov/vuln/detail/CVE-2022-48655){: external}, [CVE-2022-48674](https://nvd.nist.gov/vuln/detail/CVE-2022-48674){: external}, [CVE-2023-52752](https://nvd.nist.gov/vuln/detail/CVE-2023-52752){: external}, [CVE-2024-0397](https://nvd.nist.gov/vuln/detail/CVE-2024-0397){: external}, [CVE-2024-2511](https://nvd.nist.gov/vuln/detail/CVE-2024-2511){: external}, [CVE-2024-26583](https://nvd.nist.gov/vuln/detail/CVE-2024-26583){: external}, [CVE-2024-26584](https://nvd.nist.gov/vuln/detail/CVE-2024-26584){: external}, [CVE-2024-26585](https://nvd.nist.gov/vuln/detail/CVE-2024-26585){: external}, [CVE-2024-26886](https://nvd.nist.gov/vuln/detail/CVE-2024-26886){: external}, [CVE-2024-26907](https://nvd.nist.gov/vuln/detail/CVE-2024-26907){: external}, [CVE-2024-27019](https://nvd.nist.gov/vuln/detail/CVE-2024-27019){: external}, [CVE-2024-36016](https://nvd.nist.gov/vuln/detail/CVE-2024-36016){: external}, [CVE-2024-37370](https://nvd.nist.gov/vuln/detail/CVE-2024-37370){: external}, [CVE-2024-37371](https://nvd.nist.gov/vuln/detail/CVE-2024-37371){: external}, [CVE-2024-4032](https://nvd.nist.gov/vuln/detail/CVE-2024-4032){: external}, [CVE-2024-4741](https://nvd.nist.gov/vuln/detail/CVE-2024-4741){: external}, [CVE-2024-5535](https://nvd.nist.gov/vuln/detail/CVE-2024-5535){: external}, [CVE-2024-7264](https://nvd.nist.gov/vuln/detail/CVE-2024-7264){: external}. |
| RHEL 8 Packages | 4.18.0-553.8.1.el8_10 | 4.18.0-553.16.1.el8_10 | Package updates for [RHSA-2024:5101](https://access.redhat.com/errata/RHSA-2024:5101){: external}, [CVE-2021-46939](https://nvd.nist.gov/vuln/detail/CVE-2021-46939){: external}, [CVE-2021-47018](https://nvd.nist.gov/vuln/detail/CVE-2021-47018){: external}, [CVE-2021-47257](https://nvd.nist.gov/vuln/detail/CVE-2021-47257){: external}, [CVE-2021-47284](https://nvd.nist.gov/vuln/detail/CVE-2021-47284){: external}, [CVE-2021-47304](https://nvd.nist.gov/vuln/detail/CVE-2021-47304){: external}, [CVE-2021-47373](https://nvd.nist.gov/vuln/detail/CVE-2021-47373){: external}, [CVE-2021-47408](https://nvd.nist.gov/vuln/detail/CVE-2021-47408){: external}, [CVE-2021-47461](https://nvd.nist.gov/vuln/detail/CVE-2021-47461){: external}, [CVE-2021-47468](https://nvd.nist.gov/vuln/detail/CVE-2021-47468){: external}, [CVE-2021-47491](https://nvd.nist.gov/vuln/detail/CVE-2021-47491){: external}, [CVE-2021-47548](https://nvd.nist.gov/vuln/detail/CVE-2021-47548){: external}, [CVE-2021-47579](https://nvd.nist.gov/vuln/detail/CVE-2021-47579){: external}, [CVE-2021-47624](https://nvd.nist.gov/vuln/detail/CVE-2021-47624){: external}, [CVE-2022-48632](https://nvd.nist.gov/vuln/detail/CVE-2022-48632){: external}, [CVE-2022-48743](https://nvd.nist.gov/vuln/detail/CVE-2022-48743){: external}, [CVE-2022-48747](https://nvd.nist.gov/vuln/detail/CVE-2022-48747){: external}, [CVE-2022-48757](https://nvd.nist.gov/vuln/detail/CVE-2022-48757){: external}, [CVE-2023-28746](https://nvd.nist.gov/vuln/detail/CVE-2023-28746){: external}, [CVE-2023-52451](https://nvd.nist.gov/vuln/detail/CVE-2023-52451){: external}, [CVE-2023-52463](https://nvd.nist.gov/vuln/detail/CVE-2023-52463){: external}, [CVE-2023-52469](https://nvd.nist.gov/vuln/detail/CVE-2023-52469){: external}, [CVE-2023-52471](https://nvd.nist.gov/vuln/detail/CVE-2023-52471){: external}, [CVE-2023-52486](https://nvd.nist.gov/vuln/detail/CVE-2023-52486){: external}, [CVE-2023-52530](https://nvd.nist.gov/vuln/detail/CVE-2023-52530){: external}, [CVE-2023-52619](https://nvd.nist.gov/vuln/detail/CVE-2023-52619){: external}, [CVE-2023-52622](https://nvd.nist.gov/vuln/detail/CVE-2023-52622){: external}, [CVE-2023-52623](https://nvd.nist.gov/vuln/detail/CVE-2023-52623){: external}, [CVE-2023-52648](https://nvd.nist.gov/vuln/detail/CVE-2023-52648){: external}, [CVE-2023-52653](https://nvd.nist.gov/vuln/detail/CVE-2023-52653){: external}, [CVE-2023-52658](https://nvd.nist.gov/vuln/detail/CVE-2023-52658){: external}, [CVE-2023-52662](https://nvd.nist.gov/vuln/detail/CVE-2023-52662){: external}, [CVE-2023-52679](https://nvd.nist.gov/vuln/detail/CVE-2023-52679){: external}, [CVE-2023-52707](https://nvd.nist.gov/vuln/detail/CVE-2023-52707){: external}, [CVE-2023-52730](https://nvd.nist.gov/vuln/detail/CVE-2023-52730){: external}, [CVE-2023-52756](https://nvd.nist.gov/vuln/detail/CVE-2023-52756){: external}, [CVE-2023-52762](https://nvd.nist.gov/vuln/detail/CVE-2023-52762){: external}, [CVE-2023-52764](https://nvd.nist.gov/vuln/detail/CVE-2023-52764){: external}, [CVE-2023-52775](https://nvd.nist.gov/vuln/detail/CVE-2023-52775){: external}, [CVE-2023-52777](https://nvd.nist.gov/vuln/detail/CVE-2023-52777){: external}, [CVE-2023-52784](https://nvd.nist.gov/vuln/detail/CVE-2023-52784){: external}, [CVE-2023-52791](https://nvd.nist.gov/vuln/detail/CVE-2023-52791){: external}, [CVE-2023-52796](https://nvd.nist.gov/vuln/detail/CVE-2023-52796){: external}, [CVE-2023-52803](https://nvd.nist.gov/vuln/detail/CVE-2023-52803){: external}, [CVE-2023-52811](https://nvd.nist.gov/vuln/detail/CVE-2023-52811){: external}, [CVE-2023-52832](https://nvd.nist.gov/vuln/detail/CVE-2023-52832){: external}, [CVE-2023-52834](https://nvd.nist.gov/vuln/detail/CVE-2023-52834){: external}, [CVE-2023-52845](https://nvd.nist.gov/vuln/detail/CVE-2023-52845){: external}, [CVE-2023-52847](https://nvd.nist.gov/vuln/detail/CVE-2023-52847){: external}, [CVE-2023-52864](https://nvd.nist.gov/vuln/detail/CVE-2023-52864){: external}, [CVE-2024-21823](https://nvd.nist.gov/vuln/detail/CVE-2024-21823){: external}, [CVE-2024-2201](https://nvd.nist.gov/vuln/detail/CVE-2024-2201){: external}, [CVE-2024-25739](https://nvd.nist.gov/vuln/detail/CVE-2024-25739){: external}, [CVE-2024-26586](https://nvd.nist.gov/vuln/detail/CVE-2024-26586){: external}, [CVE-2024-26614](https://nvd.nist.gov/vuln/detail/CVE-2024-26614){: external}, [CVE-2024-26640](https://nvd.nist.gov/vuln/detail/CVE-2024-26640){: external}, [CVE-2024-26660](https://nvd.nist.gov/vuln/detail/CVE-2024-26660){: external}, [CVE-2024-26669](https://nvd.nist.gov/vuln/detail/CVE-2024-26669){: external}, [CVE-2024-26686](https://nvd.nist.gov/vuln/detail/CVE-2024-26686){: external}, [CVE-2024-26698](https://nvd.nist.gov/vuln/detail/CVE-2024-26698){: external}, [CVE-2024-26704](https://nvd.nist.gov/vuln/detail/CVE-2024-26704){: external}, [CVE-2024-26733](https://nvd.nist.gov/vuln/detail/CVE-2024-26733){: external}, [CVE-2024-26740](https://nvd.nist.gov/vuln/detail/CVE-2024-26740){: external}, [CVE-2024-26772](https://nvd.nist.gov/vuln/detail/CVE-2024-26772){: external}, [CVE-2024-26773](https://nvd.nist.gov/vuln/detail/CVE-2024-26773){: external}, [CVE-2024-26802](https://nvd.nist.gov/vuln/detail/CVE-2024-26802){: external}, [CVE-2024-26810](https://nvd.nist.gov/vuln/detail/CVE-2024-26810){: external}, [CVE-2024-26837](https://nvd.nist.gov/vuln/detail/CVE-2024-26837){: external}, [CVE-2024-26840](https://nvd.nist.gov/vuln/detail/CVE-2024-26840){: external}, [CVE-2024-26843](https://nvd.nist.gov/vuln/detail/CVE-2024-26843){: external}, [CVE-2024-26852](https://nvd.nist.gov/vuln/detail/CVE-2024-26852){: external}, [CVE-2024-26853](https://nvd.nist.gov/vuln/detail/CVE-2024-26853){: external}, [CVE-2024-26870](https://nvd.nist.gov/vuln/detail/CVE-2024-26870){: external}, [CVE-2024-26878](https://nvd.nist.gov/vuln/detail/CVE-2024-26878){: external}, [CVE-2024-26908](https://nvd.nist.gov/vuln/detail/CVE-2024-26908){: external}, [CVE-2024-26921](https://nvd.nist.gov/vuln/detail/CVE-2024-26921){: external}, [CVE-2024-26925](https://nvd.nist.gov/vuln/detail/CVE-2024-26925){: external}, [CVE-2024-26940](https://nvd.nist.gov/vuln/detail/CVE-2024-26940){: external}, [CVE-2024-26958](https://nvd.nist.gov/vuln/detail/CVE-2024-26958){: external}, [CVE-2024-26960](https://nvd.nist.gov/vuln/detail/CVE-2024-26960){: external}, [CVE-2024-26961](https://nvd.nist.gov/vuln/detail/CVE-2024-26961){: external}, [CVE-2024-27010](https://nvd.nist.gov/vuln/detail/CVE-2024-27010){: external}, [CVE-2024-27011](https://nvd.nist.gov/vuln/detail/CVE-2024-27011){: external}, [CVE-2024-27019](https://nvd.nist.gov/vuln/detail/CVE-2024-27019){: external}, [CVE-2024-27020](https://nvd.nist.gov/vuln/detail/CVE-2024-27020){: external}, [CVE-2024-27025](https://nvd.nist.gov/vuln/detail/CVE-2024-27025){: external}, [CVE-2024-27065](https://nvd.nist.gov/vuln/detail/CVE-2024-27065){: external}, [CVE-2024-27388](https://nvd.nist.gov/vuln/detail/CVE-2024-27388){: external}, [CVE-2024-27395](https://nvd.nist.gov/vuln/detail/CVE-2024-27395){: external}, [CVE-2024-27434](https://nvd.nist.gov/vuln/detail/CVE-2024-27434){: external}, [CVE-2024-31076](https://nvd.nist.gov/vuln/detail/CVE-2024-31076){: external}, [CVE-2024-33621](https://nvd.nist.gov/vuln/detail/CVE-2024-33621){: external}, [CVE-2024-35790](https://nvd.nist.gov/vuln/detail/CVE-2024-35790){: external}, [CVE-2024-35801](https://nvd.nist.gov/vuln/detail/CVE-2024-35801){: external}, [CVE-2024-35807](https://nvd.nist.gov/vuln/detail/CVE-2024-35807){: external}, [CVE-2024-35810](https://nvd.nist.gov/vuln/detail/CVE-2024-35810){: external}, [CVE-2024-35814](https://nvd.nist.gov/vuln/detail/CVE-2024-35814){: external}, [CVE-2024-35823](https://nvd.nist.gov/vuln/detail/CVE-2024-35823){: external}, [CVE-2024-35824](https://nvd.nist.gov/vuln/detail/CVE-2024-35824){: external}, [CVE-2024-35847](https://nvd.nist.gov/vuln/detail/CVE-2024-35847){: external}, [CVE-2024-35876](https://nvd.nist.gov/vuln/detail/CVE-2024-35876){: external}, [CVE-2024-35893](https://nvd.nist.gov/vuln/detail/CVE-2024-35893){: external}, [CVE-2024-35896](https://nvd.nist.gov/vuln/detail/CVE-2024-35896){: external}, [CVE-2024-35897](https://nvd.nist.gov/vuln/detail/CVE-2024-35897){: external}, [CVE-2024-35899](https://nvd.nist.gov/vuln/detail/CVE-2024-35899){: external}, [CVE-2024-35900](https://nvd.nist.gov/vuln/detail/CVE-2024-35900){: external}, [CVE-2024-35910](https://nvd.nist.gov/vuln/detail/CVE-2024-35910){: external}, [CVE-2024-35912](https://nvd.nist.gov/vuln/detail/CVE-2024-35912){: external}, [CVE-2024-35924](https://nvd.nist.gov/vuln/detail/CVE-2024-35924){: external}, [CVE-2024-35925](https://nvd.nist.gov/vuln/detail/CVE-2024-35925){: external}, [CVE-2024-35930](https://nvd.nist.gov/vuln/detail/CVE-2024-35930){: external}, [CVE-2024-35937](https://nvd.nist.gov/vuln/detail/CVE-2024-35937){: external}, [CVE-2024-35938](https://nvd.nist.gov/vuln/detail/CVE-2024-35938){: external}, [CVE-2024-35946](https://nvd.nist.gov/vuln/detail/CVE-2024-35946){: external}, [CVE-2024-35947](https://nvd.nist.gov/vuln/detail/CVE-2024-35947){: external}, [CVE-2024-35952](https://nvd.nist.gov/vuln/detail/CVE-2024-35952){: external}, [CVE-2024-36000](https://nvd.nist.gov/vuln/detail/CVE-2024-36000){: external}, [CVE-2024-36005](https://nvd.nist.gov/vuln/detail/CVE-2024-36005){: external}, [CVE-2024-36006](https://nvd.nist.gov/vuln/detail/CVE-2024-36006){: external}, [CVE-2024-36010](https://nvd.nist.gov/vuln/detail/CVE-2024-36010){: external}, [CVE-2024-36016](https://nvd.nist.gov/vuln/detail/CVE-2024-36016){: external}, [CVE-2024-36017](https://nvd.nist.gov/vuln/detail/CVE-2024-36017){: external}, [CVE-2024-36020](https://nvd.nist.gov/vuln/detail/CVE-2024-36020){: external}, [CVE-2024-36025](https://nvd.nist.gov/vuln/detail/CVE-2024-36025){: external}, [CVE-2024-36270](https://nvd.nist.gov/vuln/detail/CVE-2024-36270){: external}, [CVE-2024-36286](https://nvd.nist.gov/vuln/detail/CVE-2024-36286){: external}, [CVE-2024-36489](https://nvd.nist.gov/vuln/detail/CVE-2024-36489){: external}, [CVE-2024-36886](https://nvd.nist.gov/vuln/detail/CVE-2024-36886){: external}, [CVE-2024-36889](https://nvd.nist.gov/vuln/detail/CVE-2024-36889){: external}, [CVE-2024-36896](https://nvd.nist.gov/vuln/detail/CVE-2024-36896){: external}, [CVE-2024-36904](https://nvd.nist.gov/vuln/detail/CVE-2024-36904){: external}, [CVE-2024-36905](https://nvd.nist.gov/vuln/detail/CVE-2024-36905){: external}, [CVE-2024-36917](https://nvd.nist.gov/vuln/detail/CVE-2024-36917){: external}, [CVE-2024-36921](https://nvd.nist.gov/vuln/detail/CVE-2024-36921){: external}, [CVE-2024-36927](https://nvd.nist.gov/vuln/detail/CVE-2024-36927){: external}, [CVE-2024-36929](https://nvd.nist.gov/vuln/detail/CVE-2024-36929){: external}, [CVE-2024-36933](https://nvd.nist.gov/vuln/detail/CVE-2024-36933){: external}, [CVE-2024-36940](https://nvd.nist.gov/vuln/detail/CVE-2024-36940){: external}, [CVE-2024-36941](https://nvd.nist.gov/vuln/detail/CVE-2024-36941){: external}, [CVE-2024-36945](https://nvd.nist.gov/vuln/detail/CVE-2024-36945){: external}, [CVE-2024-36950](https://nvd.nist.gov/vuln/detail/CVE-2024-36950){: external}, [CVE-2024-36954](https://nvd.nist.gov/vuln/detail/CVE-2024-36954){: external}, [CVE-2024-36960](https://nvd.nist.gov/vuln/detail/CVE-2024-36960){: external}, [CVE-2024-36971](https://nvd.nist.gov/vuln/detail/CVE-2024-36971){: external}, [CVE-2024-36978](https://nvd.nist.gov/vuln/detail/CVE-2024-36978){: external}, [CVE-2024-36979](https://nvd.nist.gov/vuln/detail/CVE-2024-36979){: external}, [CVE-2024-38538](https://nvd.nist.gov/vuln/detail/CVE-2024-38538){: external}, [CVE-2024-38555](https://nvd.nist.gov/vuln/detail/CVE-2024-38555){: external}, [CVE-2024-38573](https://nvd.nist.gov/vuln/detail/CVE-2024-38573){: external}, [CVE-2024-38575](https://nvd.nist.gov/vuln/detail/CVE-2024-38575){: external}, [CVE-2024-38596](https://nvd.nist.gov/vuln/detail/CVE-2024-38596){: external}, [CVE-2024-38598](https://nvd.nist.gov/vuln/detail/CVE-2024-38598){: external}, [CVE-2024-38615](https://nvd.nist.gov/vuln/detail/CVE-2024-38615){: external}, [CVE-2024-38627](https://nvd.nist.gov/vuln/detail/CVE-2024-38627){: external}, [CVE-2024-39276](https://nvd.nist.gov/vuln/detail/CVE-2024-39276){: external}, [CVE-2024-39472](https://nvd.nist.gov/vuln/detail/CVE-2024-39472){: external}, [CVE-2024-39476](https://nvd.nist.gov/vuln/detail/CVE-2024-39476){: external}, [CVE-2024-39487](https://nvd.nist.gov/vuln/detail/CVE-2024-39487){: external}, [CVE-2024-39502](https://nvd.nist.gov/vuln/detail/CVE-2024-39502){: external}, [CVE-2024-40927](https://nvd.nist.gov/vuln/detail/CVE-2024-40927){: external}, [CVE-2024-40974](https://nvd.nist.gov/vuln/detail/CVE-2024-40974){: external}, [RHSA-2024:3043](https://access.redhat.com/errata/RHSA-2024:3043){: external}, [CVE-2024-0690](https://nvd.nist.gov/vuln/detail/CVE-2024-0690){: external}. |
| GPU device plug-in and installer | 47ed2ef |4bd77eb| Updates for [CVE-2019-11236](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2019-11236){: external},[CVE-2019-20916](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2019-20916){: external},[CVE-2020-26137](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2020-26137){: external},[CVE-2021-3572](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2021-3572){: external}, [CVE-2022-40897](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2022-40897){: external}, [CVE-2023-32681](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-32681){: external}, [CVE-2023-43804](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-43804){: external}, [CVE-2023-45803](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-45803){: external}, [CVE-2024-37891](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-37891){: external}, [CVE-2024-6345](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-6345){: external}, [CVE-2023-52803](https://nvd.nist.gov/vuln/detail/CVE-2023-52803){: external}. |
{: caption="Changes since version 1.27.15_1588" caption-side="bottom"}


### Master fix pack 1.27.16_1587, released 31 July 2024
{: #12716_1587_M}

The following table shows the changes that are in the master fix pack 1.27.16_1587. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.4.11 | v1.5.7 | New version contains updates and security fixes. |
| etcd | v3.5.13 | v3.5.14 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.14){: external}. |
| GPU device plug-in and installer | 10ea2b1 | 184b5e2 | New version contains updates and security fixes. |
| {{site.data.keyword.IBM_notm}} Calico extension | 1595 | 1598 | New version contains security fixes. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.4.20 | v2.4.23 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 443 | 445 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 14d0ab5 | 312030f | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.11 | v2.8.12 | New version contains updates and security fixes. |
| Kubernetes | v1.27.15 | v1.27.16 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.16){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2933 | 2967 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.16 | v0.13.17 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.17){: external}. |
{: caption="Changes since version 1.27.15_1581" caption-side="bottom"}


### Worker node fix pack 1.27.15_1588, released 29 July 2024
{: #12715_1588_W}

The following table shows the changes that are in the worker node fix pack 1.27.15_1588. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-189-generic | 5.4.0-190-generic | Worker node kernel & package updates for [CVE-2022-48655](https://nvd.nist.gov/vuln/detail/CVE-2022-48655){: external}, [CVE-2024-0760](https://nvd.nist.gov/vuln/detail/CVE-2024-0760){: external}, [CVE-2024-1737](https://nvd.nist.gov/vuln/detail/CVE-2024-1737){: external}, [CVE-2024-1975](https://nvd.nist.gov/vuln/detail/CVE-2024-1975){: external}, [CVE-2024-26583](https://nvd.nist.gov/vuln/detail/CVE-2024-26583){: external}, [CVE-2024-26584](https://nvd.nist.gov/vuln/detail/CVE-2024-26584){: external}, [CVE-2024-26585](https://nvd.nist.gov/vuln/detail/CVE-2024-26585){: external}, [CVE-2024-26907](https://nvd.nist.gov/vuln/detail/CVE-2024-26907){: external}, [CVE-2024-36016](https://nvd.nist.gov/vuln/detail/CVE-2024-36016){: external}, [CVE-2024-4076](https://nvd.nist.gov/vuln/detail/CVE-2024-4076){: external}, [CVE-2024-5569](https://nvd.nist.gov/vuln/detail/CVE-2024-5569){: external}. |
| Containerd | 1.7.19 | 1.7.20 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.20){: external}. |
| Kubernetes | N/A | N/A | N/A |
| GPU device plug-in and installer | 184b5e2 | 47ed2ef | Security fixes for [CVE-2024-4032](https://nvd.nist.gov/vuln/detail/CVE-2024-4032){: external}. |
| Haproxy | N/A | N/A | N/A |
{: caption="Changes since version 1.27.15_1584" caption-side="bottom"}


### Worker node fix pack 1.27.15_1584, released 15 July 2024
{: #12715_1584_W}

The following table shows the changes that are in the worker node fix pack 1.27.15_1584. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-187-generic | 5.4.0-189-generic | Worker node kernel & package updates for [CVE-2023-6270](https://nvd.nist.gov/vuln/detail/CVE-2023-6270){: external}, [CVE-2023-6597](https://nvd.nist.gov/vuln/detail/CVE-2023-6597){: external}, [CVE-2024-0450](https://nvd.nist.gov/vuln/detail/CVE-2024-0450){: external}, [CVE-2024-2201](https://nvd.nist.gov/vuln/detail/CVE-2024-2201){: external}, [CVE-2024-23307](https://nvd.nist.gov/vuln/detail/CVE-2024-23307){: external}, [CVE-2024-24861](https://nvd.nist.gov/vuln/detail/CVE-2024-24861){: external}, [CVE-2024-26586](https://nvd.nist.gov/vuln/detail/CVE-2024-26586){: external}, [CVE-2024-26642](https://nvd.nist.gov/vuln/detail/CVE-2024-26642){: external}, [CVE-2024-26643](https://nvd.nist.gov/vuln/detail/CVE-2024-26643){: external}, [CVE-2024-26828](https://nvd.nist.gov/vuln/detail/CVE-2024-26828){: external}, [CVE-2024-26889](https://nvd.nist.gov/vuln/detail/CVE-2024-26889){: external}, [CVE-2024-26922](https://nvd.nist.gov/vuln/detail/CVE-2024-26922){: external}, [CVE-2024-26923](https://nvd.nist.gov/vuln/detail/CVE-2024-26923){: external}, [CVE-2024-26925](https://nvd.nist.gov/vuln/detail/CVE-2024-26925){: external}, [CVE-2024-26926](https://nvd.nist.gov/vuln/detail/CVE-2024-26926){: external}. |
| Containerd | 1.7.18 | 1.7.19 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.19){: external}. |
| HAProxy | e77d4ca | c91c765 | Security fixes for [CVE-2024-28182](https://nvd.nist.gov/vuln/detail/CVE-2023-2953){: external},[CVE-2024-25062](https://nvd.nist.gov/vuln/detail/CVE-2024-28182){: external}. |
{: caption="Changes since version 1.27.15_1583" caption-side="bottom"}


### Worker node fix pack 1.27.15_1583, released 09 July 2024
{: #12715_1583_W}

The following table shows the changes that are in the worker node fix pack 1.27.15_1583. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-186-generic | 5.4.0-187-generic | Worker node kernel & package updates for [CVE-2022-4968](https://nvd.nist.gov/vuln/detail/CVE-2022-4968){: external}, [CVE-2024-2201](https://nvd.nist.gov/vuln/detail/CVE-2024-2201){: external}, [CVE-2024-26643](https://nvd.nist.gov/vuln/detail/CVE-2024-26643){: external}, [CVE-2024-26925](https://nvd.nist.gov/vuln/detail/CVE-2024-26925){: external}, [CVE-2024-32002](https://nvd.nist.gov/vuln/detail/CVE-2024-32002){: external}, [CVE-2024-38428](https://nvd.nist.gov/vuln/detail/CVE-2024-38428){: external}. |
| HAProxy | 18889dd | e77d4ca | New version contains security fixes |
| GPU device plug-in and installer | 8ef78ef | fbdf629 | New version contains updates and security fixes. |
{: caption="Changes since version 1.27.15_1582" caption-side="bottom"}


### Master fix pack 1.27.15_1581, released 19 June 2024
{: #12715_1581_M}

The following table shows the changes that are in the master fix pack 1.27.15_1581. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.4.10 | v1.4.11 | New version contains updates and security fixes. |
| GPU device plug-in and installer | 9fad43c | 10ea2b1 | New version contains updates and security fixes. |
| {{site.data.keyword.IBM_notm}} Calico extension | 1589 | 1595 | New version contains security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | 0281c94 | 48787be | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 4c5d156 | 14d0ab5 | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.10 | v2.8.11 | New version contains updates and security fixes. |
| Kubernetes | v1.27.14 | v1.27.15 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.15){: external}. |
| Kubernetes NodeLocal DNS cache | 1.23.0 | 1.23.1 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.23.1){: external}. |
| Portieris admission controller | v0.13.15 | v0.13.16 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.16){: external}. |
{: caption="Changes since version 1.27.14_1577" caption-side="bottom"}


### Worker node fix pack 1.27.15_1582, released 18 June 2024
{: #12715_1582_W}

The following table shows the changes that are in the worker node fix pack 1.27.15_1582. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-182-generic | 5.4.0-186-generic | Worker node kernel and package updates [CVE-2021-47063](https://nvd.nist.gov/vuln/detail/CVE-2021-47063){: external}, [CVE-2021-47070](https://nvd.nist.gov/vuln/detail/CVE-2021-47070){: external}, [CVE-2023-47233](https://nvd.nist.gov/vuln/detail/CVE-2023-47233){: external}, [CVE-2023-52530](https://nvd.nist.gov/vuln/detail/CVE-2023-52530){: external}, [CVE-2024-26614](https://nvd.nist.gov/vuln/detail/CVE-2024-26614){: external}, [CVE-2024-26622](https://nvd.nist.gov/vuln/detail/CVE-2024-26622){: external}, [CVE-2024-26712](https://nvd.nist.gov/vuln/detail/CVE-2024-26712){: external}, [CVE-2024-26733](https://nvd.nist.gov/vuln/detail/CVE-2024-26733){: external}, CIS benchmark compliance: [1.5.4](https://workbench.cisecurity.org/sections/1985936/recommendations/3181745){: external}, [1.5.5](https://workbench.cisecurity.org/sections/1985936/recommendations/3181749){: external}, [4.5.5](https://workbench.cisecurity.org/sections/1985957/recommendations/3181909){: external}, [3.3.4](https://workbench.cisecurity.org/sections/1985946/recommendations/3181810){: external}, [3.3.9](https://workbench.cisecurity.org/sections/1985946/recommendations/3181824){: external}, [1.1.1.2](https://workbench.cisecurity.org/sections/1985904/recommendations/3181628){: external}, [1.1.1.3](https://workbench.cisecurity.org/sections/1985904/recommendations/3181629){: external}, [1.1.1.4](https://workbench.cisecurity.org/sections/1985904/recommendations/3181631){: external}, [1.1.1.5](https://workbench.cisecurity.org/sections/1985904/recommendations/3181633){: external}. |
| Kubernetes | 1.27.14 | 1.27.15 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.27.md){: external}. |
| Containerd | 1.7.17 | 1.7.18 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.18){: external}. |
| HAProxy | 0062a3c | 18889dd | Security fixes for [CVE-2024-25062](https://nvd.nist.gov/vuln/detail/CVE-2024-25062){: external}. |
{: caption="Changes since version 1.27.14_1578" caption-side="bottom"}


### Worker node fix pack 1.27.14_1578, released 03 June 2024
{: #12714_1578_W}

The following table shows the changes that are in the worker node fix pack 1.27.14_1578. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-182-generic | 5.4.0-182-generic | Worker node package updates [CVE-2023-22745](https://nvd.nist.gov/vuln/detail/CVE-2023-22745){: external}, [CVE-2024-32004](https://nvd.nist.gov/vuln/detail/CVE-2024-32004){: external}, [CVE-2024-32020](https://nvd.nist.gov/vuln/detail/CVE-2024-32020){: external}, [CVE-2024-32021](https://nvd.nist.gov/vuln/detail/CVE-2024-32021){: external}, [CVE-2024-32465](https://nvd.nist.gov/vuln/detail/CVE-2024-32465){: external}, [CVE-2024-33599](https://nvd.nist.gov/vuln/detail/CVE-2024-33599){: external}, [CVE-2024-33600](https://nvd.nist.gov/vuln/detail/CVE-2024-33600){: external}, [CVE-2024-33601](https://nvd.nist.gov/vuln/detail/CVE-2024-33601){: external}, [CVE-2024-33602](https://nvd.nist.gov/vuln/detail/CVE-2024-33602){: external}, [CVE-2024-34064](https://nvd.nist.gov/vuln/detail/CVE-2024-34064){: external}, [CVE-2024-3651](https://nvd.nist.gov/vuln/detail/CVE-2024-3651){: external}. |
| Kubernetes | 1.27.13 | 1.27.14 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.27.md){: external}. |
| Containerd | 1.7.17 | 1.7.17 | N/A |
| HAProxy | e88695e | 0062a3c | Security fixes for [CVE-2024-0450](https://nvd.nist.gov/vuln/detail/CVE-2024-0450){: external}, [CVE-2024-33599](https://nvd.nist.gov/vuln/detail/CVE-2024-33599){: external}, [CVE-2024-26461](https://nvd.nist.gov/vuln/detail/CVE-2024-26461){: external}, [CVE-2021-43618](https://nvd.nist.gov/vuln/detail/CVE-2021-43618){: external}, [CVE-2024-22365](https://nvd.nist.gov/vuln/detail/CVE-2024-22365){: external}, [CVE-2023-6597](https://nvd.nist.gov/vuln/detail/CVE-2023-6597){: external}, [CVE-2024-26458](https://nvd.nist.gov/vuln/detail/CVE-2024-26458){: external}, [CVE-2024-2961](https://nvd.nist.gov/vuln/detail/CVE-2024-2961){: external}, [CVE-2024-33601](https://nvd.nist.gov/vuln/detail/CVE-2024-33601){: external}, [CVE-2024-33602](https://nvd.nist.gov/vuln/detail/CVE-2024-33602){: external}, [CVE-2023-7008](https://nvd.nist.gov/vuln/detail/CVE-2023-7008){: external}, [CVE-2023-6004](https://nvd.nist.gov/vuln/detail/CVE-2023-6004){: external}, [CVE-2023-6918](https://nvd.nist.gov/vuln/detail/CVE-2023-6918){: external}, [CVE-2024-33600](https://nvd.nist.gov/vuln/detail/CVE-2024-33600){: external}. |
{: caption="Changes since version 1.27.13_1575" caption-side="bottom"}


### Master fix pack 1.27.14_1577, released 29 May 2024
{: #12714_1577_M}

The following table shows the changes that are in the master fix pack 1.27.14_1577. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.26.4 | v3.27.2 | See the [Calico release notes](https://archive-os-3-27.netlify.app/calico/3.27/release-notes/#v3.27.2){: external}. |
| Cluster health image | v1.4.9 | v1.4.10 | New version contains updates and security fixes. |
| GPU device plug-in and installer | 206b5a6 | 9fad43c | New version contains updates and security fixes. |
| {{site.data.keyword.IBM_notm}} Calico extension | 1537 | 1589 | New version contains security fixes. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.4.19 | v2.4.20 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.12-10 | v1.27.14-1 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 442 | 443 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | 50808cc | 0281c94 | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.9 | v2.8.10 | New version contains updates and security fixes. |
| Konnectivity agent and server | v0.1.5_47_iks | v0.1.9_105_iks | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.1.9){: external}. |
| Kubernetes | v1.27.13 | v1.27.14 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.14){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2867 | 2933 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.13 | v0.13.15 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.15){: external}. |
{: caption="Changes since version 1.27.13_1572" caption-side="bottom"}


### Worker node fix pack 1.27.13_1575, released 23 May 2024
{: #12713_1575_W}

The following table shows the changes that are in the worker node fix pack 1.27.13_1575. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-177-generic | 5.4.0-182-generic | Worker node package and kernel updates [CVE-2016-9840](https://nvd.nist.gov/vuln/detail/CVE-2016-9840){: external}, [CVE-2016-9841](https://nvd.nist.gov/vuln/detail/CVE-2016-9841){: external}, [CVE-2018-25032](https://nvd.nist.gov/vuln/detail/CVE-2018-25032){: external}, [CVE-2022-37434](https://nvd.nist.gov/vuln/detail/CVE-2022-37434){: external}, [CVE-2023-23000](https://nvd.nist.gov/vuln/detail/CVE-2023-23000){: external}, [CVE-2023-23004](https://nvd.nist.gov/vuln/detail/CVE-2023-23004){: external}, [CVE-2023-24023](https://nvd.nist.gov/vuln/detail/CVE-2023-24023){: external}, [CVE-2023-4421](https://nvd.nist.gov/vuln/detail/CVE-2023-4421){: external}, [CVE-2023-46838](https://nvd.nist.gov/vuln/detail/CVE-2023-46838){: external}, [CVE-2023-52600](https://nvd.nist.gov/vuln/detail/CVE-2023-52600){: external}, [CVE-2023-52603](https://nvd.nist.gov/vuln/detail/CVE-2023-52603){: external}, [CVE-2023-5388](https://nvd.nist.gov/vuln/detail/CVE-2023-5388){: external}, [CVE-2023-6135](https://nvd.nist.gov/vuln/detail/CVE-2023-6135){: external}, [CVE-2024-0607](https://nvd.nist.gov/vuln/detail/CVE-2024-0607){: external}, [CVE-2024-1086](https://nvd.nist.gov/vuln/detail/CVE-2024-1086){: external}, [CVE-2024-23851](https://nvd.nist.gov/vuln/detail/CVE-2024-23851){: external}, [CVE-2024-24855](https://nvd.nist.gov/vuln/detail/CVE-2024-24855){: external}, [CVE-2024-26581](https://nvd.nist.gov/vuln/detail/CVE-2024-26581){: external}, [CVE-2024-26589](https://nvd.nist.gov/vuln/detail/CVE-2024-26589){: external}, [CVE-2024-28085](https://nvd.nist.gov/vuln/detail/CVE-2024-28085){: external}, [CVE-2024-28834](https://nvd.nist.gov/vuln/detail/CVE-2024-28834){: external}, [CVE-2024-2961](https://nvd.nist.gov/vuln/detail/CVE-2024-2961){: external}, CIS benchmark compliance: [4.5.1.6](https://workbench.cisecurity.org/sections/1985958/recommendations/3181904){: external}, [4.5.1.7](https://workbench.cisecurity.org/sections/1985958/recommendations/3181905){: external}, [4.5.7](https://workbench.cisecurity.org/sections/1985957/recommendations/3181911){: external}. |
| Kubernetes | 1.27.13 | 1.27.13 | N/A |
| Containerd | 1.7.16 | 1.7.17 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.17){: external}. |
| HAProxy | d225100 | 4e826da | [CVE-2024-2961](https://nvd.nist.gov/vuln/detail/CVE-2024-2961){: external}, [CVE-2024-28834](https://nvd.nist.gov/vuln/detail/CVE-2024-28834){: external}. |
{: caption="Changes since version 1.27.13_1574" caption-side="bottom"}


### Worker node fix pack 1.27.13_1574, released 06 May 2024
{: #12713_1574_W}

The following table shows the changes that are in the worker node fix pack 1.27.13_1574. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-177-generic | 5.4.0-177-generic | Worker node package updates for [CVE-2015-1197](https://nvd.nist.gov/vuln/detail/CVE-2015-1197){: external}, [CVE-2023-7207](https://nvd.nist.gov/vuln/detail/CVE-2023-7207){: external}, [CVE-2024-28182](https://nvd.nist.gov/vuln/detail/CVE-2024-28182){: external}, [CVE-2024-32487](https://nvd.nist.gov/vuln/detail/CVE-2024-32487){: external}. CIS benchmark compliance: [1.1.2.1](https://workbench.cisecurity.org/sections/1985909/recommendations/3181638){: external}, [1.1.2.2](https://workbench.cisecurity.org/sections/1985909/recommendations/3181639){: external}, [1.1.2.3](https://workbench.cisecurity.org/sections/1985909/recommendations/3181640){: external}, and [1.1.2.4](https://workbench.cisecurity.org/sections/1985909/recommendations/3181642){: external}.  |
| Kubernetes | 1.27.13 | 1.27.13 | N/A |
| Containerd | 1.7.15 | 1.7.16 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.16){: external}. |
| HAProxy | 295dba8 | 295dba8 | N/A |
| GPU device plug-in and installer | 9fad43c | 806184d | Security fixes for [CVE-2022-48554](https://nvd.nist.gov/vuln/detail/CVE-2022-48554){: external}, [CVE-2023-2975](https://nvd.nist.gov/vuln/detail/CVE-2023-2975){: external}, [CVE-2023-3446](https://nvd.nist.gov/vuln/detail/CVE-2023-3446){: external}, [CVE-2023-5678](https://nvd.nist.gov/vuln/detail/CVE-2023-5678){: external}, [CVE-2024-22365](https://nvd.nist.gov/vuln/detail/CVE-2024-22365){: external}, [CVE-2023-7008](https://nvd.nist.gov/vuln/detail/CVE-2023-7008){: external}, [CVE-2023-3817](https://nvd.nist.gov/vuln/detail/CVE-2023-3817){: external}, [CVE-2023-6129](https://nvd.nist.gov/vuln/detail/CVE-2023-6129){: external}, [CVE-2023-6237](https://nvd.nist.gov/vuln/detail/CVE-2023-6237){: external}, [CVE-2024-0727](https://nvd.nist.gov/vuln/detail/CVE-2024-0727){: external}. |
{: caption="Changes since version 1.27.13_1573" caption-side="bottom"}


### Master fix pack 1.27.13_1572, released 24 April 2024
{: #12713_1572_M}

The following table shows the changes that are in the master fix pack 1.27.13_1572. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.4.8 | v1.4.9 | New version contains updates and security fixes. |
| etcd | v3.5.12 | v3.5.13 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.13){: external}. |
| GPU device plug-in and installer | 71cb7f7 | 206b5a6 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.12-1 | v1.27.12-10 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | 803912f | 50808cc | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | bd30030 | 4c5d156 | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.8 | v2.8.9 | New version contains updates and security fixes. |
| Kubernetes | v1.27.12 | v1.27.13 | Update resolves [CVE-2024-3177](https://nvd.nist.gov/vuln/detail/CVE-2024-3177). For more information, see the [Security Bulletin](https://www.ibm.com/support/pages/node/7148966){: external} and the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.13){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2831 | 2867 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.12 | v0.13.13 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.13){: external}. |
{: caption="Changes since version 1.27.12_1569" caption-side="bottom"}


### Worker node fix pack 1.27.13_1573, released 22 April 2024
{: #12713_1573_W}

The following table shows the changes that are in the worker node fix pack 1.27.13_1573. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-174-generic | 5.4.0-177-generic | Worker node and kernel package updates for [CVE-2016-9840](https://nvd.nist.gov/vuln/detail/CVE-2016-9840){: external}, [CVE-2016-9841](https://nvd.nist.gov/vuln/detail/CVE-2016-9841){: external}, [CVE-2018-25032](https://nvd.nist.gov/vuln/detail/CVE-2018-25032){: external}, [CVE-2022-37434](https://nvd.nist.gov/vuln/detail/CVE-2022-37434){: external}, [CVE-2023-23000](https://nvd.nist.gov/vuln/detail/CVE-2023-23000){: external}, [CVE-2023-23004](https://nvd.nist.gov/vuln/detail/CVE-2023-23004){: external}, [CVE-2023-24023](https://nvd.nist.gov/vuln/detail/CVE-2023-24023){: external}, [CVE-2023-4421](https://nvd.nist.gov/vuln/detail/CVE-2023-4421){: external}, [CVE-2023-46838](https://nvd.nist.gov/vuln/detail/CVE-2023-46838){: external}, [CVE-2023-52600](https://nvd.nist.gov/vuln/detail/CVE-2023-52600){: external}, [CVE-2023-52603](https://nvd.nist.gov/vuln/detail/CVE-2023-52603){: external}, [CVE-2023-5388](https://nvd.nist.gov/vuln/detail/CVE-2023-5388){: external}, [CVE-2023-6135](https://nvd.nist.gov/vuln/detail/CVE-2023-6135){: external}, [CVE-2024-0607](https://nvd.nist.gov/vuln/detail/CVE-2024-0607){: external}, [CVE-2024-1086](https://nvd.nist.gov/vuln/detail/CVE-2024-1086){: external}, [CVE-2024-23851](https://nvd.nist.gov/vuln/detail/CVE-2024-23851){: external}, [CVE-2024-24855](https://nvd.nist.gov/vuln/detail/CVE-2024-24855){: external}, [CVE-2024-26581](https://nvd.nist.gov/vuln/detail/CVE-2024-26581){: external}, [CVE-2024-26589](https://nvd.nist.gov/vuln/detail/CVE-2024-26589){: external}, [CVE-2024-28085](https://nvd.nist.gov/vuln/detail/CVE-2024-28085){: external}, [CVE-2024-28834](https://nvd.nist.gov/vuln/detail/CVE-2024-28834){: external}, [CVE-2024-2961](https://nvd.nist.gov/vuln/detail/CVE-2024-2961){: external}. |
| Kubernetes | 1.27.12 | 1.27.13 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.27.md){: external}. |
| Containerd | 1.7.13 | 1.7.15 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.15){: external}. |
| HAProxy | 295dba8 | 4e826da | Security fixes for [CVE-2024-28834](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-28834){: external}. |
| GPU device plug-in and installer | 206b5a6 | 9fad43c1 | Security fixes for [CVE-2024-1488](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-1488){: external}, [CVE-2024-28834](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-28834){: external}, [CVE-2024-28835](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2024-28835){: external}. |
{: caption="Changes since version 1.27.12_1571" caption-side="bottom"}


### Worker node fix pack 1.27.12_1571, released 8 April 2024
{: #12712_1571_W}

The following table shows the changes that are in the worker node fix pack 1.27.12_1571. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-174-generic | 5.4.0-174-generic | Worker node package updates for [CVE-2024-2398](https://nvd.nist.gov/vuln/detail/CVE-2024-2398){: external}, [CVE-2024-28085](https://nvd.nist.gov/vuln/detail/CVE-2024-28085){: external}. |
| Kubernetes | 1.27.12 | 1.27.12 | N/A |
| Containerd | 1.7.14 | 1.7.13 | Reverted due to a [bug](https://github.com/containerd/containerd/issues/10036){: external}. |
| HAProxy | 512b32a | 295dba8 | Security fixes for [CVE-2023-28322](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-28322){: external}, [CVE-2023-38546](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-38546){: external}, [CVE-2023-46218](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-46218){: external}, [CVE-2023-52425](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-52425){: external}
| GPU device plug-in and installer | 5b69345 | 206b5a6 | Security fixes for [CVE-2023-28322](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-28322){: external}, [CVE-2023-38546](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-38546){: external}, [CVE-2023-46218](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-46218){: external}, [CVE-2023-52425](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-52425){: external}
{: caption="Changes since version 1.27.12_1570" caption-side="bottom"}


### Master fix pack 1.27.12_1569, released 27 March 2024
{: #12712_1569_M}

The following table shows the changes that are in the master fix pack 1.27.12_1569. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.4.7 | v1.4.8 | New version contains updates and security fixes. |
| Gateway-enabled cluster controller | 2415 | 2502 | New version contains updates and security fixes. |
| {{site.data.keyword.IBM_notm}} Calico extension | 1534 | 1537 | New version contains security fixes. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.4.18 | v2.4.19 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.11-2 | v1.27.12-1 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 441 | 442 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | 90a78ef | 803912f | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.7 | v2.8.8 | New version contains updates and security fixes. |
| Kubernetes | v1.27.11 | v1.27.12 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.12){: external}. |
| Kubernetes NodeLocal DNS cache | 1.22.28 | 1.23.0 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.23.0){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2807 | 2831 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.11 | v0.13.12 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.12){: external}. |
{: caption="Changes since version 1.27.11_1566" caption-side="bottom"}


### Worker node fix pack 1.27.12_1570, released 25 March 2024
{: #12712_1570_W}

The following table shows the changes that are in the worker node fix pack 1.27.12_1570. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-173-generic | 5.4.0-174-generic | Worker node kernel and package updates for [CVE-2012-6655](https://nvd.nist.gov/vuln/detail/CVE-2012-6655){: external}, [CVE-2023-23000](https://nvd.nist.gov/vuln/detail/CVE-2023-23000){: external}, [CVE-2023-23004](https://nvd.nist.gov/vuln/detail/CVE-2023-23004){: external}, [CVE-2024-1086](https://nvd.nist.gov/vuln/detail/CVE-2024-1086){: external}, [CVE-2024-22667](https://nvd.nist.gov/vuln/detail/CVE-2024-22667){: external}, [CVE-2024-24855](https://nvd.nist.gov/vuln/detail/CVE-2024-24855){: external}. |
| Kubernetes | 1.27.11 | 1.27.12 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.12){: external}. |
| Containerd | 1.7.14 | 1.7.14 | N/A |
| HAProxy | 512b32 | 512b32 | N/A |
{: caption="Changes since version 1.27.11_1568" caption-side="bottom"}


### Worker node fix pack 1.27.11_1568, released 13 March 2024
{: #12711_1568_W}

The following table shows the changes that are in the worker node fix pack 1.27.11_1568. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-172-generic | 5.4.0-173-generic | Worker node kernel and package updates for [CVE-2022-47695](https://nvd.nist.gov/vuln/detail/CVE-2022-47695){: external}, [CVE-2022-48063](https://nvd.nist.gov/vuln/detail/CVE-2022-48063){: external}, [CVE-2022-48065](https://nvd.nist.gov/vuln/detail/CVE-2022-48065){: external}, [CVE-2022-48624](https://nvd.nist.gov/vuln/detail/CVE-2022-48624){: external}, [CVE-2023-0340](https://nvd.nist.gov/vuln/detail/CVE-2023-0340){: external}, [CVE-2023-22995](https://nvd.nist.gov/vuln/detail/CVE-2023-22995){: external}, [CVE-2023-50782](https://nvd.nist.gov/vuln/detail/CVE-2023-50782){: external}, [CVE-2023-51779](https://nvd.nist.gov/vuln/detail/CVE-2023-51779){: external}, [CVE-2023-51781](https://nvd.nist.gov/vuln/detail/CVE-2023-51781){: external}, [CVE-2023-51782](https://nvd.nist.gov/vuln/detail/CVE-2023-51782){: external}, [CVE-2023-6915](https://nvd.nist.gov/vuln/detail/CVE-2023-6915){: external}, [CVE-2024-0565](https://nvd.nist.gov/vuln/detail/CVE-2024-0565){: external}, [CVE-2024-0646](https://nvd.nist.gov/vuln/detail/CVE-2024-0646){: external}, [CVE-2024-24806](https://nvd.nist.gov/vuln/detail/CVE-2024-24806){: external}, [CVE-2024-25062](https://nvd.nist.gov/vuln/detail/CVE-2024-25062){: external}. |
| Kubernetes | 1.27.11 | 1.27.11 | N/A |
| HAProxy | 9b0400 | 512b32 | N/A |
| Containerd | 1.7.13 | 1.7.14 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.14){: external}. |
{: caption="Changes since version 1.27.11_1567" caption-side="bottom"}


### Master fix pack 1.27.11_1566, released 28 February 2024
{: #12711_1566_M}

The following table shows the changes that are in the master fix pack 1.27.11_1566. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.4.6 | v1.4.7 | New version contains updates and security fixes. |
| etcd | v3.5.11 | v3.5.12 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.12){: external}. |
| Gateway-enabled cluster controller | N/A | 2415 | New version contains updates and security fixes. |
| GPU device plug-in and installer | 6273cd0 | d992fea | New version contains updates and security fixes. |
| {{site.data.keyword.IBM_notm}} Calico extension | 1525 | 1534 | New version contains security fixes. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.4.14 | v2.4.18 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.10-3 | v1.27.11-2 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 439 | 441 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 7185ea1 | bd30030 | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.6 | v2.8.7 | New version contains updates and security fixes. |
| Kubernetes | v1.27.10 | v1.27.11 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.11){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2789 | 2807 | New version contains updates and security fixes. |
{: caption="Changes since version 1.27.10_1561" caption-side="bottom"}


### Worker node fix pack 1.27.11_1567, released 26 February 2024
{: #12711_1567_W}

The following table shows the changes that are in the worker node fix pack 1.27.11_1567. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-171-generic | 5.4.0-172-generic | Worker node kernel & package updates for [CVE-2023-4408](https://nvd.nist.gov/vuln/detail/CVE-2023-4408){: external}, [CVE-2023-4641](https://nvd.nist.gov/vuln/detail/CVE-2023-4641){: external}, [CVE-2023-50387](https://nvd.nist.gov/vuln/detail/CVE-2023-50387){: external}, [CVE-2023-50868](https://nvd.nist.gov/vuln/detail/CVE-2023-50868){: external}, [CVE-2023-51781](https://nvd.nist.gov/vuln/detail/CVE-2023-51781){: external}, [CVE-2023-5517](https://nvd.nist.gov/vuln/detail/CVE-2023-5517){: external}, [CVE-2023-6516](https://nvd.nist.gov/vuln/detail/CVE-2023-6516){: external}, [CVE-2023-6915](https://nvd.nist.gov/vuln/detail/CVE-2023-6915){: external}, [CVE-2024-0565](https://nvd.nist.gov/vuln/detail/CVE-2024-0565){: external}, [CVE-2024-0646](https://nvd.nist.gov/vuln/detail/CVE-2024-0646){: external}. |
| Containerd | 1.7.13 | 1.7.13 | N/A |
{: caption="Changes since version 1.27.10_1563" caption-side="bottom"}


### Worker node fix pack 1.27.10_1563, released 12 February 2024
{: #12710_1563_W}

The following table shows the changes that are in the worker node fix pack 1.27.10_1563. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-170-generic | 5.4.0-171-generic | Worker node kernel & package updates for [CVE-2023-2953](https://nvd.nist.gov/vuln/detail/CVE-2023-2953){: external}, [CVE-2023-45863](https://nvd.nist.gov/vuln/detail/CVE-2023-45863){: external}, [CVE-2023-5678](https://nvd.nist.gov/vuln/detail/CVE-2023-5678){: external}, [CVE-2023-6040](https://nvd.nist.gov/vuln/detail/CVE-2023-6040){: external}, [CVE-2023-6606](https://nvd.nist.gov/vuln/detail/CVE-2023-6606){: external}, [CVE-2023-6931](https://nvd.nist.gov/vuln/detail/CVE-2023-6931){: external}, [CVE-2023-6932](https://nvd.nist.gov/vuln/detail/CVE-2023-6932){: external}, [CVE-2024-0727](https://nvd.nist.gov/vuln/detail/CVE-2024-0727){: external}. |
| Kubernetes | N/A |N/A|N/A|
| Containerd | 1.7.12 | 1.7.13 | For more information, see [change log](https://github.com/containerd/containerd/releases/tag/v1.7.13){: external} and [security bulletin for CVE-2024-21626](https://www.ibm.com/support/pages/node/7116230){: external}. |
| HAProxy | a13673 | 9b0400 | Security fixes for [CVE-2024-0553](https://nvd.nist.gov/vuln/detail/CVE-2024-0553){: external}, [CVE-2023-48795](https://nvd.nist.gov/vuln/detail/CVE-2023-48795){: external}, [CVE-2021-35937](https://nvd.nist.gov/vuln/detail/CVE-2021-35937){: external}, [CVE-2021-35938](https://nvd.nist.gov/vuln/detail/CVE-2021-35938){: external}, [CVE-2021-35939](https://nvd.nist.gov/vuln/detail/CVE-2021-35939){: external}. |
{: caption="Changes since version 1.27.10_1562" caption-side="bottom"}


### Master fix pack 1.27.10_1561, released 31 January 2024
{: #12710_1561_M}

The following table shows the changes that are in the master fix pack 1.27.10_1561. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.26.3 | v3.26.4 | See the [Calico release notes](https://archive-os-3-26.netlify.app/calico/3.26/release-notes/#v3.26.4){: external}. |
| Cluster health image | v1.4.5 | v1.4.6 | New version contains security fixes. |
| etcd | v3.5.10 | v3.5.11 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.11){: external}. |
| GPU device plug-in and installer | 0e3950c | 6273cd0 | New version contains security fixes. |
| {{site.data.keyword.IBM_notm}} Calico extension | 1487 | 1525 | New version contains security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.8-5 | v1.27.10-3 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | 58e69e0 | 90a78ef | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | e544e35 | 7185ea1 | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.5 | v2.8.6 | New version contains updates and security fixes. |
| Kubernetes | v1.27.8 | v1.27.10 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.10){: external}. |
| Kubernetes NodeLocal DNS cache | 1.22.27 | 1.22.28 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.22.28){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2767 | 2789 | New version contains updates and security fixes. |
| Portieris admission controller | v0.13.10 | v0.13.11 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.11){: external}. |
{: caption="Changes since version 1.27.8_1556" caption-side="bottom"}


### Worker node fix pack 1.27.10_1562, released 29 January 2024
{: #12710_1562_W}

The following table shows the changes that are in the worker node fix pack 1.27.10_1562. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-169-generic | 5.4.0-170-generic | Worker node package and kernel updates for [CVE-2020-28493](https://nvd.nist.gov/vuln/detail/CVE-2020-28493){: external}, [CVE-2022-44840](https://nvd.nist.gov/vuln/detail/CVE-2022-44840){: external}, [CVE-2022-45703](https://nvd.nist.gov/vuln/detail/CVE-2022-45703){: external}, [CVE-2022-47007](https://nvd.nist.gov/vuln/detail/CVE-2022-47007){: external}, [CVE-2022-47008](https://nvd.nist.gov/vuln/detail/CVE-2022-47008){: external}, [CVE-2022-47010](https://nvd.nist.gov/vuln/detail/CVE-2022-47010){: external}, [CVE-2022-47011](https://nvd.nist.gov/vuln/detail/CVE-2022-47011){: external}, [CVE-2023-6004](https://nvd.nist.gov/vuln/detail/CVE-2023-6004){: external}, [CVE-2023-6040](https://nvd.nist.gov/vuln/detail/CVE-2023-6040){: external}, [CVE-2023-6606](https://nvd.nist.gov/vuln/detail/CVE-2023-6606){: external}, [CVE-2023-6918](https://nvd.nist.gov/vuln/detail/CVE-2023-6918){: external}, [CVE-2023-6931](https://nvd.nist.gov/vuln/detail/CVE-2023-6931){: external}, [CVE-2023-6932](https://nvd.nist.gov/vuln/detail/CVE-2023-6932){: external}, [CVE-2024-0553](https://nvd.nist.gov/vuln/detail/CVE-2024-0553){: external}, [CVE-2024-22195](https://nvd.nist.gov/vuln/detail/CVE-2024-22195){: external}, [CVE-2024-22365](https://nvd.nist.gov/vuln/detail/CVE-2024-22365){: external}. |
| Kubernetes | 1.27.8 | 1.27.10 | For more information, see [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.10){: external}. |
| Containerd | 1.7.12 | 1.7.12 | N/A |
| HAProxy | e105dc | a13673 | Security fixes for [CVE-2023-7104](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-7104){: external}, [CVE-2023-27043](https://exchange.xforce.ibmcloud.com/vulnerabilities/CVE-2023-27043){: external}. |
{: caption="Changes since version 1.27.8_1560" caption-side="bottom"}


### Worker node fix pack 1.27.8_1560, released 16 January 2024
{: #1278_1560_W}

The following table shows the changes that are in the worker node fix pack 1.27.8_1560. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-169-generic | 5.4.0-169-generic | Worker node package updates for [CVE-2021-41617](https://nvd.nist.gov/vuln/detail/CVE-2021-41617){: external}, [CVE-2022-39348](https://nvd.nist.gov/vuln/detail/CVE-2022-39348){: external}, [CVE-2023-46137](https://nvd.nist.gov/vuln/detail/CVE-2023-46137){: external}, [CVE-2023-51385](https://nvd.nist.gov/vuln/detail/CVE-2023-51385){: external}, [CVE-2023-7104](https://nvd.nist.gov/vuln/detail/CVE-2023-7104){: external}. |
| Kubernetes | 1.27.8 | 1.27.8 | N/A |
| Containerd | 1.7.11 | 1.7.12 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.12){: external}. |
| Haproxy | 3060b0 | e105dc | [CVE-2023-39615](https://nvd.nist.gov/vuln/detail/CVE-2023-39615){: external}, [CVE-2023-5981](https://nvd.nist.gov/vuln/detail/CVE-2023-5981){: external}, [CVE-2022-48560](https://nvd.nist.gov/vuln/detail/CVE-2022-48560){: external}, [CVE-2022-48564](https://nvd.nist.gov/vuln/detail/CVE-2022-48564){: external}. |
{: caption="Changes since version 1.27.8_1559" caption-side="bottom"}


### Worker node fix pack 1.27.8_1559, released 02 January 2024
{: #1278_1559_W}

The following table shows the changes that are in the worker node fix pack 1.27.8_1559. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-169-generic | 5.4.0-169-generic | Worker node package updates for [CVE-2023-48795](https://nvd.nist.gov/vuln/detail/CVE-2023-48795){: external}. |
| Kubernetes | 1.27.8 | 1.27.8 | N/A |
| Containerd | 1.7.11 | 1.7.11 | N/A |
{: caption="Changes since version 1.27.8_1558" caption-side="bottom"}


### Worker node fix pack 1.27.8_1558, released 18 December 2023
{: #1278_1558_W}

The following table shows the changes that are in the worker node fix pack 1.27.8_1558. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-167-generic | 5.4.0-169-generic | Worker node kernel & package updates for [CVE-2020-19726](https://nvd.nist.gov/vuln/detail/CVE-2020-19726){: external}, [CVE-2021-46174](https://nvd.nist.gov/vuln/detail/CVE-2021-46174){: external}, [CVE-2022-1725](https://nvd.nist.gov/vuln/detail/CVE-2022-1725){: external}, [CVE-2022-1771](https://nvd.nist.gov/vuln/detail/CVE-2022-1771){: external}, [CVE-2022-1897](https://nvd.nist.gov/vuln/detail/CVE-2022-1897){: external}, [CVE-2022-2000](https://nvd.nist.gov/vuln/detail/CVE-2022-2000){: external}, [CVE-2022-35205](https://nvd.nist.gov/vuln/detail/CVE-2022-35205){: external}, [CVE-2023-23931](https://nvd.nist.gov/vuln/detail/CVE-2023-23931){: external}, [CVE-2023-31085](https://nvd.nist.gov/vuln/detail/CVE-2023-31085){: external}, [CVE-2023-37453](https://nvd.nist.gov/vuln/detail/CVE-2023-37453){: external}, [CVE-2023-39192](https://nvd.nist.gov/vuln/detail/CVE-2023-39192){: external}, [CVE-2023-39193](https://nvd.nist.gov/vuln/detail/CVE-2023-39193){: external}, [CVE-2023-39804](https://nvd.nist.gov/vuln/detail/CVE-2023-39804){: external}, [CVE-2023-42754](https://nvd.nist.gov/vuln/detail/CVE-2023-42754){: external}, [CVE-2023-45539](https://nvd.nist.gov/vuln/detail/CVE-2023-45539){: external}, [CVE-2023-45871](https://nvd.nist.gov/vuln/detail/CVE-2023-45871){: external}, [CVE-2023-46218](https://nvd.nist.gov/vuln/detail/CVE-2023-46218){: external}, [CVE-2023-46246](https://nvd.nist.gov/vuln/detail/CVE-2023-46246){: external}, [CVE-2023-4806](https://nvd.nist.gov/vuln/detail/CVE-2023-4806){: external}, [CVE-2023-4813](https://nvd.nist.gov/vuln/detail/CVE-2023-4813){: external}, [CVE-2023-48231](https://nvd.nist.gov/vuln/detail/CVE-2023-48231){: external}, [CVE-2023-48233](https://nvd.nist.gov/vuln/detail/CVE-2023-48233){: external}, [CVE-2023-48234](https://nvd.nist.gov/vuln/detail/CVE-2023-48234){: external}, [CVE-2023-48235](https://nvd.nist.gov/vuln/detail/CVE-2023-48235){: external}, [CVE-2023-48236](https://nvd.nist.gov/vuln/detail/CVE-2023-48236){: external}, [CVE-2023-48237](https://nvd.nist.gov/vuln/detail/CVE-2023-48237){: external}, [CVE-2023-5178](https://nvd.nist.gov/vuln/detail/CVE-2023-5178){: external}, [CVE-2023-5717](https://nvd.nist.gov/vuln/detail/CVE-2023-5717){: external}. |
| Kubernetes | N/A |N/A|N/A|
| Containerd | 1.7.10 |1.7.11| For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.11){: external}. |
{: caption="Changes since version 1.27.8_1557" caption-side="bottom"}


### Master fix pack 1.27.8_1556, released 06 December 2023
{: #1278_1556_M}

The following table shows the changes that are in the master fix pack 1.27.8_1556. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| GPU device plug-in and installer | 99267c4 | 0e3950c | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.4.12 | v2.4.14 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.7-4 | v1.27.8-5 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 438 | 439 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | c33e6e7 | 58e69e0b | New version contains updates and security fixes. |
| Konnectivity agent and server | v0.1.5_39_iks | v0.1.5_47_iks | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.1.5){: external}. |
| Kubernetes | v1.27.7 | v1.27.8 | Review the [community Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.8){: external}. Resolves [CVE-2023-39325](https://nvd.nist.gov/vuln/detail/CVE-2023-39325){: external} and [CVE-2023-44487](https://nvd.nist.gov/vuln/detail/CVE-2023-44487){: external}. For more information, see [Security Bulletin: IBM Cloud Kubernetes Service is affected by Kubernetes API server security vulnerabilities (CVE-2023-39325 and CVE-2023-44487)](https://www.ibm.com/support/pages/node/7091444){: external}. |
| Kubernetes NodeLocal DNS cache | 1.22.24 | 1.22.27 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.22.27){: external}. |
| Load balancer and Load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2731 | 2767 | New version contains updates and security fixes. |
{: caption="Changes since version 1.27.7_1547" caption-side="bottom"}


### Worker node fix pack 1.27.8_1557, released 04 December 2023
{: #1278_1557_W}

The following table shows the changes that are in the worker node fix pack 1.27.8_1557. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-166-generic | 5.4.0-167-generic | Worker node kernel & package updates for [CVE-2023-31085](https://nvd.nist.gov/vuln/detail/CVE-2023-31085){: external}, [CVE-2023-40217](https://nvd.nist.gov/vuln/detail/CVE-2023-40217){: external}, [CVE-2023-44487](https://nvd.nist.gov/vuln/detail/CVE-2023-44487){: external}, [CVE-2023-45871](https://nvd.nist.gov/vuln/detail/CVE-2023-45871){: external}, [CVE-2023-47038](https://nvd.nist.gov/vuln/detail/CVE-2023-47038){: external}, [CVE-2023-5981](https://nvd.nist.gov/vuln/detail/CVE-2023-5981){: external}. |
| Kubernetes | 1.27.7 | 1.27.8 | Review the [community Kubernetes change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.8){: external}. |
{: caption="Changes since version 1.27.7_1548" caption-side="bottom"}


### Worker node fix pack 1.27.7_1548, released 29 November 2023
{: #1277_1548_W}

The following table shows the changes that are in the worker node fix pack 1.27.7_1548. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-166-generic | 5.4.0-166-generic | Worker node package updates for [CVE-2023-36054](https://nvd.nist.gov/vuln/detail/CVE-2023-36054){: external}, [CVE-2023-4016](https://nvd.nist.gov/vuln/detail/CVE-2023-4016){: external}, [CVE-2023-43804](https://nvd.nist.gov/vuln/detail/CVE-2023-43804){: external}, [CVE-2023-45803](https://nvd.nist.gov/vuln/detail/CVE-2023-45803){: external}. |
| Kubernetes | 1.27.6 | 1.27.7 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.7){: external}. |
| Containerd| 1.7.8 | 1.7.9 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.9){: external}. |
{: caption="Changes since version 1.27.6_1546" caption-side="bottom"}


### Master fix pack 1.27.7_1547, released 15 November 2023
{: #1277_1547_M}

The following table shows the changes that are in the master fix pack 1.27.7_1547. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.4.4 | v1.4.5 | New version contains updates and security fixes. |
| etcd | v3.5.9 | v3.5.10 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.10){: external}. |
| GPU device plug-in and installer | 4319682 | 99267c4 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.6-8 | v1.27.7-4 | New version contains updates and security fixes. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 435 | 438 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | a1edf56 | c33e6e7 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | f0d3265 | e544e35 | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.4 | v2.8.5 | New version contains updates and security fixes. |
| Kubernetes | v1.27.6 | v1.27.7 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.7){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2681 | 2731 | New version contains updates and security fixes. |
| Konnectivity agent and server | v0.1.3_5_iks | v0.1.5_39_iks | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.1.5){: external}. |
| Portieris admission controller | v0.13.8 | v0.13.10 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.10){: external}. |
{: caption="Changes since version 1.27.6_1544" caption-side="bottom"}


### Worker node fix pack 1.27.6_1546, released 08 November 2023
{: #1276_1546_W}

The following table shows the changes that are in the worker node fix pack 1.27.6_1546. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
|Ubuntu 20.04 packages | 5.4.0-165-generic | 5.4.0-166-generic | Worker node kernel & package updates for [CVE-2023-0597](https://nvd.nist.gov/vuln/detail/CVE-2023-0597){: external}, [CVE-2023-31083](https://nvd.nist.gov/vuln/detail/CVE-2023-31083){: external}, [CVE-2023-34058](https://nvd.nist.gov/vuln/detail/CVE-2023-34058){: external}, [CVE-2023-34059](https://nvd.nist.gov/vuln/detail/CVE-2023-34059){: external}, [CVE-2023-34319](https://nvd.nist.gov/vuln/detail/CVE-2023-34319){: external}, [CVE-2023-3446](https://nvd.nist.gov/vuln/detail/CVE-2023-3446){: external}, [CVE-2023-3772](https://nvd.nist.gov/vuln/detail/CVE-2023-3772){: external}, [CVE-2023-3817](https://nvd.nist.gov/vuln/detail/CVE-2023-3817){: external}, [CVE-2023-4132](https://nvd.nist.gov/vuln/detail/CVE-2023-4132){: external}, [CVE-2023-42752](https://nvd.nist.gov/vuln/detail/CVE-2023-42752){: external}, [CVE-2023-42753](https://nvd.nist.gov/vuln/detail/CVE-2023-42753){: external}, [CVE-2023-42755](https://nvd.nist.gov/vuln/detail/CVE-2023-42755){: external}, [CVE-2023-42756](https://nvd.nist.gov/vuln/detail/CVE-2023-42756){: external}, [CVE-2023-4622](https://nvd.nist.gov/vuln/detail/CVE-2023-4622){: external}, [CVE-2023-4623](https://nvd.nist.gov/vuln/detail/CVE-2023-4623){: external}, [CVE-2023-4733](https://nvd.nist.gov/vuln/detail/CVE-2023-4733){: external}, [CVE-2023-4735](https://nvd.nist.gov/vuln/detail/CVE-2023-4735){: external}, [CVE-2023-4750](https://nvd.nist.gov/vuln/detail/CVE-2023-4750){: external}, [CVE-2023-4751](https://nvd.nist.gov/vuln/detail/CVE-2023-4751){: external}, [CVE-2023-4752](https://nvd.nist.gov/vuln/detail/CVE-2023-4752){: external}, [CVE-2023-4781](https://nvd.nist.gov/vuln/detail/CVE-2023-4781){: external}, [CVE-2023-4881](https://nvd.nist.gov/vuln/detail/CVE-2023-4881){: external}, [CVE-2023-4921](https://nvd.nist.gov/vuln/detail/CVE-2023-4921){: external}, [CVE-2023-5344](https://nvd.nist.gov/vuln/detail/CVE-2023-5344){: external}, [CVE-2023-5441](https://nvd.nist.gov/vuln/detail/CVE-2023-5441){: external}, [CVE-2023-5535](https://nvd.nist.gov/vuln/detail/CVE-2023-5535){: external}. |
| Containerd | 1.7.7 | 1.7.8 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.8){: external}. |
{: caption="Changes since version 1.27.6_1545" caption-side="bottom"}


### Master fix pack 1.27.6_1544, released 25 October 2023
{: #1276_1544_M}

The following table shows the changes that are in the master fix pack 1.27.6_1544. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.26.1 | v3.26.3 | See the [Calico release notes](https://docs.tigera.io/calico/latest/release-notes/#v3.26.3){: external}. |
| Cluster health image | v1.4.2 | v1.4.4 | New version contains updates and security fixes. |
| {{site.data.keyword.IBM_notm}} Calico extension | 1390 | 1487 | New version contains security fixes. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.4.10 | v2.4.12 | New version contains updates and security fixes. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.5-3 | v1.27.6-8 | New version contains updates and security fixes. The logic for the `service.kubernetes.io/ibm-load-balancer-cloud-provider-vpc-idle-connection-timeout` annotation has changed. The default idle timeout is dependent on your account settings. Usually, this value is `50`. However, some allowlisted accounts have larger timeout settings. If you don't set the annotation, your load balancers use the timeout setting in your account. You can explicitly specify the timeout by setting this annotation. |
| {{site.data.keyword.cloud_notm}} RBAC Operator | 4e2f346 | f0d3265 | New version contains updates and security fixes. |
| Key Management Service provider | v2.8.2 | v2.8.4 | New version contains updates and security fixes. |
| Kubernetes | v1.27.5 | v1.27.6 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.6){: external}. |
| Kubernetes NodeLocal DNS cache | 1.22.23 | 1.22.24 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.22.24){: external}. |
| Portieris admission controller | v0.13.6 | v0.13.8 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.8){: external}. |
{: caption="Changes since version 1.27.5_1540" caption-side="bottom"}


### Worker node fix pack 1.27.6_1545, released 23 October 2023
{: #1276_1545_W}

The following table shows the changes that are in the worker node fix pack 1.27.6_1545. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-164-generic | 5.4.0-165-generic | Worker node kernel & package updates for [CVE-2022-3234](https://nvd.nist.gov/vuln/detail/CVE-2022-3234){: external}, [CVE-2022-3256](https://nvd.nist.gov/vuln/detail/CVE-2022-3256){: external}, [CVE-2022-3324](https://nvd.nist.gov/vuln/detail/CVE-2022-3324){: external}, [CVE-2022-3352](https://nvd.nist.gov/vuln/detail/CVE-2022-3352){: external}, [CVE-2022-3520](https://nvd.nist.gov/vuln/detail/CVE-2022-3520){: external}, [CVE-2022-3591](https://nvd.nist.gov/vuln/detail/CVE-2022-3591){: external}, [CVE-2022-3705](https://nvd.nist.gov/vuln/detail/CVE-2022-3705){: external}, [CVE-2022-4292](https://nvd.nist.gov/vuln/detail/CVE-2022-4292){: external}, [CVE-2022-4293](https://nvd.nist.gov/vuln/detail/CVE-2022-4293){: external}, [CVE-2023-34319](https://nvd.nist.gov/vuln/detail/CVE-2023-34319){: external}, [CVE-2023-38546](https://nvd.nist.gov/vuln/detail/CVE-2023-38546){: external}, [CVE-2023-42752](https://nvd.nist.gov/vuln/detail/CVE-2023-42752){: external}, [CVE-2023-42753](https://nvd.nist.gov/vuln/detail/CVE-2023-42753){: external}, [CVE-2023-42755](https://nvd.nist.gov/vuln/detail/CVE-2023-42755){: external}, [CVE-2023-42756](https://nvd.nist.gov/vuln/detail/CVE-2023-42756){: external}, [CVE-2023-4622](https://nvd.nist.gov/vuln/detail/CVE-2023-4622){: external}, [CVE-2023-4623](https://nvd.nist.gov/vuln/detail/CVE-2023-4623){: external}, [CVE-2023-4881](https://nvd.nist.gov/vuln/detail/CVE-2023-4881){: external}, [CVE-2023-4921](https://nvd.nist.gov/vuln/detail/CVE-2023-4921){: external}. |
| Kubernetes | 1.27.5 | 1.27.6 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.6){: external}. |
| Containerd | 1.7.6 | 1.7.7 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.7.7){: external}. |
{: caption="Changes since version 1.27.5_1542" caption-side="bottom"}


### Worker node fix pack 1.27.5_1542, released 9 October 2023
{: #1275_1542_W}

The following table shows the changes that are in the worker node fix pack 1.27.5_1542. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-163-generic | 5.4.0-164-generic | Worker node kernel & package updates for [CVE-2021-4001](https://nvd.nist.gov/vuln/detail/CVE-2021-4001){: external}, [CVE-2023-1206](https://nvd.nist.gov/vuln/detail/CVE-2023-1206){: external}, [CVE-2023-20588](https://nvd.nist.gov/vuln/detail/CVE-2023-20588){: external}, [CVE-2023-3212](https://nvd.nist.gov/vuln/detail/CVE-2023-3212){: external}, [CVE-2023-3863](https://nvd.nist.gov/vuln/detail/CVE-2023-3863){: external}, [CVE-2023-40283](https://nvd.nist.gov/vuln/detail/CVE-2023-40283){: external}, [CVE-2023-4128](https://nvd.nist.gov/vuln/detail/CVE-2023-4128){: external}, [CVE-2023-4194](https://nvd.nist.gov/vuln/detail/CVE-2023-4194){: external}, [CVE-2023-43785](https://nvd.nist.gov/vuln/detail/CVE-2023-43785){: external}, [CVE-2023-43786](https://nvd.nist.gov/vuln/detail/CVE-2023-43786){: external}, [CVE-2023-43787](https://nvd.nist.gov/vuln/detail/CVE-2023-43787){: external}. |
| Kubernetes | N/A |N/A|N/A|
| Containerd | N/A |N/A|N/A|
{: caption="Changes since version 1.27.5_1541" caption-side="bottom"}


### Worker node fix pack 1.27.5_1541, released 27 September 2023
{: #1275_1541_W}

The following table shows the changes that are in the worker node fix pack 1.27.5_1541. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-162-generic | 5.4.0-163-generic| Package updates for [CVE-2023-3341](https://nvd.nist.gov/vuln/detail/CVE-2023-3341){: external}, [CVE-2023-4156](https://nvd.nist.gov/vuln/detail/CVE-2023-4156){: external}, [CVE-2023-4128](https://nvd.nist.gov/vuln/detail/CVE-2023-4128){: external}, [CVE-2023-20588](https://nvd.nist.gov/vuln/detail/CVE-2023-20588){: external}, [CVE-2023-20900](https://nvd.nist.gov/vuln/detail/CVE-2023-20900){: external}, [CVE-2023-40283](https://nvd.nist.gov/vuln/detail/CVE-2023-40283){: external}. |
| RHEL 8 Packages | 4.18.0-477.21.1.el8_8 | 4.18.0-477.27.1.el8_8 | Worker node kernel & package updates for [CVE-2023-2002](https://nvd.nist.gov/vuln/detail/CVE-2023-2002){: external}, [CVE-2023-3090](https://nvd.nist.gov/vuln/detail/CVE-2023-3090){: external}, [CVE-2023-3390](https://nvd.nist.gov/vuln/detail/CVE-2023-3390){: external}, [CVE-2023-3776](https://nvd.nist.gov/vuln/detail/CVE-2023-3776){: external}, [CVE-2023-4004](https://nvd.nist.gov/vuln/detail/CVE-2023-4004){: external}, [CVE-2023-20593](https://nvd.nist.gov/vuln/detail/CVE-2023-20593){: external}, [CVE-2023-29491](https://nvd.nist.gov/vuln/detail/CVE-2023-29491){: external}, [CVE-2023-30630](https://nvd.nist.gov/vuln/detail/CVE-2023-30630){: external}, [CVE-2023-35001](https://nvd.nist.gov/vuln/detail/CVE-2023-35001){: external}, [CVE-2023-35788](https://nvd.nist.gov/vuln/detail/CVE-2023-35788){: external}. |
{: caption="Changes since version 1.27.4_1538" caption-side="bottom"}


### Master fix pack 1.27.5_1540, released 20 September 2023
{: #1275_1540_M}

The following table shows the changes that are in the master fix pack 1.27.5_1540. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.26.0 | v3.26.1 | See the [Calico release notes](https://docs.tigera.io/calico/latest/release-notes/#v3.26.1){: external}. |
| Cluster health image | v1.4.1 | v1.4.2 | Updated `Go` to version `1.20.8` and updated dependencies. |
| {{site.data.keyword.cloud_notm}} Block Storage driver and plug-in | v2.4.5 | v2.4.10 | Updated `Go dependencies`. Updated to newer UBI base image. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.4-5 | v1.27.5-3 | Updated to support the `Kubernetes 1.27.5` release. Updated `Go` to version `1.20.7` and updated `Go dependencies`. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 434 | 435 | Updated `Go` to version `1.20.6` and updated dependencies. Updated to newer UBI base image. |
| Key Management Service provider | v2.8.1 | v2.8.2 | Updated `Go dependencies`. |
| Kubernetes | v1.27.4 | v1.27.5 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.5){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2631 | 2681 | Updated `Go` to version `1.19.12` and updated `Go dependencies`. |
{: caption="Changes since version 1.27.4_1536" caption-side="bottom"}


### Worker node fix pack 1.27.4_1538, released 12 September 2023
{: #1274_1538_W}

The following table shows the changes that are in the worker node fix pack 1.27.4_1538. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-156-generic | 5.4.0-162-generic | Worker node kernel & package updates for [CVE-2020-21047](https://nvd.nist.gov/vuln/detail/CVE-2020-21047){: external}, [CVE-2021-33294](https://nvd.nist.gov/vuln/detail/CVE-2021-33294){: external}, [CVE-2022-40982](https://nvd.nist.gov/vuln/detail/CVE-2022-40982){: external}, [CVE-2023-20593](https://nvd.nist.gov/vuln/detail/CVE-2023-20593){: external}[CVE-2023-2269](https://nvd.nist.gov/vuln/detail/CVE-2023-2269){: external}, [CVE-2023-31084](https://nvd.nist.gov/vuln/detail/CVE-2023-31084){: external}, [CVE-2023-3268](https://nvd.nist.gov/vuln/detail/CVE-2023-3268){: external}, [CVE-2023-3609](https://nvd.nist.gov/vuln/detail/CVE-2023-3609){: external}, [CVE-2023-3611](https://nvd.nist.gov/vuln/detail/CVE-2023-3611){: external}, [CVE-2023-3776](https://nvd.nist.gov/vuln/detail/CVE-2023-3776){: external}. |
| Containerd | 1.7.4| 1.7.5 |N/A|
{: caption="Changes since version 1.27.4_1537" caption-side="bottom"}


### Master fix pack 1.27.4_1536, released 30 August 2023
{: #1274_1536_M}

The following table shows the changes that are in the master fix pack 1.27.4_1536. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.4.0 | v1.4.1 | Updated `Go` to version `1.19.12` and updated dependencies. |
| GPU device plug-in and installer | 495931a | 8e87e60 | Updated `Go` to version `1.19.11` |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.4-1 | v1.27.4-5 | Updated `Go` dependencies to resolve a CVE. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 433 | 434 | Updated `Go` to version `1.20.6` and updated dependencies. Updated to newer UBI base image. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | d293d8b | a1edf56 | Updated `Go` to version `1.20.6`. |
| Key Management Service provider | v2.8.0 | v2.8.1 | Updated `Go` dependencies |
| Portieris admission controller | v0.13.5 | v0.13.6 | See the [Portieris admission controller release notes](https://github.com/{{site.data.keyword.IBM_notm}}/portieris/releases/tag/v0.13.6){: external}. |
{: caption="Changes since version 1.27.4_1533" caption-side="bottom"}


### Worker node fix pack 1.27.4_1537, released 28 August 2023
{: #1274_1537_W}

The following table shows the changes that are in the worker node fix pack 1.27.4_1537. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | 5.4.0-155-generic | 5.4.0-156-generic | Worker node kernel & package updates for [CVE-2022-2598](https://nvd.nist.gov/vuln/detail/CVE-2022-2598){: external}, [CVE-2022-3016](https://nvd.nist.gov/vuln/detail/CVE-2022-3016){: external}, [CVE-2022-3037](https://nvd.nist.gov/vuln/detail/CVE-2022-3037){: external}, [CVE-2022-3099](https://nvd.nist.gov/vuln/detail/CVE-2022-3099){: external}, [CVE-2023-40225](https://nvd.nist.gov/vuln/detail/CVE-2023-40225){: external}. |
{: caption="Changes since version 1.27.4_1535" caption-side="bottom"}


### Worker node fix pack 1.27.4_1535, released 15 August 2023
{: #1274_1535_W}

The following table shows the changes that are in the worker node fix pack 1.27.4_1535. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 20.04 packages | N/A | N/A | Package updates for [CVE-2020-36691](https://nvd.nist.gov/vuln/detail/CVE-2020-36691){: external}, [CVE-2022-0168](https://nvd.nist.gov/vuln/detail/CVE-2022-0168){: external}, [CVE-2022-1184](https://nvd.nist.gov/vuln/detail/CVE-2022-1184){: external}, [CVE-2022-2208](https://nvd.nist.gov/vuln/detail/CVE-2022-2208){: external}, [CVE-2022-2210](https://nvd.nist.gov/vuln/detail/CVE-2022-2210){: external}, [CVE-2022-2257](https://nvd.nist.gov/vuln/detail/CVE-2022-2257){: external}, [CVE-2022-2264](https://nvd.nist.gov/vuln/detail/CVE-2022-2264){: external}, [CVE-2022-2284](https://nvd.nist.gov/vuln/detail/CVE-2022-2284){: external}, [CVE-2022-2285](https://nvd.nist.gov/vuln/detail/CVE-2022-2285){: external}, [CVE-2022-2286](https://nvd.nist.gov/vuln/detail/CVE-2022-2286){: external}, [CVE-2022-2287](https://nvd.nist.gov/vuln/detail/CVE-2022-2287){: external}, [CVE-2022-2289](https://nvd.nist.gov/vuln/detail/CVE-2022-2289){: external}, [CVE-2022-27672](https://nvd.nist.gov/vuln/detail/CVE-2022-27672){: external}, [CVE-2022-4269](https://nvd.nist.gov/vuln/detail/CVE-2022-4269){: external}, [CVE-2023-1611](https://nvd.nist.gov/vuln/detail/CVE-2023-1611){: external}, [CVE-2023-2124](https://nvd.nist.gov/vuln/detail/CVE-2023-2124){: external}, [CVE-2023-3090](https://nvd.nist.gov/vuln/detail/CVE-2023-3090){: external}, [CVE-2023-3111](https://nvd.nist.gov/vuln/detail/CVE-2023-3111){: external}, [CVE-2023-3141](https://nvd.nist.gov/vuln/detail/CVE-2023-3141){: external}, [CVE-2023-32629](https://nvd.nist.gov/vuln/detail/CVE-2023-32629){: external}, [CVE-2023-3390](https://nvd.nist.gov/vuln/detail/CVE-2023-3390){: external}, [CVE-2023-35001](https://nvd.nist.gov/vuln/detail/CVE-2023-35001){: external}. |
| Kubernetes | N/A | N/A | N/A |
| Containerd | N/A | N/A | N/A |
{: caption="Changes since version 1.27.4_1534" caption-side="bottom"}


### Worker node fix pack 1.27.4_1534, released 1 August 2023
{: #1274_1534_W}

The following table shows the changes that are in the worker node fix pack 1.27.4_1534. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-212-generic | 4.15.0-214-generic | Worker node kernel & package updates for [CVE-2020-13987](https://nvd.nist.gov/vuln/detail/CVE-2020-13987){: external}, [CVE-2020-13988](https://nvd.nist.gov/vuln/detail/CVE-2020-13988){: external}, [CVE-2020-17437](https://nvd.nist.gov/vuln/detail/CVE-2020-17437){: external}, [CVE-2022-1184](https://nvd.nist.gov/vuln/detail/CVE-2022-1184){: external}, [CVE-2022-3303](https://nvd.nist.gov/vuln/detail/CVE-2022-3303){: external}, [CVE-2023-1611](https://nvd.nist.gov/vuln/detail/CVE-2023-1611){: external}, [CVE-2023-1670](https://nvd.nist.gov/vuln/detail/CVE-2023-1670){: external}, [CVE-2023-1859](https://nvd.nist.gov/vuln/detail/CVE-2023-1859){: external}, [CVE-2023-1990](https://nvd.nist.gov/vuln/detail/CVE-2023-1990){: external}, [CVE-2023-20867](https://nvd.nist.gov/vuln/detail/CVE-2023-20867){: external}, [CVE-2023-2124](https://nvd.nist.gov/vuln/detail/CVE-2023-2124){: external}, [CVE-2023-2828](https://nvd.nist.gov/vuln/detail/CVE-2023-2828){: external}, [CVE-2023-3090](https://nvd.nist.gov/vuln/detail/CVE-2023-3090){: external}, [CVE-2023-3111](https://nvd.nist.gov/vuln/detail/CVE-2023-3111){: external}, [CVE-2023-3141](https://nvd.nist.gov/vuln/detail/CVE-2023-3141){: external}, [CVE-2023-3268](https://nvd.nist.gov/vuln/detail/CVE-2023-3268){: external}, [CVE-2023-3390](https://nvd.nist.gov/vuln/detail/CVE-2023-3390){: external}, [CVE-2023-35001](https://nvd.nist.gov/vuln/detail/CVE-2023-35001){: external}. |
| Ubuntu 20.04 packages | 5.4.0-153-generic | 5.4.0-155-generic | Worker node kernel & package updates for [CVE-2020-13987](https://nvd.nist.gov/vuln/detail/CVE-2020-13987){: external}, [CVE-2020-13988](https://nvd.nist.gov/vuln/detail/CVE-2020-13988){: external}, [CVE-2020-17437](https://nvd.nist.gov/vuln/detail/CVE-2020-17437){: external}, [CVE-2023-20867](https://nvd.nist.gov/vuln/detail/CVE-2023-20867){: external}, [CVE-2023-28321](https://nvd.nist.gov/vuln/detail/CVE-2023-28321){: external}, [CVE-2023-28322](https://nvd.nist.gov/vuln/detail/CVE-2023-28322){: external}, [CVE-2023-3090](https://nvd.nist.gov/vuln/detail/CVE-2023-3090){: external}, [CVE-2023-32629](https://nvd.nist.gov/vuln/detail/CVE-2023-32629){: external}, [CVE-2023-3390](https://nvd.nist.gov/vuln/detail/CVE-2023-3390){: external}, [CVE-2023-35001](https://nvd.nist.gov/vuln/detail/CVE-2023-35001){: external}, [CVE-2023-38408](https://nvd.nist.gov/vuln/detail/CVE-2023-38408){: external}. |
| Kubernetes | 1.27.3 | 1.27.4 | For more information, see the [change logs](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.4){: external}. |
| Containerd | 1.6.21 | 1.6.22 | For more information, see the [change logs](https://github.com/containerd/containerd/releases/tag/v1.6.22){: external}. |
{: caption="Changes since version 1.27.3_1532" caption-side="bottom"}


### Master fix pack 1.27.4_1533, released 27 July 2023
{: #1274_1533_M}

The following table shows the changes that are in the master fix pack 1.27.4_1533. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Cluster health image | v1.3.21 | v1.4.0 | Updated `Go` to version `1.19.11` and updated `Go` dependencies. Updated UBI base image with FedRAMP enablement support. |
| etcd | N/A | N/A | etcd is now automatically defragmented when necessary. |
| GPU device plug-in and installer | 202b284 | 495931a | Updated `Go` to version `1.20.6`. |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.3-1 | v1.27.4-1 | Updated to support the Kubernetes `1.27.4` release. Updated `Go` dependencies and to `Go` version `1.20.6`. Updates to classic load balancers are now staggered. |
| Key Management Service provider | v2.6.7 | v2.8.0 | Updated `Go` to version `1.19.11` and updated `Go` dependencies. Updated UBI base image with FedRAMP enablement support. |
| Konnectivity agent and server | v0.1.2_591_iks | v0.1.3_5_iks | See the [Konnectivity release notes](https://github.com/kubernetes-sigs/apiserver-network-proxy/releases/tag/v0.1.3){: external}. |
| Kubernetes NodeLocal DNS cache | 1.22.21 | 1.22.23 | See the [Kubernetes NodeLocal DNS cache release notes](https://github.com/kubernetes/dns/releases/tag/1.22.23){: external}. |
| Kubernetes | v1.27.3 | v1.27.3 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.4){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2584 | 2631 | Updated `Go` to version `1.19.10` and updated `Go` dependencies. Updated Alpine base image. |
{: caption="Changes since version 1.27.3_1529" caption-side="bottom"}


### Worker node fix pack 1.27.3_1532, released 17 July 2023
{: #1273_1532_W}

The following table shows the changes that are in the worker node fix pack 1.27.3_1532. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Kubernetes | N/A | N/A | N/A |
| Ubuntu 18.04 packages | N/A | N/A | Worker node package updates for [CVE-2023-24626](https://nvd.nist.gov/vuln/detail/CVE-2023-24626){: external}, [CVE-2023-2953](https://nvd.nist.gov/vuln/detail/CVE-2023-2953){: external}. |
| Ubuntu 20.04 packages | N/A | N/A | N/A |
{: caption="Changes since version 1.27.3_1530" caption-side="bottom"}


### Worker node fix pack 1.27.3_1530, released 03 July 2023
{: #1273_1530_W}

The following table shows the changes that are in the worker node fix pack 1.27.3_1530. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | N/A | N/A | Worker node package updates for [CVE-2023-2603](https://nvd.nist.gov/vuln/detail/CVE-2023-2603){: external},[CVE-2023-3138](https://nvd.nist.gov/vuln/detail/CVE-2023-3138){: external}
| Ubuntu 20.04 packages | 5.4.0-150-generic | 5.4.0-153-generic | Worker node kernel & package updates for [CVE-2023-0461](https://nvd.nist.gov/vuln/detail/CVE-2023-0461){: external},[CVE-2023-1380](https://nvd.nist.gov/vuln/detail/CVE-2023-1380){: external},[CVE-2023-1670](https://nvd.nist.gov/vuln/detail/CVE-2023-1670){: external},[CVE-2023-1859](https://nvd.nist.gov/vuln/detail/CVE-2023-1859){: external},[CVE-2023-2612](https://nvd.nist.gov/vuln/detail/CVE-2023-2612){: external},[CVE-2023-2828](https://nvd.nist.gov/vuln/detail/CVE-2023-2828){: external},[CVE-2023-30456](https://nvd.nist.gov/vuln/detail/CVE-2023-30456){: external},[CVE-2023-3138](https://nvd.nist.gov/vuln/detail/CVE-2023-3138){: external},[CVE-2023-31436](https://nvd.nist.gov/vuln/detail/CVE-2023-31436){: external},[CVE-2023-32233](https://nvd.nist.gov/vuln/detail/CVE-2023-32233){: external},[CVE-2023-3297](https://nvd.nist.gov/vuln/detail/CVE-2023-3297){: external}. |
| Kubernetes | 1.27.2 | 1.27.3 |See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/blob/master/CHANGELOG/CHANGELOG-1.27.md#v1273){: external}.|
{: caption="Changes since version 1.27.2_1528" caption-side="bottom"}


### Master fix pack 1.27.3_1529, released 27 June 2023
{: #1273_1529_M}

The following table shows the changes that are in the master fix pack 1.27.3_1529. Master patch updates are applied automatically. 



| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Calico | v3.25.1 | v3.26.0 | See the [Calico release notes](https://docs.tigera.io/calico/latest/release-notes/#v3.26.0){: external}. |
| Cluster health image | v1.3.20 | v1.3.21 | Updated `Go` dependencies and to `Go` version `1.19.10`. |
| etcd | v3.5.8 | v3.5.9 | See the [etcd release notes](https://github.com/etcd-io/etcd/releases/v3.5.9){: external}. |
| GPU device plug-in and installer | 28d80a0 | 202b284 | Updated to `Go` version `1.19.9` |
| {{site.data.keyword.cloud_notm}} Controller Manager | v1.27.1-8 | v1.27.3-1 | Updated to support the `Kubernetes 1.27.3` release. Updated `Go` dependencies and to `Go` version `1.20.5`. Updated `calicoctl` and `vpcctl`. |
| {{site.data.keyword.filestorage_full_notm}} plug-in and monitor | 431 | 433 | Updated `Go` to version `1.20.4`. Updated UBI base image. |
| {{site.data.keyword.cloud_notm}} Metrics Server Config Watcher | d842983 | d293d8b | Updated `Go` to version `1.20.5`. Updates to build and base images. |
| Key Management Service provider | v2.6.6 | v2.6.7 | Updated `Go` dependencies and to `Go` version `1.19.10`. |
| Kubernetes | v1.27.2 | v1.27.3 | [CVE-2023-2728](https://nvd.nist.gov/vuln/detail/CVE-2023-2728){: external}. For more information, see [{{site.data.keyword.containerlong_notm}} is affected by a Kubernetes API server security vulnerability (CVE-2023-2728)](https://www.ibm.com/support/pages/node/7011039){: external}. See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.3){: external}. |
| Load balancer and load balancer monitor for {{site.data.keyword.cloud_notm}} Provider | 2486 | 2584 | Updated `Go` dependencies and to `Go` version `1.19.9`. Updated base image. |
{: caption="Changes since version 1.27.2_1524" caption-side="bottom"}


### Worker node fix pack 1.27.2_1528, released 19 June 2023
{: #1272_1528_W}

The following table shows the changes that are in the worker node fix pack 1.27.2_1528. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | N/A | N/A | Worker node package updates for [CVE-2020-11080](https://nvd.nist.gov/vuln/detail/CVE-2020-11080){: external},[CVE-2023-24329](https://nvd.nist.gov/vuln/detail/CVE-2023-24329){: external},[CVE-2023-2603](https://nvd.nist.gov/vuln/detail/CVE-2023-2603){: external},[CVE-2023-2609](https://nvd.nist.gov/vuln/detail/CVE-2023-2609){: external},[CVE-2023-2610](https://nvd.nist.gov/vuln/detail/CVE-2023-2610){: external},[CVE-2023-32681](https://nvd.nist.gov/vuln/detail/CVE-2023-32681){: external}
| Ubuntu 20.04 packages | 5.4.0-149-generic | 5.4.0-150-generic | Worker node kernel & package updates for [CVE-2020-11080](https://nvd.nist.gov/vuln/detail/CVE-2020-11080){: external},[CVE-2021-45078](https://nvd.nist.gov/vuln/detail/CVE-2021-45078){: external},[CVE-2023-1380](https://nvd.nist.gov/vuln/detail/CVE-2023-1380){: external},[CVE-2023-1667](https://nvd.nist.gov/vuln/detail/CVE-2023-1667){: external},[CVE-2023-1670](https://nvd.nist.gov/vuln/detail/CVE-2023-1670){: external},[CVE-2023-1859](https://nvd.nist.gov/vuln/detail/CVE-2023-1859){: external},[CVE-2023-2283](https://nvd.nist.gov/vuln/detail/CVE-2023-2283){: external},[CVE-2023-24329](https://nvd.nist.gov/vuln/detail/CVE-2023-24329){: external},[CVE-2023-24593](https://nvd.nist.gov/vuln/detail/CVE-2023-24593){: external},[CVE-2023-2602](https://nvd.nist.gov/vuln/detail/CVE-2023-2602){: external},[CVE-2023-2603](https://nvd.nist.gov/vuln/detail/CVE-2023-2603){: external},[CVE-2023-2609](https://nvd.nist.gov/vuln/detail/CVE-2023-2609){: external},[CVE-2023-2610](https://nvd.nist.gov/vuln/detail/CVE-2023-2610){: external},[CVE-2023-2612](https://nvd.nist.gov/vuln/detail/CVE-2023-2612){: external},[CVE-2023-30456](https://nvd.nist.gov/vuln/detail/CVE-2023-30456){: external},[CVE-2023-3138](https://nvd.nist.gov/vuln/detail/CVE-2023-3138){: external},[CVE-2023-31436](https://nvd.nist.gov/vuln/detail/CVE-2023-31436){: external},[CVE-2023-31484](https://nvd.nist.gov/vuln/detail/CVE-2023-31484){: external},[CVE-2023-32233](https://nvd.nist.gov/vuln/detail/CVE-2023-32233){: external},[CVE-2023-32643](https://nvd.nist.gov/vuln/detail/CVE-2023-32643){: external},[CVE-2023-32681](https://nvd.nist.gov/vuln/detail/CVE-2023-32681){: external}. |
| Kubernetes | N/A |N/A|N/A|
{: caption="Changes since version 1.27.2_1527" caption-side="bottom"}


### Worker node fix pack 1.27.2_1527, released 5 June 2023
{: #1272_1527_W}

The following table shows the changes that are in the worker node fix pack 1.27.2_1527. Worker node patch updates can be applied by updating, reloading (in classic infrastructure), or replacing (in VPC infrastructure) the worker node.
{: shortdesc}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| Ubuntu 18.04 packages | 4.15.0-211-generic | 4.15.0-212-generic | Worker node kernel & package updates for [CVE-2019-17595](https://nvd.nist.gov/vuln/detail/CVE-2019-17595){: external}, [CVE-2021-39537](https://nvd.nist.gov/vuln/detail/CVE-2021-39537){: external}, [CVE-2022-29458](https://nvd.nist.gov/vuln/detail/CVE-2022-29458){: external}, [CVE-2022-4304](https://nvd.nist.gov/vuln/detail/CVE-2022-4304){: external}, [CVE-2023-1380](https://nvd.nist.gov/vuln/detail/CVE-2023-1380){: external}, [CVE-2023-25584](https://nvd.nist.gov/vuln/detail/CVE-2023-25584){: external}, [CVE-2023-25585](https://nvd.nist.gov/vuln/detail/CVE-2023-25585){: external}, [CVE-2023-25588](https://nvd.nist.gov/vuln/detail/CVE-2023-25588){: external}, [CVE-2023-2650](https://nvd.nist.gov/vuln/detail/CVE-2023-2650){: external}, [CVE-2023-29491](https://nvd.nist.gov/vuln/detail/CVE-2023-29491){: external}, [CVE-2023-30456](https://nvd.nist.gov/vuln/detail/CVE-2023-30456){: external}, [CVE-2023-31436](https://nvd.nist.gov/vuln/detail/CVE-2023-31436){: external}, [CVE-2023-31484](https://nvd.nist.gov/vuln/detail/CVE-2023-31484){: external}, [CVE-2023-32233](https://nvd.nist.gov/vuln/detail/CVE-2023-32233){: external}. |
| Ubuntu 20.04 packages | 5.4.0-148-generic | 5.4.0-149-generic | Worker node kernel & package updates for [CVE-2021-39537](https://nvd.nist.gov/vuln/detail/CVE-2021-39537){: external}, [CVE-2022-29458](https://nvd.nist.gov/vuln/detail/CVE-2022-29458){: external}, [CVE-2023-1075](https://nvd.nist.gov/vuln/detail/CVE-2023-1075){: external}, [CVE-2023-1118](https://nvd.nist.gov/vuln/detail/CVE-2023-1118){: external}, [CVE-2023-1380](https://nvd.nist.gov/vuln/detail/CVE-2023-1380){: external}, [CVE-2023-25584](https://nvd.nist.gov/vuln/detail/CVE-2023-25584){: external}, [CVE-2023-25585](https://nvd.nist.gov/vuln/detail/CVE-2023-25585){: external}, [CVE-2023-25588](https://nvd.nist.gov/vuln/detail/CVE-2023-25588){: external}, [CVE-2023-2612](https://nvd.nist.gov/vuln/detail/CVE-2023-2612){: external}, [CVE-2023-2650](https://nvd.nist.gov/vuln/detail/CVE-2023-2650){: external}, [CVE-2023-29491](https://nvd.nist.gov/vuln/detail/CVE-2023-29491){: external}, [CVE-2023-30456](https://nvd.nist.gov/vuln/detail/CVE-2023-30456){: external}, [CVE-2023-31436](https://nvd.nist.gov/vuln/detail/CVE-2023-31436){: external}, [CVE-2023-32233](https://nvd.nist.gov/vuln/detail/CVE-2023-32233){: external}. |
| Kubernetes | N/A |N/A|N/A|
{: caption="Changes since version 1.27.2_1526" caption-side="bottom"}


### Master fix pack 1.27.2_1524 and worker node fix pack 1.27.2_1526, released 24 May 2023
{: #1.27.2_1524M_and_1.27.2_1526W}

| Component | Previous | Current | Description |
| --- | --- | --- | --- |
| etcd configuration | N/A | N/A | Improved etcd probe configurations. |
| IBM Cloud Controller Manager | v1.26.4-7 | v1.27.1-8 | Updated to support the Kubernetes `1.27.1` release. Updated `Go` dependencies and to `Go` version `1.20.3`. Base image updated. Increased default number of concurrent node and service sync workers. VPC load balancer updates can now be complete asynchronously. |
| Kubernetes | v1.26.5 | v1.27.2 | See the [Kubernetes release notes](https://github.com/kubernetes/kubernetes/releases/tag/v1.27.2). |
| Kubernetes add-on resizer | 1.8.16 | 1.8.18 | See the [Kubernetes add-on resizer release notes](https://github.com/kubernetes/autoscaler/releases/tag/addon-resizer-1.8.18). |
| Kubernetes CSI snapshot controller and CRDs | v6.0.1 | v6.2.1 | See the [Kubernetes container storage interface (CSI) snapshotter release notes](https://github.com/kubernetes-csi/external-snapshotter/releases/tag/v6.2.1). |
| Kubernetes DNS autoscaler configuration | N/A | N/A | Increased Kubernetes DNS autoscaler memory resource request to `10Mi`. |
| Kubernetes Metrics Server | v0.6.2 | v0.6.3 | See the [Kubernetes Metrics Server release notes](https://github.com/kubernetes-sigs/metrics-server/releases/tag/v0.6.3). |
| Kubernetes NodeLocal DNS cache configuration | N/A | N/A | Increased Kubernetes NodeLocal DNS cache memory resource request to `20Mi`. |
{: caption="Changes since version 1.26." caption-side="bottom"}
