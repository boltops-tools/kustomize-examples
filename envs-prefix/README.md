# Simple Prefix Overlays

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