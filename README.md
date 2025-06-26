# Kubernetes Dashboard

## But du cours
Ce projet vise à déployer un cluster Kubernetes local avec un tableau de bord graphique pour la gestion des conteneurs.

## Étapes en détails

1. Déployer un cluster Kubernetes local avec Minikube.
   - Installer Minikube : 
[Kubernetes Dashboard KWANTWOO WILLIAMS.pdf](https://github.com/user-attachments/files/20925966/Kubernetes.Dashboard.KWANTWOO.WILLIAMS.pdf)


     choco install minikube
  
   - Installer Kubernetes CLI : 
 
     choco install kubernetes-cli
  
2. Activer le dashboard :
 
   minikube dashboard

3.  Activer le metrics server :
minikube addons enable metrics-server

4. Déployer une application NGINX scalable avec HPA :
kubectl create deployment webapp --image=nginx
kubectl expose deployment webapp --type=NodePort --port=80
kubectl autoscale deployment webapp --cpu-percent=50 --min=1 --max=5

URL  : http://127.0.0.1:53248/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/workloads?namespace=default
