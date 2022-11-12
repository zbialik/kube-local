# A GitOps repository for Local K8s

This repository is meant to be a template for establishing a GitOps repository for a local kubernetes environment (e.g. Minikube, Rancher Desktop, etc.) 

ArgoCD is used for establishing the GitOps pattern. As such, it is the only application that requires manual deployment.

But fear not, the initial deployment includes the creation of the `ApplicationSet` manifest which  so it will immediately start managing itself after initialization.

## Initial Deployment (manual)

```bash
git clone https://github.com/zbialik/kube-local.git
kubectl apply -k k8s/argocd/argocd
```
