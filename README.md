# Installation Guide 

# The following resources are required for a generic deployment

```
kubectl create -f  ingress-nginx/namespace.yaml
```
```
kubectl create -f  ingress-nginx/default-backend.yaml
```
```
kubectl create -f  ingress-nginx/configmap.yaml
```
```
kubectl create -f  ingress-nginx/tcp-services-configmap.yaml
```
```
kubectl create -f  ingress-nginx/udp-services-configmap.yaml
```
# Install with RBAC roles

```
sh ingress-nginx/patch.sh 
```
```
kubectl create -f  ingress-nginx/service.yaml 
```
```
kubectl create -f  ingress-nginx/patch-service-with-rbac.yaml 
```
```
kubectl create -f  ingress-nginx/rbac.yaml 
```
```
kubectl create -f  ingress-nginx/with-rbac.yaml 
```
# Free self-renewing SSL certificate with kube-lego 
```
kubectl create -f kube-lego/configmap.yaml
```
```
kubectl create -f kube-lego/deployment.yaml
```
```
kubectl create -f kube-lego/namespace.yaml
```

# Deploy apps with Ingress

```
kubectl create -f app/ingress.yaml
```
```
kubectl create -f app/jenkins.yml
```
```
kubectl create -f app/service.yml
```
