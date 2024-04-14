# MVP

## Access To The Application

```sh
kubectl port-forward -n demo svc/ambassador 8088:80&
```

## Download image(example)

```sh
wget -O /tmp/k8s.png https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/kubernetes-icon.png
```

## Convert image

```sh
curl -F 'image=@/tmp/k8s.png' localhost:8088/img/
```
