---

copyright: 
  years: 2014, 2025
lastupdated: "2025-04-29"


keywords: kubernetes, help, network, connectivity

subcollection: containers

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}





# Checking the status of Ingress components
{: #ingress-status}
{: support}

[Virtual Private Cloud]{: tag-vpc} [Classic infrastructure]{: tag-classic-inf}

## Getting the status and message
{: #check_status}

To check the overall health and status of your cluster's Ingress components:
{: shortdesc}

```sh
ibmcloud ks ingress status-report get -c <cluster_name_or_ID>
```
{: pre}

The state of the Ingress components are reported in an **Ingress Status** and **Ingress Message**.

Example output


```sh
Ingress Status:   healthy
Message:          All Ingress components are healthy.

Cluster                        Status
ingress-controller-configmap   healthy
alb-healthcheck-ingress        healthy

Subdomain                                                                           Status
example-ae7743ca70a399d9cff4eaf617434c72-0000.us-south.containers.appdomain.cloud   healthy

ALB                                  Status
public-crad7rd4m219nv1vtgdivg-alb1   healthy

Secret                                          Namespace           Status
example-ae7743ca70a399d9cff4eaf617434c72-0000   ibm-cert-store      healthy
example-ae7743ca70a399d9cff4eaf617434c72-0000   default             healthy
example-ae7743ca70a399d9cff4eaf617434c72-0000   kube-system         healthy
```
{: screen}









The **Ingress Status** and **Ingress Message** fields are also returned in the output of the `ibmcloud ks cluster get` command. 
{: tip}


## Ingress statuses
{: #ingress_status}

The Ingress Status reflects the overall health of the Ingress components.
{: shortdesc}

| Ingress status | Description |
|--- | --- |
| `healthy` | The Ingress components are healthy.|
| `warning` | Some Ingress components might not function properly.|
| `critical` | Some Ingress components are malfunctioning.|
| `disabled` | Ingress status reporting is disabled. You can turn it on using the `ibmcloud ks ingress status-report enable` command.|
| `unsupported`| Ingress status reporting is not available for unsupported cluster versions. |
| `unknown`| The system is unable to calculate the Ingress status. |
{: caption="Ingress statuses" caption-side="bottom"}


## Ingress messages
{: #ingress_message}

The Ingress message provides details of what operation is in progress or information about any components that are unhealthy. Each status and message is described in the following tables.
{: shortdesc}

|Ingress message|Description|
|--- |--- |
| `The load balancer service is missing (ERRSNF).` | For more information, see [Why does the Ingress status show an ERRSNF error?](/docs/containers?topic=containers-ts-ingress-errsnf).|
| `The Ingress controller ConfigMap is not found on the cluster (ERRICCNF).` | For more information, see [Why does the Ingress status show an ERRICCNF error?](/docs/containers?topic=containers-ts-ingress-erriccnf).|
| `The ALB version is no longer supported (ERRAVUS).` | For more information, see [Why does the Ingress status show an ERRAVUS error?](/docs/containers?topic=containers-ts-ingress-erravus).|
| `The ALB deployment is not found on the cluster (ERRADNF).` | For more information, see [Why does the Ingress status show an ERRADNF error?](/docs/containers?topic=containers-ts-ingress-erradnf).|
| `One or more ALB pod is not in running state (ERRADRUH).` | For more information, see [Why does the Ingress status show an `ERRADRUH` error?](/docs/containers?topic=containers-ts-ingress-erradruh).|
| `The ALB health Ingress resource is not found on the cluster (ERRAHINF).` | For more information, see [Why does the Ingress status show an ERRAHINF error?](/docs/containers?topic=containers-ts-ingress-errahinf).|
| `The ALB health service is not found on the cluster (ERRAHSNF).` | For more information, see [Why does the Ingress status show an ERRAHSNF error?](/docs/containers?topic=containers-ts-ingress-errahsnf).|
| `The ALB is unable to respond to health requests (ERRAHCF).` | For more information, see [Why does the Ingress status show an ERRAHCF error?](/docs/containers?topic=containers-ts-ingress-errahcf).|
| `Autoscaling is ineffective (ERRHPAETPI).` | For more information, see [Why does the Ingress status show an ERRHPAETPI error?](/docs/containers?topic=containers-ts-ingress-errhpaetpi).|
| `The cluster does not have enough worker nodes to satisfy the autoscaling configuration (ERRHPAIWC).` | For more information, see [Why does the Ingress status show an ERRHPAIWC error?](/docs/containers?topic=containers-ts-ingress-errhpaiwc).|
| `Autoscaling is failing (ERRHPANA).` | For more information, see [Why does the Ingress status show an ERRHPANA error?](/docs/containers?topic=containers-ts-ingress-errhpana).|
| `The autoscaler resource is missing (ERRHPANF).` | For more information, see [Why does the Ingress status show an ERRHPANF error?](/docs/containers?topic=containers-ts-ingress-errhpanf).|
| `The load balancer service address is missing (ERRSAM).` | For more information, see [Why does the Ingress status show an ERRSAM error?](/docs/containers?topic=containers-ts-ingress-errsam).|
| `Could not access {{site.data.keyword.secrets-manager_short}} instance (ESSSMI).` | For more information, see [Why does the Ingress status show an ESSSMI error?](/docs/containers?topic=containers-ts-ingress-esssmi).|
| `Could not access the secret group (ESSSMG).` | For more information, see [Why does the Ingress status show an ESSSMG error?](/docs/containers?topic=containers-ts-ingress-esssmg).|
| `The CRN does not match the default secret with the same domain (ESSVC).` | For more information, see [Why does the Ingress status show an ESSVC error?](/docs/containers?topic=containers-ts-ingress-essvc).|
| `The certificate for TLS secret expired or will expire soon (ESSEC).` | For more information, see [Why does the Ingress status show an ESSEC error?](/docs/containers?topic=containers-ts-ingress-essec).|
| `The Opaque secret field expired or will expire soon (ESSEF).` | For more information, see [Why does the Ingress status show an ESSEF error?](/docs/containers?topic=containers-ts-ingress-essef).|
| `The secret status shows a warning (ESSWS).` | For more information, see [Why does the Ingress status show an ESSWS error?](/docs/containers?topic=containers-ts-ingress-essws).|
| `The secret is not present on the cluster or is in the wrong namespace (ESSDNE).` | For more information, see [Why does the Ingress status show an ESSDNE error?](/docs/containers?topic=containers-ts-ingress-essdne).|
| `The external provider for the given subdomain has authorization issues (ERRDSAISS).` | For more information, see [Why does the Ingress status show an ERRDSAISS error?](/docs/containers?topic=containers-ts-ingress-errdsaiss)|
| `The subdomain has TLS secret issues (ERRDSISS).` | For more information, see [Why does the Ingress status show an ERRDSISS error?](/docs/containers?topic=containers-ts-ingress-errdsiss).|
| `The subdomain has DNS resolution issues (ERRDRISS).` | For more information, see [Why does the Ingress status show an ERRDRISS error?](/docs/containers?topic=containers-ts-ingress-errdriss).|
| `The subdomain has incorrect addresses registered (ERRDSIA).` | For more information, see [Why does the Ingress status show an ERRDSIA error?](/docs/containers?topic=containers-ts-ingress-errdsia).|
| `Invalid value for ALB version. (E0061).` | Before updating an ALB, check the list of ingress image versions available in the region using the command `ibmcloud ks ingress alb versions --region <region_id>`. For more information, see [Managing ALBs](/docs/containers?topic=containers-ingress-alb-manage).|
{: caption="Ingress messages" caption-side="bottom"}
