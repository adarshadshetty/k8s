### NameSpace 
```
kubectl get namespace
```


```
ubuntu@ip-172-31-51-210:~$ kubectl get ns
NAME              STATUS   AGE
default           Active   2d2h
kube-node-lease   Active   2d2h
kube-public       Active   2d2h
kube-system       Active   2d2h
ubuntu@ip-172-31-51-210:~$
```

#### kube-system  
Do not create modify in the kube-system
system process
control plane and kubectl processes

#### kube-public 
It contain the publicly accessible data
A ConfigMap, Which contains cluster information 
```
kubectl cluster-info
```

#### kube-node-lease
It holds the info about the heartbeats of the Nodes
Each Nde has associate lease object in namespace
Determines the availability of a Node

####  default Namespace
Resource you created are located here by default if you are not created the namespace /

##### create a new ns
```
kubectl create namespace my-namespace
```

Another way to create a namespace is through yaml / 
Create a name space with a configuration file /
```
apiVersion: v1
kind: Namespace
metadata:
  name: my-namespace
```

#### What are ns why this ns is needed
Group the resources into namespaces like Database , Monitoring , Elastic Stack , Nginx-Ingress  namespace \
Do not use the ns for smaller project \
use ns if you have multiple teams in a same application \
resources sharing : staging and development \
Use the ns when your are using the blue-green deployment \
Access and resource limits on NameSpace \



