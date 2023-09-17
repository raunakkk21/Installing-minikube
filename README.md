# Minikube Install

## Install Dependencies
```
sudo apt-get update && sudo apt-get install -y curl wget virtualbox
```
## Install Kubectl
```
sudo apt-get update && sudo apt-get install -y apt-transport-https
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
```
## Install Minikube
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```
## Verify Installation
```
minikube version
```
## Start Minikube
```
minikube start
```
## Deploy a Sample Application
```
kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
```
