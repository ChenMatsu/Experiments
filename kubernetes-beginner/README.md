# Kubernetes

- Operation System
  - OS Kernel

## Orchestration Technologies

1. Docker Swarm
2. Kubernetes
3. Mesos

## K8s Architecture

- Node(Minion): A machine where containers belong to
- Cluster: Multiple nodes
- Master: Manage clusters

## K8s Components

- APIs Server: K8s frontend
- etcd: Key-Value store
- Kubelet: Agent that runs its node on cluster, making sure container run
- Container Runtime: Run containers (Ex: Docker, Rkt, CRI-O )
- Controller: Brain behind orchestration
- Schedular: Distribute container across multiple nodes

## K8s Workers

- Master
  - kube-apiserver
- Worker Nodes
  - kubelet

## K8s Pods
Pods are the smallest deployable units of computing that you can create and manage in Kubernetes.
