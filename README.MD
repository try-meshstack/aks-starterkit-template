# 🚀 Your Application with AKS Deployment

[![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=flat&logo=docker&logoColor=white)](https://www.docker.com/)  
[![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=flat&logo=kubernetes&logoColor=white)](https://kubernetes.io/)

> Containerized Node.js & Angular application with automated deployments to Azure Kubernetes Service (AKS) using GitHub Actions.

## 📋 Overview

This repository provides a foundation for deploying full-stack containerized applications to Azure Kubernetes Service (AKS). It includes:

- **🔄 CI/CD with GitHub Actions**
- **🐳 Two separate Dockerfiles**: one for a Node.js backend, and one for an Angular frontend
- **☁️ Azure Kubernetes Service** for scalable orchestration
- **📁 Kubernetes manifests** organized under `/k8s/`

## 🎯 Key Features

- ✅ **Full-stack containerization**: Node.js backend and Angular frontend, each in its own container
- ✅ **Automatic Git-based deployments**: every commit triggers a full deployment pipeline
- ✅ **Secure image storage** in Azure Container Registry
- ✅ **Configurable Kubernetes resources** managed in versioned manifests under `/k8s/`
- ✅ **Multi-environment support** through branch-based workflows

## 🚀 Getting Started

You can start customizing the application right away. Any changes pushed to the repository will trigger an automated CI/CD pipeline that builds and deploys the updated application to AKS.

Typical changes might include:

- Updating the frontend (Angular app)
- Modifying backend APIs (Node.js)
- Adjusting resource definitions under `/k8s/`
- Tweaking workflow behavior in `.github/workflows/`

No manual deployments required — everything runs automatically through GitHub Actions.

## 🔄 How It Works

The CI/CD pipeline handles everything:

1. **Code Push**: You push changes to the repository
2. **Build**: Separate Docker images are built for the Node.js and Angular apps
3. **Registry**: Images are pushed to Azure Container Registry
4. **Deploy**: Kubernetes manifests from `/k8s/` are applied to AKS

You’ll find your Kubernetes configuration in the `/k8s/` directory, which allows full control over deployments, services, ingress, and other resources.

## 📊 Monitoring Deployments

### GitHub Actions

Track deployment progress in the [Actions tab](../../actions):

- ✅ Green = successful build & deploy
- ❌ Red = failed step with logs
- 📝 Logs include image builds, ACR pushes, and AKS deployment status

### Azure

You can monitor running pods, logs, and services directly in the Azure portal or using `kubectl`, if needed. Cluster access is managed securely via GitHub secrets.

## 📚 Resources

- [Azure Kubernetes Service Documentation](https://docs.microsoft.com/en-us/azure/aks/)
- [Docker Best Practices](https://docs.docker.com/develop/dev-best-practices/)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [meshStack Documentation](https://docs.meshcloud.io/)

---

**That's it!** 🎉 Just push your changes and watch them go live automatically.
