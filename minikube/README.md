# Minikube Installation
```
<!-- Mac ARM64 -->
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-arm64
sudo install minikube-darwin-arm64 /usr/local/bin/minikube
```
> kubectl will be configured to use **minikube** cluster once minikube is installed

- kubectl get po -A => minikube kubectl -- get po -A
  - Configure command `alias kubectl="minikube kubectl --"`

# Minikube Basic Command
- minikube dashboard

# Minikube Sample Deplyoment
```
kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver:1.4
kubectl expose deployment hello-minikube --type=NodePort --port=8080

<!-- Access Service -->
minikube service hello-minikube
kubectl port-forward service/hello-minikube 7080:8080

<!-- Get / Delete Deployment -->
minikube kubectl -- get deployments
minikube kubectl -- delete deployment <DeploymentName>
```


