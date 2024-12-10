# How to setup two-tier application deployment on kubernetes cluster
## First setup kubernetes kubeadm cluster
Use this repository to setup kubeadm https://github.com/LondheShubham153/kubestarter/blob/main/kubeadm_installation.md

## SetUp
- First clone the code to your machine
```bash
git clone https://github.com/LondheShubham153/two-tier-flask-app.git
```
- Move to k8s directory
```bash
cd two-tier-flask-app/k8s
```
- Now, execute below commands one by one
```bash
kubectl apply -f twotier-deployment.yml
```
```bash
kubectl apply -f twotier-deployment-svc.yml
```
```bash
kubectl apply -f mysql-deployment.yml
```
Once Mysql Server is running on kubernetes then access that pod and connect to mysql server and use mentioned DB then use below query then frontend app will work as expected.

CREATE TABLE messages (
    id INT AUTO_INCREMENT PRIMARY KEY,
    message TEXT
);
```bash
kubectl apply -f mysql-deployment-svc.yml

Once you get svc ClusterIP modify it on two tier deployment yml file
```
```bash
kubectl apply -f persistent-volume.yml
```
```bash
kubectl apply -f persistent-volume-claim.yml
```
