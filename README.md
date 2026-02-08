# Apache Helm Chart

[![Helm Version](https://img.shields.io/badge/Helm-3.x-blue.svg?style=flat-square)](https://helm.sh/)
[![Kubernetes Version](https://img.shields.io/badge/Kubernetes-1.24+-green.svg?style=flat-square)](https://kubernetes.io/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

This Helm chart deploys an **Apache HTTP Server** on a Kubernetes cluster.

---

## 🚀 Features

- **Scalable:** Adjust `replicaCount` to scale pods.
- **Configurable Resources:** Customize CPU/memory requests and limits.
- **Flexible Service:** Supports `ClusterIP`, `NodePort`, or `LoadBalancer`.
- **Easy Access:** Quick local access with port forwarding.

---

## 🛠 Prerequisites

- Kubernetes cluster (local, cloud, or KIND)
- `kubectl` installed and configured
- Helm 3 installed

Install Helm 3:

```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh
