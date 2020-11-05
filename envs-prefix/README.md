# Simple Prefix Overlays

[![BoltOps Badge](https://img.boltops.com/boltops/badges/boltops-badge.png)](https://www.boltops.com)

Blog Post: [Kustomize vs Helm vs Kubes: Kubernetes Deploy Tools](https://blog.boltops.com/2020/11/05/kustomize-vs-helm-vs-kubes-kubernetes-deploy-tools)

Simple overlays example with prefix to separate environments like dev and prod.

## Structure

    ├── base
    │   ├── deployment.yaml
    │   ├── kustomization.yaml
    │   └── service.yaml
    └── overlays
        ├── dev
        │   ├── deployment.yaml
        │   └── kustomization.yaml
        └── prod
            ├── deployment.yaml
            └── kustomization.yaml

## Apply

    kubectl apply -k overlays/dev
    kubectl apply -k overlays/prod