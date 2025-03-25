# Commands
### Deployment hello-world
```
kubectl -n dev port-forward service/hello-world 8888:80
Enable auto sync and change number of replicas
kubectl exec -it pod/hello-world-67978c67df-b2mdh -n dev -- /bin/bash
```
```
helm lint Lab-01-Helm-Deployment/
helm install app01 Lab-01-Helm-Deployment/ --values Lab-01-Helm-Deployment/values.yaml -f Lab-01-Helm-Deployment/values-dev.yaml --set environment=dev --namespace dev
kubectl get all -n dev
curl 192.168.49.2:30000
helm uninstall app01 -n dev

helm install app01 Lab-01-Helm-Deployment/ --values Lab-01-Helm-Deployment/values.yaml -f Lab-01-Helm-Deployment/values-prd.yaml --set environment=prd --namespace prd
kubectl get all -n prd
curl 192.168.49.2:30500
helm uninstall app01 -n dev
```