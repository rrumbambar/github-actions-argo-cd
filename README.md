# Deployment Workflow for `hello-app` with ArgoCD

This repository demonstrates deployment workflow with ArgoCD

The `.github/workflows/ci-cd-workflow.yaml` file automates this workflow:
- Builds the Docker image.
- Pushes the image to a registry.
- Updates Kubernetes manifests with the new Docker image tag using Kustomize.
- Pushes updated Kubernetes resource files to the repository.
- ArgoCD applies the updated manifests for deployment in cluster.

---

For manual deployment steps, Kubernetes manifests are located in the `k8s/` directory.