# Deploying
```bash
argocd app create catfacts-argocd-app \
    --dest-namespace argocd \
    --dest-server https://kubernetes.default.svc \
    --repo https://github.com/brasstax/catfacts-argocd-app.git \
    --path . \
    --sync-policy automated
argocd app sync catfacts-argocd-app
argocd app sync catfacts
```
