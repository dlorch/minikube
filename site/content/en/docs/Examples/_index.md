
---
title: "Examples"
linkTitle: "Examples"
weight: 3
date: 2017-01-05
description: >
  See minikube in action!
---

Start a cluster by running:

`minikube start`

Access the Kubernetes Dashboard running within the minikube cluster:

`minikube dashboard`

Once started, you can interact with your cluster using `kubectl`, just like any other Kubernetes cluster. For instance, starting a server:

`kubectl run hello-minikube --generator=run-pod/v1 --image=k8s.gcr.io/echoserver:1.4 --port=8080`

Exposing a service as a NodePort

`kubectl expose deployment hello-minikube --type=NodePort`

minikube makes it easy to open this exposed endpoint in your browser:

`minikube service hello-minikube`

Start a second local cluster:

`minikube start -p cluster2`

Stop your local cluster:

`minikube stop`

Delete your local cluster:

`minikube delete`
