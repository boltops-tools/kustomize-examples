# Simple Namespace Overlays

[![BoltOps Badge](https://img.boltops.com/boltops/badges/boltops-badge.png)](https://www.boltops.com)

Blog Post: [Kustomize vs Helm vs Kubes: Kubernetes Deploy Tools](https://blog.boltops.com/2020/11/05/kustomize-vs-helm-vs-kubes-kubernetes-deploy-tools)

Simple overlays example with namespace to separate environments like dev and prod.

## Structure

    ├── base
    │   ├── deployment.yaml
    │   ├── kustomization.yaml
    │   └── service.yaml
    └── overlays
        ├── dev
        │   ├── deployment.yaml
        │   ├── kustomization.yaml
        │   └── namespace.yaml
        └── prod
            ├── deployment.yaml
            ├── kustomization.yaml
            └── namespace.yaml

## Apply

    kubectl apply -k overlays/dev
    kubectl apply -k overlays/prod