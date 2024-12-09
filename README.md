**Follow below for Deploy Prometheus & Grafana in AWS EKS **
Link: https://www.coachdevops.com/2022/05/how-to-setup-monitoring-on-kubernetes.html

**Install Nginx Ingress Controller**

- helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
- helm repo update
- helm install ingress-nginx ingress-nginx/ingress-nginx --namespace ingress-nginx --create-namespace
- kubectl get all -n ingress-nginx
- kubectl get svc -n ingress-nginx

**Install Cert-Manager**

- helm repo add jetstack https://charts.jetstack.io
- helm repo update
- helm install cert-manager jetstack/cert-manager --namespace cert-manager --create-namespace --set installCRDs=true
- kubectl get all -n cert-manager
- kubectl get svc -n cert-manager
