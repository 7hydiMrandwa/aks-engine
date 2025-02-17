# AKS Engine - Units of Kubernetes on Azure!

[![Build Status](https://msazure.visualstudio.com/One/_apis/build/status/Custom/Compute/ContainerService/AKS%20Engine%20CI%20E2E?branchName=master)](https://msazure.visualstudio.com/One/_build/latest?definitionId=50661&branchName=master)
[![GoDoc](https://godoc.org/github.com/Azure/aks-engine?status.svg)](https://godoc.org/github.com/Azure/aks-engine)
[![Go Report Card](https://goreportcard.com/badge/github.com/Azure/aks-engine)](https://goreportcard.com/report/github.com/Azure/aks-engine)

## Project status

This project is deprecated for Azure public cloud customers. Please consider using [Azure Kubernetes Service (AKS)](https://azure.microsoft.com/en-us/services/kubernetes-service/#overview) for managed Kubernetes or [Cluster API Provider Azure](https://github.com/kubernetes-sigs/cluster-api-provider-azure) for self-managed Kubernetes. There are no new features planned; this project will only be updated for CVEs & similar, with Kubernetes 1.24 as the final version to receive updates.

For use on the [Azure Stack Hub product](https://docs.microsoft.com/en-us/azure-stack/user/azure-stack-kubernetes-aks-engine-overview) this project is fully supported and will continue to be supported by the Hub team throughout the lifespan of Azure Stack Hub. Development is already moved to a new Azure Stack Hub specific repository ([Azure/aks-engine-azurestack](https://github.com/Azure/aks-engine-azurestack)). This new repository is where new [releases](https://github.com/Azure/aks-engine-azurestack/releases) for Azure Stack Hub clouds, starting at v0.75.3, will be published and where [issues](https://github.com/Azure/aks-engine-azurestack/issues/new) concerning Azure Stack Hub should be created.

## Overview

AKS Engine is an ARM template-driven way to provision a self-managed Kubernetes cluster on Azure. By leveraging [ARM (Azure Resource Manager)][ARM], AKS Engine helps you create, destroy and maintain clusters provisioned with basic IaaS resources in Azure. AKS Engine has limited support for ongoing operational capabilities such as scaling, in-place upgrade, and extensions. The [Cluster API Provider for Azure a.k.a. CAPZ](https://capz.sigs.k8s.io/) provides more complete operational capabilities. AKS Engine remains the tool for managing Kubernetes clusters on Azure Stack Hub as CAPZ does not yet work there.

## Getting started

- Read the [CLI Overview](docs/tutorials/cli-overview.md) for a list of features provided by the `aks-engine` command line tool.

- The [Quickstart Guide](docs/tutorials/quickstart.md) describes how to download the latest release of `aks-engine` for your environment, and demonstrates how to use `aks-engine` to create a Kubernetes cluster on Azure that you will manage and customize.

- The [complete body of documentation can be found here][docs].

Please see the [FAQ][] for answers about AKS Engine and its progenitor ACS-Engine.

## Join the community

We encourage AKS Engine users to evaluate moving to AKS or to CAPZ, per the [project status](#project-status).

For existing users of AKS Engine, the [community guide][community] and [developer guide][developer-guide] are available, as is the [#aks-engine-dev Slack channel](https://kubernetes.slack.com/archives/CU1CXUHN0).

## Support

Please see our [support policy][support-policy].

## Code of conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information, see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Data Collection
The software may collect information about you and your use of the software and send it to Microsoft. Microsoft may use this information to provide services and improve our products and services. You may turn off the telemetry [as described in the repository][telemetry-config]. There are also some features in the software that may enable you and Microsoft to collect data from users of your applications. If you use these features, you must comply with applicable law, including providing appropriate notices to users of your applications together with a copy of Microsoft's privacy statement. Our privacy statement is located at https://go.microsoft.com/fwlink/?LinkID=824704. You can learn more about data collection and use in the help documentation and our privacy statement. Your use of the software operates as your consent to these practices.

For more information, please see the [telemetry documentation][telemetry].

[ARM]: https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-overview
[community]: docs/community/README.md
[developer-guide]: docs/community/developer-guide.md
[docs]: docs/README.md
[FAQ]: docs/faq.md
[support-policy]: SUPPORT.md
[tutorials]: docs/tutorials/README.md
[telemetry]: docs/topics/telemetry.md
[telemetry-config]: docs/topics/telemetry.md#configuration
