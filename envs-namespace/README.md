# Simple Namespace Overlays

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
    kubectl apply -k overlays/dev