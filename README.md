# Azure Cloud Platform

A hands-on cloud engineering project focused on building and running a web application on Microsoft Azure.

The goal of this project is to understand how a real application moves from development to a cloud environment — from writing the application and building Docker images to provisioning Azure infrastructure, deploying workloads on Kubernetes, setting up CI/CD, and monitoring the environment.

## Architecture

```text
                    ┌──────────────────┐
                    │      GitHub      │
                    │   Source Code    │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │  GitHub Actions  │
                    │      CI/CD       │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │ Azure Container  │
                    │    Registry      │
                    └────────┬─────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │       AKS        │
                    │    Kubernetes    │
                    └────────┬─────────┘
                             │
                   ┌─────────┴─────────┐
                   ▼                   ▼
            ┌─────────────┐      ┌─────────────┐
            │  Frontend   │      │   Backend   │
            │    React    │ ───▶ │ Spring Boot │
            └─────────────┘      └──────┬──────┘
                                        │
                                        ▼
                                 ┌─────────────┐
                                 │ Azure DB    │
                                 └─────────────┘

        Monitoring → Azure Monitor / Log Analytics
        Secrets    → Azure Key Vault
        IaC        → Terraform
```

## Tech Stack

| Area               | Technology                   |
| ------------------ | ---------------------------- |
| Cloud              | Microsoft Azure              |
| Infrastructure     | Terraform                    |
| Containers         | Docker                       |
| Orchestration      | Kubernetes / AKS             |
| CI/CD              | GitHub Actions               |
| Container Registry | Azure Container Registry     |
| Backend            | Java, Spring Boot            |
| Frontend           | React                        |
| Database           | Azure Database               |
| Secrets            | Azure Key Vault              |
| Monitoring         | Azure Monitor, Log Analytics |
| Version Control    | Git, GitHub                  |

## What I'm Building

The project is being built step by step to cover the main areas involved in cloud and platform engineering.

* Build a backend REST API using Spring Boot
* Build a frontend application using React
* Containerize the application using Docker
* Provision Azure resources using Terraform
* Store Docker images in Azure Container Registry
* Deploy the application to Azure Kubernetes Service (AKS)
* Configure Kubernetes deployments, services, and ingress
* Set up CI/CD pipelines using GitHub Actions
* Manage application secrets securely with Azure Key Vault
* Set up logging and monitoring using Azure Monitor and Log Analytics
* Add health checks and basic application observability
* Document the architecture, deployment process, and troubleshooting steps

## Repository Structure

```text
azure-cloud-platform/
│
├── application/
│   ├── backend/          # Spring Boot REST API
│   └── frontend/         # React application
│
├── infrastructure/
│   └── terraform/        # Azure infrastructure as code
│
├── kubernetes/           # Kubernetes deployment configuration
├── scripts/              # Setup and deployment scripts
├── monitoring/           # Monitoring and alert configuration
├── docs/                 # Architecture and project documentation
│
├── .github/
│   └── workflows/        # GitHub Actions workflows
│
└── README.md
```

## Engineering Practices

Throughout the project, I'm focusing on practices that are commonly used in cloud and platform engineering:

* Infrastructure as Code with Terraform
* Automated build and deployment pipelines
* Containerized applications
* Kubernetes-based deployments
* Secure handling of application secrets
* Centralized logging and monitoring
* Application health checks
* Least-privilege access
* Environment-specific configuration
* Clear documentation and troubleshooting guides


## Why This Project?

This project is being built as a practical way to learn and demonstrate how different cloud technologies work together in a real deployment workflow.

Rather than looking at Azure, Docker, Kubernetes, Terraform, and CI/CD as separate tools, the focus is on understanding how they fit together to deploy, operate, monitor, and maintain an application in the cloud.
