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

## Run the _OGC API Processes with ZOO Project_ module on minikube with:

```
cd ogc-api-processes-with-zoo
skaffold dev
```

Wait for the deployment to stablize (1-2 minutes) and the open your browser on the link printed, usually http://127.0.0.1:8000.

## Follow the tutorial

This tutorial is designed for developers, scientists, and Earth observation enthusiasts who want to get acquainted with the ZOO-Project OGC API Processes implementation to deploy and run Application Packages as web services

* Documentation available at: [https://eoap.github.io/ogc-api-processes-with-zoo/](https://eoap.github.io/ogc-api-processes-with-zoo/)
* Repository available at: [https://github.com/eoap/ogc-api-processes-with-zoo/](https://github.com/eoap/ogc-api-processes-with-zoo/)
