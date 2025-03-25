# Commands
### Deployment hello-world
```
kubectl -n dev port-forward service/hello-world 8888:80
Enable auto sync and change number of replicas
kubectl exec -it pod/hello-world-67978c67df-b2mdh -n dev -- /bin/bash
```