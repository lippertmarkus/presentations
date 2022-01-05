Download from https://github.com/argoproj/argo-workflows/releases/download/v3.2.6/argo-windows-amd64.gz
extract and place in path

Install Argo:
```
helm repo add argo https://argoproj.github.io/argo-helm
helm install argo-workflows argo/argo-workflows --version 0.9.4 -n argo --create-namespace --set server.serviceType=LoadBalancer --set workflow.serviceAccount.name=default --set controller.containerRuntimeExecutor=emissary
```

get external ip and Open UI:
```
kubectl get svc -n argo
open http://20.103.68.56:2746
```

Get Token:
```
argo.exe auth token
```

Authenticate with that token.


TODO WORKFLOW

--------


