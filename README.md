## ToDo
https://tanzu.vmware.com/developer/guides/ci-cd/tekton-gs-p2/
Kaniko Build
```
kubectl create secret docker-registry dockercreds \
  --docker-server='index.docker.io' \
  --docker-username=cjineson \
  --docker-password=<PASSWORD> \
  --docker-email=chrisineson@gmail.com
kubectl apply -f kaniko-build.yaml
tkn taskrun logs --last -f
```


## Tekton Catalog
### Kaniko task
```
kubectl apply -f https://raw.githubusercontent.com/tektoncd/catalog/master/task/kaniko/0.2/kaniko.yaml
```

## tektoncd-operator
https://operatorhub.io/operator/tektoncd-operator

```
curl -sL https://github.com/operator-framework/operator-lifecycle-manager/releases/download/v0.17.0/install.sh | bash -s v0.17.0
kubectl create -f https://operatorhub.io/install/tektoncd-operator.yaml
kubectl get csv -n operators
```
--> better? https://artifacthub.io/packages/olm/community-operators/tektoncd-operator
