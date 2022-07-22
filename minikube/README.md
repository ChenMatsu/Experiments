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
- minikube start
- minikube stop
- minikube pause
- minikube delete
- minikube addons list
- minikube addons enable \<ADDON_NAME>
- minikube addons disable \<ADDON_NAME>
- minikube addons open \<ADDON_NAME>
- minikube service \<ServiceName> --url

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

<!-- Inspect Pod -->
kubectl describe service <DeploymentName>
```

# Kubectl in minikubte

- minikube kubectl -- get pods
- minikube kubectl -- create deployment \<DeploymentNAme> --image=\<ImageName>
- minikube kubectl -- expose deployment \<DeploymentNAme> --type=\<DeploymentType> --port=\<PORT>
- minikube kubectl --help

# Kubectl

- kubectl get svc

# Categories in minikube

- NodePort
  - Opens a specific port, and any traffic that is sent to this port is forwarded to the service
- LoadBalancer
  - A LoadBalancer service is the standard way to expose a service to the internet. With this method, each service gets its own IP address

# LoadBalancer

- minikube tunnel
- minikube tunnel --cleanup
