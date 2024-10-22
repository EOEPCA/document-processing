# Quick Start - Boostrap a deployment on minikube

## Requirements

Before you begin, make sure you have the following tools installed and set up on your local environment:

### Skaffold

Skaffold is used to build, push, and deploy your application to Kubernetes. 

You can install it by following the instructions [here](https://skaffold.dev/docs/install/#standalone-binary).

### Helm

Helm is a package manager for Kubernetes, enabling you to manage Kubernetes applications easily. 

You can install it by following the steps [here](https://helm.sh/docs/intro/install/).

### Minikube

Minikube runs a local Kubernetes cluster, ideal for development and testing. 

You can install it by following the guide [here](https://minikube.sigs.k8s.io/docs/start).

Start your minikube instance with:

```
minikube start
```

### Optional requirements

#### Kubectl

Kubectl is a command-line tool for interacting with Kubernetes clusters. It allows you to manage and inspect cluster resources. While not strictly required, it's highly recommended for debugging and interacting with your Kubernetes environment.

You can install it by following the instructions [here](https://kubernetes.io/docs/tasks/tools/#kubectl).

#### OpenLens

OpenLens is a graphical user interface for managing and monitoring Kubernetes clusters. It provides a visual way to interact with resources. 

While it's optional, it can significantly improve your workflow. You can download it [here](https://github.com/MuhammedKalkan/OpenLens?tab=readme-ov-file#installation).

### Add the helm repositories

```
helm repo add localstack https://helm.localstack.cloud
helm repo add zoo-project https://zoo-project.github.io/charts/
```

### Checking the requirements

After installing these tools, ensure they are available in your terminal by running the following commands:

```bash
skaffold version
helm version
minikube version
```

If all commands return a version, you’re good to go!

## Clone the repository

```
git clone https://github.com/eoap/dev-platform-eoap/
cd dev-platform-eoap/
```

## Run the _OGC API Processes with ZOO Project_ module

Bootstrap the deployment with:
```
cd ogc-api-processes-with-zoo
skaffold dev
```
Wait for the deployment to stablize (1-2 minutes) and the open your browser on the link printed, usually http://127.0.0.1:8000.

The typical output is:

```
No tags generated
Starting deploy...
Helm release zoo-project-dru not installed. Installing...
NAME: zoo-project-dru
LAST DEPLOYED: Tue Oct 22 07:44:52 2024
NAMESPACE: eoap-zoo-project
STATUS: deployed
REVISION: 1
NOTES:
1. Get the application URL by running these commands:
  export POD_NAME=$(kubectl get pods --namespace eoap-zoo-project -l "app.kubernetes.io/name=zoo-project-dru,app.kubernetes.io/instance=zoo-project-dru" -o jsonpath="{.items[0].metadata.name}")
  export CONTAINER_PORT=$(kubectl get pod --namespace eoap-zoo-project $POD_NAME -o jsonpath="{.spec.containers[0].ports[0].containerPort}")
  echo "Visit http://127.0.0.1:8080 to use your application"
  kubectl --namespace eoap-zoo-project port-forward $POD_NAME 8080:$CONTAINER_PORT
Helm release eoap-zoo-project-coder not installed. Installing...
NAME: eoap-zoo-project-coder
LAST DEPLOYED: Tue Oct 22 07:44:54 2024
...
...
 - eoap-zoo-project:statefulset/zoo-project-dru-postgresql: Waiting for 1 pods to be ready...
 - eoap-zoo-project:statefulset/zoo-project-dru-rabbitmq: Waiting for 1 pods to be ready...
 - eoap-zoo-project:statefulset/zoo-project-dru-postgresql is ready. [5/7 deployment(s) still pending]
 - eoap-zoo-project:deployment/eoap-zoo-project-localstack is ready. [4/7 deployment(s) still pending]
 - eoap-zoo-project:statefulset/zoo-project-dru-rabbitmq is ready. [3/7 deployment(s) still pending]
 - eoap-zoo-project:deployment/zoo-project-dru-zoofpm is ready. [2/7 deployment(s) still pending]
 - eoap-zoo-project:deployment/zoo-project-dru-zookernel is ready. [1/7 deployment(s) still pending]
 - eoap-zoo-project:deployment/code-server-deployment is ready.
Deployments stabilized in 51.073 seconds
Port forwarding service/code-server-service in namespace eoap-zoo-project, remote port 8080 -> http://localhost:8000
Port forwarding service/zoo-project-dru-service in namespace eoap-zoo-project, remote port 80 -> http://localhost:8080
No artifacts found to watch
Press Ctrl+C to exit
Watching for changes...
```

Open the link [http://localhost:8000](http://localhost:8000) to access the Code Server

Open the link [http://localhost:8080/swagger-ui/oapip/](http://localhost:8080/swagger-ui/oapip/) to access the Zoo Project swagger

## Follow the tutorial

This tutorial is designed for developers, scientists, and Earth observation enthusiasts who want to get acquainted with the ZOO-Project OGC API Processes implementation to deploy and run Application Packages as web services

* Documentation available at: [https://eoap.github.io/ogc-api-processes-with-zoo/](https://eoap.github.io/ogc-api-processes-with-zoo/)
* Repository available at: [https://github.com/eoap/ogc-api-processes-with-zoo/](https://github.com/eoap/ogc-api-processes-with-zoo/)
