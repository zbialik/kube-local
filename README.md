# A GitOps repository for Local K8s

This repository is meant to be a template for establishing a GitOps repository for a local kubernetes environment (e.g. Minikube, Rancher Desktop, etc.) 

ArgoCD is used for establishing the GitOps pattern. As such, it is the only application that requires manual deployment.

But fear not, the initial deployment includes the creation of the `ApplicationSet` manifest which  so it will immediately start managing itself after initialization.

## Initial Deployment (manual)


```bash
# clone this repo
git clone https://github.com/zbialik/kube-local.git

# generate manifests
helm repo add argo https://argoproj.github.io/argo-helm
helm template argocd argo/argo-cd -f k8s/argocd/argocd/helm/values.yaml -n argocd > k8s/argocd/argocd/generated.yaml

# initial deploy
kubectl apply -k k8s/argocd/argocd
```
