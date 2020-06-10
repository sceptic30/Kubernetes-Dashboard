# Kubernetes Dashboard
Automatically Install Kubernetes Dashboard to your Cluster

# Installation
kubectl apply -f https://raw.githubusercontent.com/sceptic30/kubernetes-dashboard/master/install.yaml

# Get the Admin Access Token
kubectl -n kubernetes-dashboard describe secret $(kubectl -n kubernetes-dashboard get secret | grep admin-user | awk '{print $1}')
