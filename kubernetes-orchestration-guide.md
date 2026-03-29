# Kubernetes Container Orchestration Guide

## Table of Contents
1. [Introduction](#introduction)
2. [Pods](#pods)
3. [Deployments](#deployments)
4. [Services](#services)
5. [RBAC](#rbac)
6. [Troubleshooting](#troubleshooting)
7. [Interview Questions](#interview-questions)

## Introduction
Kubernetes is an open-source container orchestration system for automating computer application deployment, scaling, and management.

## Pods
### What are Pods?
- The smallest deployable units in Kubernetes.
- A pod can host one or more containers.

### Pod Lifecycle
- Pending
- Running
- Succeeded
- Failed
- Unknown

### Managing Pods
- Creating Pods using YAML/JSON files.
- View and manage Pods using `kubectl` commands.

## Deployments
### What are Deployments?
- Provides declarative updates to Pods and ReplicaSets.

### Key Features
- Rollback features to revert to previous deployments.

### Creating Deployments
- Defining desired state in a Deployment YAML file.

## Services
### What are Services?
- A way to expose Pods to network traffic.

### Service Types
- ClusterIP, NodePort, LoadBalancer, ExternalName.

### Managing Services
- Creating Services using Service YAML files.

## RBAC (Role-Based Access Control)
### What is RBAC?
- A method to regulate access to computer or network resources.

### Components
- Roles, RoleBindings, ClusterRoles, ClusterRoleBindings.

### Implementing RBAC
- Defining roles and bindings in YAML files.

## Troubleshooting
### Common Issues
- Troubleshooting failed Pods.
- Checking logs with `kubectl logs`.

### Useful Commands
- `kubectl describe pod <pod-name>`
- `kubectl get events`

## Interview Questions
1. What is the difference between a Pod and a Container?
2. Explain the Kubernetes architecture.
3. How does service discovery work in Kubernetes?
4. What are the benefits of using Deployments in Kubernetes?
5. How do you scale a deployment in Kubernetes?

## Conclusion
This guide provides a comprehensive overview of Kubernetes container orchestration, aimed at helping beginners and practitioners understand the essential concepts and practices.