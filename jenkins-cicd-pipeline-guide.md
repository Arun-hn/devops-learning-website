# Jenkins CI/CD Pipeline Guide

## Pipeline Types
- **Declarative Pipeline**: A more structured form of pipeline that uses a predefined syntax.
- **Scripted Pipeline**: A more flexible and powerful way of defining pipelines using Groovy scripting.

## Architecture
- Jenkins uses a **master-slave architecture** where the master node controls the build process and slaves/agents execute jobs.
- The architecture also includes components like plugins, which extend Jenkins' functionalities.

## Docker/Kubernetes Integration
- **Docker**: Jenkins can build and run Docker images, allowing for standardized environments across development and production.
- **Kubernetes**: Jenkins can dynamically spin up containers in a Kubernetes cluster to run build jobs, providing scalability and efficient resource management.

## Scenario-Based Interview Questions
1. **What is a Jenkins pipeline and how does it differ from a Jenkins job?**
2. **How can you handle secrets in Jenkins pipelines?**
3. **Explain the differences between declarative and scripted pipelines.**

## Best Practices
- Keep pipeline definitions version controlled.
- Use parameters in your pipelines for dynamic behavior.
- Modularize your pipeline with shared libraries for reusability.
- Implement thorough logging and error handling for easier debugging.