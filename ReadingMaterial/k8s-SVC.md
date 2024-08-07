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
-> ClusterIP Ip are acessible only within the service 
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
-> Use of name attribute in the service 
![Screenshot 2024-07-08 182429](https://github.com/adarshadshetty/k8s/assets/136900544/d2bad965-d71e-404b-82b2-ea58cb9fb7f7)
![Screenshot 2024-07-08 182451](https://github.com/adarshadshetty/k8s/assets/136900544/6c91a956-2007-4f5f-ada3-95e1d9e43b3d)

# Headless Services
-> Client wants to communicate with 1 specific pod directly /
-> Pods want to talk directly with a specific Pod /
-> Not randomly selected /
-> Use Case : Stateful applications like databases like mysql , mongodb , elastic stack /

![Screenshot 2024-07-08 183033](https://github.com/adarshadshetty/k8s/assets/136900544/a60aa89e-c6d8-465b-af0a-509295796b2d)
![Screenshot 2024-07-08 183134](https://github.com/adarshadshetty/k8s/assets/136900544/4577ad93-ba7e-4334-9138-2ea5453e4584)
![Screenshot 2024-07-08 183154](https://github.com/adarshadshetty/k8s/assets/136900544/e9184bce-f24b-4115-b47b-bdc02f602b15)
![Screenshot 2024-07-08 183324](https://github.com/adarshadshetty/k8s/assets/136900544/3edf3459-394f-41aa-b90f-cfb9c8c9b029)

# NodePort Services 
NodePort Range => 30000 - 32767.
Here ClusterIP Service is automatically created.
NodePort Service is not secure , external client may access the SVC
![Screenshot 2024-07-08 191218](https://github.com/adarshadshetty/k8s/assets/136900544/6576d63b-4838-4f92-9901-aadcab59a435)
![Screenshot 2024-07-08 193518](https://github.com/adarshadshetty/k8s/assets/136900544/4c10b363-620e-4817-8519-7a9d57dfecae)


# LoadBalancer Service
#### ->Beacome Accessible exteenally through cloud providers LB
#### -> NodePort and ClusterIP service are created automatically !

![Screenshot 2024-07-08 193820](https://github.com/adarshadshetty/k8s/assets/136900544/5ea01c64-d100-4139-998a-0808b88fc734)
![Screenshot 2024-07-08 193833](https://github.com/adarshadshetty/k8s/assets/136900544/150bdd1e-a84b-424a-a167-2b7421a5b14f)


# Wrap-Up
![Screenshot 2024-07-08 194013](https://github.com/adarshadshetty/k8s/assets/136900544/b118b3e8-eac3-47aa-bb26-13abde27bbae)
