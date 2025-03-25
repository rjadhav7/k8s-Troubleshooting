# List all the resources in the namespace:
$ kubectl api-resources --verbs=list --namespaced=true -o name \
| xargs -n 1 kubectl get --ignore-not-found --show-kind -n <namespace>
# Delete pod forcefully:
kubectl delete pod <pod-name> --force --grace-period=0
kubectl delete pods --all --force --grace-period=0 -n <namespace-name>
