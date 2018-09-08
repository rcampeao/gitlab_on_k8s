# Installing GitLab using Helm
> **Note**: There are currently [known limitations](../../README.md#known-issues-and-limitations) when using this chart, and not all features of GitLab are available.

Install GitLab on Kubernetes with the cloud native GitLab Helm chart. Follow the instructions below to get started.

## Requirements

1. A Kubernetes cluster, version 1.8 or higher.
1. [`kubectl`](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl) version 1.8 or higher, compatible with your cluster. ([+/- 1 minor release from your cluster](https://kubernetes.io/docs/tasks/tools/install-kubectl/#before-you-begin))
1. [`Helm`](https://docs.helm.sh/using_helm/#installing-helm), we recommend v2.9.1 or higher.

## Get started with GitLab

### 1. Prerequisites

In order to install GitLab in a Kubernetes cluster, there are a few required tools. To get started, [prepare your computer](tools.md).

### 2. Where do you want to install GitLab?

Follow the instructions to connect to the Kubernetes cluster of your choice.

> **Note**: [Kubernetes 1.8 or higher is required](#requirements), due to the usage of certain Kubernetes features.

* [Google Kubernetes Engine][]
* [Amazon EKS](../cloud/eks.md)
* Azure Container Service - Documentation to be added.
* Pivotal Container Service - Documentation to be added.
* On-Premises solutions - Documentation to be added.

### 3. Deploy

With the environment setup and configuration generated,
we can proceed to [deployment][]. Or if you are upgrading an existing
installation follow [upgrade docs][]

### 4. Migrate data from an existing GitLab

To migrate your existing GitLab instance to your deployed Kubernetes GitLab instance, take a backup of your existing instance.
Then proceed to the [restore documentation](../backup-restore/README.md#restoring-a-gitLab-installation).

> To obtain a backup tarball of an existing GitLab instance that used other installation methods like an omnibus-gitlab package or GitLab-Omnibus helm chart, follow the instructions [given in documentation](https://docs.gitlab.com/ee/raketasks/backup_restore.html#creating-a-backup-of-the-gitlab-system)
>
> **Note**: If you are restoring a backup taken from another instance, you must migrate your existing instance to using object storage before taking the backup. See [issue 646](https://gitlab.com/charts/gitlab/issues/646)

[Google Kubernetes Engine]: ../cloud/gke.md
[resources]: resources.md
[deployment]: deployment.md
[upgrade docs]: upgrade.md
