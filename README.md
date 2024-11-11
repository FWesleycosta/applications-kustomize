# application-kustomize

[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)]()
[![GitHub license](https://img.shields.io/github/license/FWesleyCosta/bash-scripts.svg)](https://github.com/FWesleyCosta/bash-scripts/blob/main/LICENSE)
[![Kustomize](https://img.shields.io/badge/Kustomize-3.8.8-blue)](https://kustomize.io/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-1.22.2-blue)](https://kubernetes.io/)

## This repository is dedicated to storing a example of Kustomize to deploy a simple application in Kubernetes.

## Table of Contents
- [Table of Contents](#table-of-contents)
    - [1. Introduction](#1-introduction)
    - [2. Usage](#2-usage)
    - [3. License](#3-license)
    - [4. Documentation](#4-documentation)

## 1. Introduction

<p>Kustomize is a tool that allows you to customize Kubernetes resources using a simple and declarative configuration format. 
With Kustomize, you can define a set of base resources and then apply overlays to customize those resources for different environments or use cases. 
This makes it easy to manage complex Kubernetes configurations and keep them in sync across different environments.</p>


## 2. Usage

<p>This repository contains a structure of directories and files that can be used as an example to deploy a simple application in Kubernetes using Kustomize.
The structure is as follows:</p>

```bash
application-golang
├── kustomize
│   ├── base
│   │   ├── deployment.yaml
│   │   ├── configmap.yaml
│   │   ├── secret.yaml
│   │   ├── role.yaml
│   │   ├── rolebinding.yaml
│   │   ├── service-account.yaml
│   │   ├── kustomization.yaml      
│   │   ├── service.yaml            
│   ├── overlays                    
│   │   ├── dev                     
│   │   │   ├── kustomization.yaml  
│   │   │   ├── patches             
│   │   │   │   ├── deployment.yaml 
│   │   ├── prod                    
│   │   │   ├── kustomization.yaml  
│   │   │   ├── patches             
│   │   │   │   ├── deployment.yaml
│   │   ├── staging
│   │       ├── kustomization.yaml
│   │       ├── patches
│   │           ├── deployment.yaml  
├── LICENSE
└── README.md
```

<p>As you can see, the structure is divided into two main directories: base and overlays. The base directory contains the base resources for the application, and the overlays directory contains the different overlays for different environments (dev, prod, and staging).</p>

<p>The base directory contains the following files:</p>

- deployment.yaml: Contains the deployment configuration for the application.
- configmap.yaml: Contains the configmap configuration for the application.
- secret.yaml: Contains the secret configuration for the application.
- role.yaml: Contains the role configuration for the application.
- rolebinding.yaml: Contains the rolebinding configuration for the application.
- service-account.yaml: Contains the service account configuration for the application.
- kustomization.yaml: Contains the kustomization configuration for the base resources.
- service.yaml: Contains the service configuration for the application.

<p>The overlays directory contains the following directories:</p>

- dev: Contains the dev overlay for the application.
- prod: Contains the prod overlay for the application.
- staging: Contains the staging overlay for the application.

<p>Each overlay directory contains the following files:</p>

- kustomization.yaml: Contains the kustomization configuration for the overlay.
- patches: Contains the patches for the overlay.
- deployment.yaml: Contains the deployment patch for the overlay.


## 3. License

This project is licensed under the MIT License - see the [LICENSE](https://mit-license.org/) page for details.

## 4. Documentation

### Kustomize

- **[Kustomize Official Documentation](https://kustomize.io/)**: The official documentation for Kustomize, including installation instructions, usage examples, and advanced features.
- **[Kustomize GitHub Repository](https://github.com/kubernetes-sigs/kustomize)**: The GitHub repository for Kustomize, where you can find the latest releases, open issues, and contribute to the project.
- **[Kustomize Guide on Kubernetes.io](https://kubernetes.io/docs/tasks/manage-kubernetes-objects/kustomization/)**: A guide to using Kustomize on the Kubernetes website, with examples and best practices for managing Kubernetes resources with Kustomize.

### Kubernetes

- **[Kubernetes Documentation](https://kubernetes.io/docs/)**: The official documentation for Kubernetes, including installation instructions, concepts, and best practices for managing Kubernetes clusters.
- **[Kubernetes API Reference](https://kubernetes.io/docs/reference/kubernetes-api/)**: The API reference for Kubernetes, including detailed information about the Kubernetes API objects and resources.
- **[Kubernetes Concepts](https://kubernetes.io/docs/concepts/)**: An overview of the core concepts of Kubernetes, including Pods, Deployments, Services, and other key components of the Kubernetes architecture.

