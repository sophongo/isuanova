---
MTPE: windsonsea
Date: 2024-07-19
---

# Cluster Roles

Suanova AI platform categorizes clusters based on different functionalities to help users better manage IT infrastructure.

## Global Service Cluster

This cluster is used to run AI platform components such as
Container Management, Global Management, Insight.
It generally does not carry business workloads.

| Supported Features | Description |
| ------------------ | ----------- |
| K8s Version | 1.22+ |
| Operating System | RedHat 7.6 x86/ARM, RedHat 7.9 x86, RedHat 8.4 x86/ARM, RedHat 8.6 x86;<br>Ubuntu 18.04 x86, Ubuntu 20.04 x86;<br>CentOS 7.6 x86/AMD, CentOS 7.9 x86/AMD |
| Full Lifecycle Management | Supported |
| K8s Resource Management | Supported |
| Cloud Native Storage | Supported |
| Cloud Native Network | Calico, Cillium, Multus, and other CNIs |
| Policy Management | Supports network policies, quota policies, resource limits, disaster recovery policies, security policies |

## Management Cluster

This cluster is used to manage worker clusters and generally does not carry business workloads.

| Supported Features | Description |
| ------------------ | ----------- |
| K8s Version | 1.22+ |
| Operating System | RedHat 7.6 x86/ARM, RedHat 7.9 x86, RedHat 8.4 x86/ARM, RedHat 8.6 x86;<br>Ubuntu 18.04 x86, Ubuntu 20.04 x86;<br>CentOS 7.6 x86/AMD, CentOS 7.9 x86/AMD |
| Full Lifecycle Management | Supported |
| K8s Resource Management | Supported |
| Cloud Native Storage | Supported |
| Cloud Native Network | Calico, Cillium, Multus, and other CNIs |
| Policy Management | Supports network policies, quota policies, resource limits, disaster recovery policies, security policies |

## Worker Cluster

This is a cluster created using Container Management and is mainly used to
carry business workloads. This cluster is managed by the management cluster.

| Supported Features | Description |
| ------------------ | ----------- |
| K8s Version | Supports K8s 1.22 and above |
| Operating System | RedHat 7.6 x86/ARM, RedHat 7.9 x86, RedHat 8.4 x86/ARM, RedHat 8.6 x86;<br>Ubuntu 18.04 x86, Ubuntu 20.04 x86;<br>CentOS 7.6 x86/AMD, CentOS 7.9 x86/AMD |
| Full Lifecycle Management | Supported |
| K8s Resource Management | Supported |
| Cloud Native Storage | Supported |
| Cloud Native Network | Calico, Cillium, Multus, and other CNIs |
| Policy Management | Supports network policies, quota policies, resource limits, disaster recovery policies, security policies |

## Integrated Cluster

This cluster is used to integrate existing standard K8s clusters, including but not limited to self-built clusters
in local data centers, clusters provided by public cloud vendors, clusters provided by private cloud vendors,
edge clusters, Xinchuang clusters, heterogeneous clusters, and different Suanova clusters.
It is mainly used to carry business workloads.

| Supported Features | Description |
| ------------------ | ----------- |
| K8s Version | 1.18+ |
| Supported Vendors | VMware Tanzu, Amazon EKS, Redhat Openshift, SUSE Rancher, Alibaba ACK, Huawei CCE, Tencent TKE, Standard K8s Cluster, Suanova |
| Full Lifecycle Management | Not Supported |
| K8s Resource Management | Supported |
| Cloud Native Storage | Supported |
| Cloud Native Network | Depends on the network mode of the integrated cluster's kernel |
| Policy Management | Supports network policies, quota policies, resource limits, disaster recovery policies, security policies |

!!! note

    A cluster can have multiple cluster roles. For example, a cluster can be both
    a global service cluster and a management cluster or a worker cluster.
