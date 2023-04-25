# Kubernetes Tutorial

Kubernetes basic example to assist in learning using [kubernetes/examples](https://github.com/kubernetes/examples) and [kubernetes/client-go](https://github.com/kubernetes/client-go)

## Setup

1. Create cluster using minikube `minikube start`
2. Start the replication controllers and services:
```
$ kubectl create -f redis-master-controller.yaml
$ kubectl create -f redis-master-service.yaml
$ kubectl create -f redis-replica-controller.yaml
$ kubectl create -f redis-replica-service.yaml
$ kubectl create -f guestbook-controller.yaml
$ kubectl create -f guestbook-service.yaml
```

Can check status of services/pods/controllers using kubectl:
```
$ kubectl get pods
$ kubectl get services
$ kubectl get rc
```
3. Launch service with minikube `minikube service guestbook`
