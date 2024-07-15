# k8s-hpa-metrics-server 

## Overview

This project demonstrates how to scale Kubernetes applications using Horizontal Pod Autoscaler (HPA) with Helm for installation and Argo CD for continuous deployment. It provides a streamlined approach to automating application scaling based on CPU and memory metrics in Kubernetes environments.

## Key Features

- **Horizontal Pod Autoscaler (HPA)**: Automatically adjusts pod replicas based on CPU and memory utilization metrics.
- **Metrics Server**: Installs and configures Metrics Server with Helm, providing essential metrics required for HPA.
- **Argo CD Integration**: Uses Argo CD for automated deployment and management of HPA configurations.
- **Example Configuration**: Includes an example `hpa.yaml` configuration file to illustrate setting up HPA for a Node.js application.

## Getting Started

To get started with deploying and scaling applications using this project:

1. **Install Metrics Server**: 

   `helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/`

   `helm repo update`

   `helm install metrics-server metrics-server/metrics-server`

   
2. **Configure Horizontal Pod Autoscaler (HPA)**: Use the example `hpa.yaml` in this repository (`helm-chart/templates/hpa.yaml`) as a template to configure HPA for your applications.

3. **Deploy with Argo CD**: Set up Argo CD to manage the deployment of HPA configurations and ensure automated scaling based on real-time metrics.

## Usage

Detailed usage instructions and configurations are provided in each respective directory (`helm-chart/` and `argocd/`), as well as in my blog post about Argo CD: [Demystifying Argo CD: A Guide to Declarative Setup](https://medium.com/@ugurozkandev/demystifying-argocd-a-guide-to-declarative-setup-a43b609265db).