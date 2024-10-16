[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/goofy-chart)](https://artifacthub.io/packages/search?repo=goofy-chart)

# Niv-DevOps Helm Charts

Welcome to the My Helm Charts repository! This repository contains Helm charts for deploying applications on Kubernetes.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)

## Introduction

This repository provides a collection of Helm charts that can be used to deploy various applications on Kubernetes. Each chart includes templates for Kubernetes resources, along with configuration options for customization.

## Installation

To use these charts, you need to add the repository to your Helm client:

```bash
helm repo add my-repo https://<your-username>.github.io/my-helm-charts/
helm repo update
```

## Usage

After adding the repository, you can install a chart using the following command:

```bash
helm install <release-name> my-repo/<chart-name>
```

Replace `<release-name>` with your desired release name and `<chart-name>` with the name of the chart you want to install.

### Example

```bash
helm install my-app my-repo/my-custom-chart
```

## Configuration

Each chart has its own configurable values. You can customize your installation by providing a `values.yaml` file:

```yaml
# values.yaml
replicaCount: 1
image:
  repository: my-custom-image
  tag: latest
service:
  type: ClusterIP
  port: 80
```

You can apply your custom values during installation:

```bash
helm install my-app my-repo/my-custom-chart -f values.yaml
```
