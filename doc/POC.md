# Proof of Concept

## ArgoCD

### Install ArgoCD

```sh
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

### Access The Argo CD API Server

```sh
kubectl port-forward svc/argocd-server -n argocd 8080:443&
```

### Get secret to the admin user

```sh
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```

### You need switch to a browser and set next url

```sh
https://127.0.0.1:8080
```

## Demo

![Image](./argocd.gif)
