# Linkerd Demo on Minikube

This README will walk you through installing and using [Linkerd](https://linkerd.io/) on a local Kubernetes cluster provisioned with [Minikube](https://minikube.sigs.k8s.io/docs/). By the end of this demo, you’ll have:

- A running **Minikube** cluster
- The **Linkerd** control plane installed and running
- The **Linkerd CLI** for command-line interactions
- **Linkerd Viz** (on-cluster metrics stack)
- Optionally, **Buoyant Cloud** (a hosted metric stack and monitoring service)
- The **emojivoto** demo application instrumented with the Linkerd sidecar proxies

---

## Prerequisites

- A Linux machine (or a compatible environment) with:
  - [cURL](https://curl.se/)
  - [Docker](https://docs.docker.com/get-docker/) installed and running
  - [kubectl](https://kubernetes.io/docs/tasks/tools/) installed
  - [Minikube](https://minikube.sigs.k8s.io/docs/start/) installed

---

## 1. Install the Linkerd CLI

The Linkerd CLI allows you to interact with Linkerd services on your cluster.

```bash
curl -sL run.linkerd.io/install | sh

---

 1.1 Add the Linkerd CLI to your PATH

```bash
export PATH=$PATH:/home/<system-username>/linkerd2/bin
```bash


## 2. Start the minikube cluster

```bash
minikube start --cpus 4 --memory 4096

