# ⎈ Apache Helm Chart

![Helm](https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white) ![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)

A **Helm 3 chart** that deploys the **Apache HTTP Server** on Kubernetes with configurable replicas, resources, service type, autoscaling and ingress.

## ✨ Features

- Deployment, Service and ServiceAccount templates
- Optional **HPA**, **Ingress** and **Gateway API HTTPRoute**
- Helm test (`test-connection.yaml`) to verify the release
- Packaged chart: `apache-helm-0.1.0.tgz`

## 📁 Structure

```
apache-helm/
├── Chart.yaml
├── values.yaml
└── templates/
    ├── deployment.yaml  service.yaml  serviceaccount.yaml
    ├── hpa.yaml  ingress.yaml  httproute.yaml
    ├── _helpers.tpl  NOTES.txt
    └── tests/test-connection.yaml
```

## 🚀 Usage

```bash
# install Helm 3
./get_helm.sh

# install the chart
helm install apache ./apache-helm

# customize
helm upgrade apache ./apache-helm --set replicaCount=3 --set service.type=NodePort

# test and access
helm test apache
kubectl port-forward svc/apache-apache-helm 8080:80

# remove
helm uninstall apache
```

---

## 👤 Author

**Abdur Rehman** · DevSecOps Engineer · Founder of [ARTechOps](https://artechops.com)

[LinkedIn](https://www.linkedin.com/in/muhamad-abdur-rehman-81777b366/) · [GitHub](https://github.com/abdur-rehman-tech) · [artechops.com](https://artechops.com)
