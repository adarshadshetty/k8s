# Project Execution Details.

### Create a 'mysql' helm-chart
```
helm create mysql-database
```
### Package the mysql helm-chart
```
helm package mysql-database
```
### Install the mysql chart
```
helm install mysql mysql-database
```
### Create the flask-app helm-chart
```
helm create  flask-app
```
### Package the flask-app 
```
helm package flask-app
```
### Install the flask-app
```
helm install python-app flask-app
```

```
helm list
```
![Screenshot 2024-08-02 092227](https://github.com/user-attachments/assets/0994014b-6c42-4621-bc40-7ddd6456d3f5)


```
kubectl get all
```
![Screenshot 2024-08-02 092416](https://github.com/user-attachments/assets/d49d6192-3c56-4750-818e-62dcbb08a217)

```
kubectl get svc
kubectl get pods
kubectl get deployment
```
![Screenshot 2024-08-02 092501](https://github.com/user-attachments/assets/b44a9e8d-eccf-438d-8902-3c2e30caa702)



```
helm list
```
![Screenshot 2024-08-02 092047](https://github.com/user-attachments/assets/6018ee8e-3bc0-491f-a209-cb57a10a767c)

```
docker exec -it <mysql-container-id> bash
mysql -u admin -u
<give password>
show databases;
use mydb
show tables;
```
![Screenshot 2024-08-02 091518](https://github.com/user-attachments/assets/918da4be-ca9e-4eb4-8941-ed3381328912)


```
localhost 30007
```
![Screenshot 2024-08-02 092546](https://github.com/user-attachments/assets/026d9edf-368b-4551-9031-575f8f2ba57f)


