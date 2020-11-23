# argocd-demo-bootstrap

This repository bootstraps a cluster that is already running argocd for the gitops demo. Clone it and run

```
kubectl apply -f bootstrap.yaml
```

The `bootsrap.yaml` manifest will create
- An argocd `Application` resource that syncs all "tenant" applications from an external repository which contains additional argocd `Project` and `Application` resources for each of our cluster tenants and their applications. By default the repository is https://github.com.au/bernos/argocd-demo-environments
