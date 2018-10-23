# learn-helm

# init project
```console
helm init learn-helm
```

# helm structure
```console
|____templates
| |____ingress.yaml
| |____deployment.yaml ( k8s deployment )
| |____NOTES.txt
| |_____helpers.tpl
| |____service.yaml
|____Chart.yaml ( npm like package.json )
|____.helmignore
|____values.yaml ( store the values map )
|____charts
```

# debug helm chart
```console
helm install learn-helm --dry-run --debug
```

# update helm repo
```console
helm repo update
```

# kubectl useful commend
- kubectl exec -it pod-name bash
- kubectl describe po pod-name
- kubectl get po -o wide
  - it will show the detail of the po
- kubectl config get-contexts
  - it will show all the context
- kubectl config use-context context-name
  - it will switch the context
- kubectl port-forward po-name <host-port>:<pod-port>
