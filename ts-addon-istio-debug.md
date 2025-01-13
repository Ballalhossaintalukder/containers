---

copyright:
  years: 2014, 2025
lastupdated: "2025-01-13"


keywords: kubernetes, help, debug istio, troubleshoot istio, istio add-on debug

subcollection: containers
content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}





# Debugging Istio
{: #istio_debug_tool}
{: support}

[Virtual Private Cloud]{: tag-vpc} [Classic infrastructure]{: tag-classic-inf}

To further troubleshoot the [managed Istio add-on](/docs/containers?topic=containers-istio), consider the following debugging tools.
{: shortdesc}

1. Ensure that your Istio components all run the same version of managed Istio. Whenever the Istio add-on is updated to a new patch or minor version, the Istio control plane is automatically updated, but you must [manually update your data plane components](/docs/containers?topic=containers-istio#update_client_sidecar), including the `istioctl` client and the Istio sidecars for your app.

1. Check your Istio configurations by using the `istioctl analyze` CLI command. For more information about the command, including available command options and examples, see the [Istio open-source documentation](https://istio.io/latest/docs/reference/commands/istioctl/#istioctl-analyze){: external}.

1. In your [cluster dashboard](https://cloud.ibm.com/containers/cluster-management/clusters){: external}, click the name of the cluster where you want to install the debug tool add-on.
1. On the Diagnostics and Debug Tool card, click **Install**.
1. In the dialog box, click **Install**. Note that it can take a few minutes for the add-on to be installed.
1. On the Diagnostics and Debug Tool card, click **Dashboard**.
1. In the debug tool dashboard, select the **istio_control_plane** or **istio_resources**  group of tests. Some tests check for potential warnings, errors, or issues, and some tests only gather information that you can reference while you troubleshoot. For more information about the function of each test, click the information icon next to the test's name.
1. Click **Run**.
1. Check the results of each test. If any test fails, click the information icon next to the test's name for information about how to resolve the issue.
