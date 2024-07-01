## Step 1  Install Metric Server
#### $ git clone https://github.com/ashokitschool/k8s_metrics_server
#### $ cd k8s_metrics_server/
#### $ cd deploy/1.8+/
#### $ kubectl apply -f .

## Step 2 Deploy Sample App
```
##### git clone https://github.com/ashokitschool/kubernetes_manifest_yml_files.git
```
##### Here refer HPA file 
##### $ kubectl apply -f deploy.yaml
##### $ kubectl apply -f service.yaml
##### $ kubectl apply -f HPA.yaml     ---> Is used for horizontal pod autoscaling
