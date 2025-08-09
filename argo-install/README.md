

check argo configs
```sh
helm repo add argo https://argoproj.github.io/argo-helm
helm repo update
helm search repo argocd
helm search repo argo/argo-cd --versions | head -n 11
helm show values argo/argo-cd --version 8.2.7 > argocd-defaults.yaml
```

```
helm search repo argo/argo-cd --versions | head -n 11

helm install argocd argo/argo-cd \
  --namespace argocd \
  --create-namespace \
  --version 8.2.7 \
  -f argo-install/values.yaml
```