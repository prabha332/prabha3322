# 🚀 platformctl — Intelligent DevOps CLI Tool

> A powerful command-line tool for DevOps engineers, SREs, and platform teams to troubleshoot Kubernetes clusters, monitor deployments, and resolve infrastructure issues faster — directly from the terminal.

[![PyPI version](https://img.shields.io/pypi/v/platformctl.svg)](https://pypi.org/project/platformctl/)
[![Python](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Mac%20%7C%20Windows-lightgrey)]()

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Key Features](#-key-features)
- [Supported Environments](#-supported-environments)
- [Installation](#-installation)
- [Basic Commands](#-basic-commands)
- [Example Output](#-example-output)
- [How It Solves Production Problems](#-how-it-solves-production-problems)
- [Architecture](#-architecture)
- [Tech Stack](#-tech-stack)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 🔹 Overview

**platformctl** is an open-source Python CLI tool built to speed up Kubernetes troubleshooting and infrastructure management for DevOps engineers and SREs.

Instead of running multiple `kubectl` commands manually, `platformctl` gives you a single intelligent interface that:
- Scans your cluster health in one command
- Detects real production issues automatically
- Provides AI-powered troubleshooting suggestions
- Tracks deployment history and failures

---

## 💡 Problem Statement

DevOps engineers waste valuable time manually running `kubectl` commands to diagnose issues like:
- CrashLoopBackOff pods
- OOMKilled containers
- Missing liveness/readiness probes
- High CPU/memory usage on nodes
- Deployment failures and rollback tracking

**platformctl solves this** by providing a single intelligent CLI that automates diagnostics, detects issues, and accelerates incident response.

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🏥 Kubernetes Health Checks | Full cluster health scan in one command |
| 📊 Pod, Node & Deployment Monitoring | Real-time status of all workloads |
| 🤖 AI-Powered Troubleshooting | Intelligent suggestions for detected issues |
| 📜 Deployment History Tracking | Track past deployments and failures |
| 🖥️ Dashboard Support | Terminal-based cluster dashboard |
| ☁️ Multi-Cloud Ready | Works with AWS, Azure, GCP |
| 🔌 Works Everywhere | Local, VM, Docker, EKS, AKS, GKE |

---

## ☁️ Supported Environments

### Local & VM
- ✅ Linux (Ubuntu, CentOS, RHEL)
- ✅ macOS
- ✅ Windows
- ✅ Docker containers
- ✅ Virtual Machines

### Cloud Platforms
- ✅ AWS EC2 + Amazon EKS
- ✅ Azure VM + Azure Kubernetes Service (AKS)
- ✅ GCP Compute Engine + Google Kubernetes Engine (GKE)

---

## 📦 Installation

```bash
pip install platformctl
```

### If the command is not found after installation:

```bash
# Add to PATH (Mac/Linux)
export PATH=$PATH:$HOME/.local/bin:/usr/local/bin

# Make it permanent — add to your ~/.bashrc or ~/.zshrc
echo 'export PATH=$PATH:$HOME/.local/bin:/usr/local/bin' >> ~/.bashrc
source ~/.bashrc
```

### Verify installation:

```bash
platformctl --version
```

---

## 🖥️ Basic Commands

```bash
# Show all available commands
platformctl --help

# Run full cluster health diagnostic
platformctl doctor

# Launch terminal dashboard
platformctl dashboard

# Deploy an application
platformctl deploy

# List all pods
platformctl get pods

# List all nodes
platformctl get nodes

# AI-powered debug assistant
platformctl ai-debug
```

---

## 📸 Example Output

```
╔══════════════════════════════════════════════╗
║     PlatformCTL Intelligent Doctor Running   ║
╚══════════════════════════════════════════════╝

🔍 PlatformCTL Cluster Health Scan
─────────────────────────────────────
Total Pods:     12
Healthy Pods:   10  ✅
Warning Pods:    1  ⚠️
Unhealthy Pods:  1  ❌

⚠️  Detected Issues:
  → CrashLoopBackOff pod in production namespace
  → High CPU usage on worker node
  → Missing liveness probe in deployment

💡 AI Suggestions:
  → Check pod logs: kubectl logs <pod-name> -n production
  → Review resource limits in deployment YAML
  → Add liveness probe to prevent silent failures
```

---

## ✅ How It Solves Production Problems

- ✅ Detects unhealthy Kubernetes pods instantly
- ✅ Identifies OOMKilled and CrashLoopBackOff issues
- ✅ Finds missing probes and bad resource limits
- ✅ Helps troubleshoot high CPU / memory usage
- ✅ Tracks deployment history and failures
- ✅ Speeds up incident response in production clusters
- ✅ Reduces manual `kubectl` debugging time by ~50%

---

## 🏗️ Architecture

```
User Terminal
     ⬇
platformctl CLI (Entry Point)
     ⬇
Command Router (Click / Argparse)
     ⬇
┌─────────────────────────────────────┐
│         Core Modules                │
│  ┌──────────┐  ┌─────────────────┐  │
│  │  Doctor  │  │   AI Debug      │  │
│  │  Module  │  │   Engine        │  │
│  └──────────┘  └─────────────────┘  │
│  ┌──────────┐  ┌─────────────────┐  │
│  │Dashboard │  │ Deploy Tracker  │  │
│  │  Module  │  │   Module        │  │
│  └──────────┘  └─────────────────┘  │
└─────────────────────────────────────┘
     ⬇
Kubernetes API / Cloud SDKs
     ⬇
AWS EKS / Azure AKS / GKE / Local K8s
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python 3.8+ | Core language |
| Kubernetes Python Client | Cluster API integration |
| Click / Argparse | CLI framework |
| Docker SDK | Container management |
| Rich / Colorama | Terminal UI & formatting |
| PyYAML | YAML config parsing |
| Boto3 (AWS SDK) | AWS integration |
| Git | Version control |

---

## 📈 Future Improvements

- [ ] Slack & PagerDuty alerting integration
- [ ] Helm chart deployment support
- [ ] Cost optimization recommendations per namespace
- [ ] GitHub Actions integration for CI/CD pipelines
- [ ] Web UI dashboard (React-based)
- [ ] Plugin system for custom modules
- [ ] Auto-remediation for common issues
- [ ] Grafana metrics export

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

```bash
# Fork the repo and clone it
git clone https://github.com/prabha332/platformctl.git
cd platformctl

# Create a new branch
git checkout -b feature/your-feature-name

# Make your changes and push
git push origin feature/your-feature-name

# Open a Pull Request 🎉
```

---

## 👩‍💻 Author

**Prabhavati Agre**
Platform Engineer | AWS | Kubernetes | DevOps Automation

- 🐙 GitHub: [@prabha332](https://github.com/prabha332)
- 💼 LinkedIn: [linkedin.com/in/prabhavati-agre-b29116131](https://linkedin.com/in/prabhavati-agre-b29116131)
- 📧 Email: prabhavatiagre@gmail.com

---

⭐ *If platformctl helped you, please give it a star on GitHub — it means a lot!*

---

## 🔗 Related Projects

- 🚗 [Fuel Route Optimization API](https://github.com/prabha332/fuel-route-optimization-api) — Django REST API for optimized fuel stop planning
