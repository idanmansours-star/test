## Argo CD Config

This directory stores Argo CD configuration as code for this cluster.

### Files

- `argocd-cm.yaml` - core Argo CD settings.
- `argocd-rbac-cm.yaml` - RBAC policy and defaults.
- `argocd-cmd-params-cm.yaml` - runtime command parameters.
- `kuber-application.yaml` - Argo CD Application for this project manifests.

### Apply

```bash
kubectl apply -f infra/argocd/argocd-cm.yaml
kubectl apply -f infra/argocd/argocd-rbac-cm.yaml
kubectl apply -f infra/argocd/argocd-cmd-params-cm.yaml
kubectl apply -f infra/argocd/kuber-application.yaml
```

Before applying `kuber-application.yaml`, update `spec.source.repoURL` to your repository URL.
