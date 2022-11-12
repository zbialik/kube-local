# ArgoCD Manifests

Generate manifests with `helm template` like so:

```bash
helm repo add argo https://argoproj.github.io/argo-helm
helm template argocd argo/argo-cd -f helm/values.yaml > generated.yaml
```
