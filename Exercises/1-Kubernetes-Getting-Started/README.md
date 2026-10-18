# Exercise 1 – Hello Pod

## Objective

Deploy an Nginx container as a Kubernetes Pod using Minikube, expose it using a NodePort Service, and access the application through a web browser.

## Environment

* OS: Windows 11
* Kubernetes: v1.35.1
* Minikube: v1.38.1
* Container Runtime: Docker
* Application: Nginx

## 1. Start Minikube

Start the local Kubernetes cluster:

```bash
minikube start
```

Minikube successfully started using Docker as the container driver, and `kubectl` was configured to use the Minikube cluster.

## 2. Create the Pod

Create a Pod named `hello-k8s` using the Nginx image:

```bash
kubectl run hello-k8s --image=nginx --port=80
```

Output:

```text
pod/hello-k8s created
```

## 3. Verify the Pod

Check the status of the Pod:

```bash
kubectl get pods
```

The Pod successfully reached the `Running` state:

```text
NAME        READY   STATUS    RESTARTS
hello-k8s   1/1     Running   0
```

The `1/1` status indicates that the Nginx container is ready and running.

![Kubernetes Deployment](screenshots/01-kubernetes-deployment.png)

## 4. Expose the Pod

Expose the Pod using a NodePort Service:

```bash
kubectl expose pod hello-k8s --type=NodePort --port=80
```

Output:

```text
service/hello-k8s exposed
```

The Pod is now accessible through the Kubernetes Service.

## 5. Access the Application

Open the Service using Minikube:

```bash
minikube service hello-k8s
```

Minikube created a tunnel for the Service and opened the application in the browser.

The Nginx welcome page was successfully displayed:

![Nginx Welcome Page](screenshots/02-nginx-welcome-page.png)

## 6. Kubernetes Working

The basic flow for creating the Pod is:

```text
kubectl
   ↓
Kubernetes API Server
   ↓
etcd
   ↓
Scheduler
   ↓
Worker Node
   ↓
Kubelet
   ↓
Container Runtime
   ↓
Nginx Container
```

* `kubectl` sends the Pod creation request to the Kubernetes API Server.
* The cluster state is maintained in `etcd`.
* The Scheduler selects a node for the Pod.
* The Kubelet on the selected node ensures that the Pod is running.
* The container runtime creates the Nginx container.
* The Nginx application runs on port `80`.
* The NodePort Service provides access to the Pod.

## 7. Commands Used

```bash
minikube start

kubectl run hello-k8s --image=nginx --port=80

kubectl get pods

kubectl expose pod hello-k8s --type=NodePort --port=80

minikube service hello-k8s
```

## 8. Result

The Nginx application was successfully deployed as a Kubernetes Pod on Minikube.

The Pod reached the `Running` state, was exposed using a NodePort Service, and the Nginx welcome page was successfully accessed through the browser.
