Step-5 : Increase the Load
=
$ kubectl get hpa
```
kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://hpa-demo-deployment; done"
```
Note: After executing load generator open Duplicate tab to monitor hpa events

$ kubectl get hpa -w

$ kubectl describe deploy hpa-demo-deployment

$ kubectl get hpa

$ kubectl get events

$ kubectl top pods 

$ kubectl get hpa
