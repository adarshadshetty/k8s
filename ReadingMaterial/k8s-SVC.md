#### What is a kubernetes services and when we need it
-> Each pod has its own IP address
-> Pods are ephmeral - are destroyed frequentky 

Service:->
-> Stable IP address
-> Load balancing 
-> Loose Coupling 
-> Within and outside cluster



#### Different service type
cluster IP service -> Internal service\ 
headless service\
node port service\
Load Balancer service\

#### Differences between them and when to use which one ?

# ClusterIP Service 
-> Default service 
![Screenshot 2024-07-08 181443](https://github.com/adarshadshetty/k8s/assets/136900544/28274291-60bf-4139-8314-89f26178e573)

#####

![Screenshot 2024-07-08 181726](https://github.com/adarshadshetty/k8s/assets/136900544/4561bd1c-a08c-4153-896b-00814a367151)

-> Service Port is Arbitrary
-> targetPort must match the port the container is litening at ! 

![image](https://github.com/adarshadshetty/k8s/assets/136900544/8d04390a-7450-4a6a-b38c-0766672717d1)


```
kubectl get endpoints
```
![Screenshot 2024-07-08 182155](https://github.com/adarshadshetty/k8s/assets/136900544/a310e4fc-323b-4913-8887-4d2a01cb74e5)
![Screenshot 2024-07-08 182204](https://github.com/adarshadshetty/k8s/assets/136900544/c506a920-0cd2-41ed-95df-9108bdbe8381)


# Multi-Port Services
