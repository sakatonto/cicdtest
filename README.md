# Multipass K3s Cluster Provisioning with GitHub Actions

[![Workflow Status](https://img.shields.io/github/actions/workflow/status/<your-org>/<your-repo>/cluster-provision.yml?branch=main)](https://github.com/<your-org>/<your-repo>/actions)
[![Last Commit](https://img.shields.io/github/last-commit/<your-org>/<your-repo>)](https://github.com/<your-org>/<your-repo>/commits/main)

This repository provides an **Ansible playbook** and **GitHub Actions workflow** to automatically provision a **lightweight K3s Kubernetes cluster** using **Multipass VMs**. The workflow supports **dynamic scaling** of worker nodes.

---

## Features

- Provision **one master node** and a configurable number of **worker nodes**.
- Install **K3s** on master and worker nodes automatically.
- Retrieve the **Kubeconfig** for local usage.
- Fully **automated via GitHub Actions**, using a **self-hosted runner**.
- Supports **dynamic scaling** of worker nodes with workflow input.

---

## Prerequisites

- macOS machine with **Multipass** installed.
- **Ansible** installed.
- **GitHub CLI (`gh`)** for manual workflow triggers.
- **Self-hosted runner** registered on your Mac (if using GitHub Actions).

---

## Usage

### 1. Pull the repository

Clone the repository locally (optional for triggering workflow, required for local testing):

```bash
git clone https://github.com/<your-org>/<your-repo>.git
cd <your-repo>
