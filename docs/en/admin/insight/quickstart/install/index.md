---
MTPE: ModetaNiu
DATE: 2024-07-19
---

# Start Observing

AI platform enables the management and creation of multicloud and multiple clusters.
Building upon this capability, Insight serves as a unified observability solution for
multiple clusters. It collects observability data from multiple clusters by deploying the insight-agent
plugin and allows querying of metrics, logs, and trace data through the AI platform Insight.

 __insight-agent__ is a tool that facilitates the collection of observability data from multiple clusters.
Once installed, it automatically collects metrics, logs, and trace data without any modifications.

Clusters created through __Container Management__ come pre-installed with insight-agent. Hence,
this guide specifically provides instructions on enabling observability for integrated clusters.

- [Install insight-agent online](install-agent.md)

As a unified observability platform for multiple clusters, Insight's resource consumption of certain components 
is closely related to the data of cluster creation and the number of integrated clusters.
When installing insight-agent, it is necessary to adjust the resources of the proper components based on the cluster size.

1. Adjust the CPU and memory resources of the __Prometheus__ collection component in insight-agent
   according to the size of the cluster created or integrated. Please refer to
   [Prometheus resource planning](../res-plan/prometheus-res.md).

2. As the metric data from multiple clusters is stored centrally, AI platform administrators
   need to adjust the disk space of __vmstorage__ based on the cluster size.
   Please refer to [vmstorage disk capacity planning](../res-plan/vms-res-plan.md).

- For instructions on adjusting the disk space of vmstorage, please refer to
  [Expanding vmstorage disk](../res-plan/modify-vms-disk.md).

Since AI platform supports the management of multicloud and multiple clusters,
insight-agent has undergone partial verification. However, there are known conflicts
with monitoring components when installing insight-agent in Suanova 4.0 clusters and
Openshift 4.x clusters. If you encounter similar issues, please refer to the following documents:

- [Install insight-agent in Suanova 4.0.x](../other/install-agentindce.md)
- [Install insight-agent in Openshift 4.x](../other/install-agent-on-ocp.md)

Currently, the insight-agent collection component has undergone functional testing
for popular versions of Kubernetes. Please refer to:

- [Kubernetes cluster compatibility testing](../../compati-test/k8s-compatibility.md)
- [Openshift 4.x cluster compatibility testing](../../compati-test/ocp-compatibility.md)
- [Rancher cluster compatibility testing](../../compati-test/rancher-compatibility.md)
