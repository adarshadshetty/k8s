## Setup HPA In K8s Cluster
#### 1. Install Metric Server
#### 2. Deploy Sample App
#### 3. Create Service
#### 4. Deploy HPA
#### 5. Increase Load
#### 6. Monitor HPA Events


##################
## Helm Installation
##################
```
$ curl -fsSl -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
```

```
$ chmod 700 get_helm.sh
```
```
$ ./get_helm.sh
```
```
$ helm
```
-> check do we have metrics server on the cluster

```
$ kubectl top pods
```

```
$ kubectl top nodes
```


# check helm repos 
```
$ helm repo ls
```


# Before you can install the chart you will need to add the metrics-server repo to helm
```
$ helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
```
# Install the chart

```
$ helm upgrade --install metrics-server metrics-server/metrics-server
```

```
$ kubectl top pods
```
```
$ kubectl top nodes
```
```
$ helm list
```
```
$ helm delete <release-name>
```


=========================================
Metric Server Unavailability issue fix
=========================================

```
URL : https://www.linuxsysadmins.com/service-unavailable-kubernetes-metrics/
```


```
$ kubectl edit deployments.apps -n kube-system metrics-server 
```
=> Edit the below file and add  new properties which are given below

--------------------------- Existing File--------------------
```
 spec:
      containers:
      - args:
        - --cert-dir=/tmp
        - --secure-port=4443
```

--------------------------- New File--------------------
```
---
    spec:
      containers:
      - args:
        - --cert-dir=/tmp
        - --secure-port=4443
        - --kubelet-insecure-tls=true
        - --kubelet-preferred-address-types=InternalIP
```
------------------------------------------------------------------

