# Ansible Configuration Management Guide

## Introduction
Ansible is a powerful automation tool used for configuration management, application deployment, and task automation. This guide will provide an overview of various aspects of Ansible, including playbooks, roles, idempotency, vault usage, and common interview questions to prepare you for Ansible-related roles.

## 1. Playbooks
Playbooks are the heart of Ansible’s automation. They are written in YAML and describe the desired state of the system you want to manage.
### Structure of Playbooks
A typical playbook consists of: 
- **Hosts**: Defines the target hosts.
- **Tasks**: Defines the actions to be performed.
- **Handlers**: Notifications that trigger when a task changes.
### Example
```yaml
- hosts: webservers
  tasks:
    - name: Install Nginx
      apt:
        name: nginx
        state: present
      notify: Start Nginx

  handlers:
    - name: Start Nginx
      service:
        name: nginx
        state: started
```

## 2. Roles
Roles allow you to organize playbooks into reusable components. A role typically contains tasks, handlers, defaults, variables, files, and templates.
### Directory Structure
```
roles/
  webserver/
    tasks/
      main.yml
    handlers/
      main.yml
    templates/
    files/
    vars/
    defaults/
```
### Using Roles in Playbooks
```yaml
- hosts: all
  roles:
    - webserver
```

## 3. Idempotency
Idempotency means that if you run a playbook multiple times, the result will be the same. Ansible ensures idempotency by checking the current state before making any changes.
### Importance
- Prevents unnecessary changes
- Saves time and resources

## 4. Ansible Vault
Ansible Vault is a feature that allows you to encrypt sensitive data within Ansible projects. This is particularly useful for storing passwords and other confidential information.
### Creating and Using Vaults
- **Create a Vault**: `ansible-vault create secrets.yml`
- **Encrypting Files**: `ansible-vault encrypt file.yml`
- **Decrypting Files**: `ansible-vault decrypt file.yml`
### Using Vault in Playbooks
```yaml
vars_files:
  - secrets.yml
```

## 5. Interview Questions
### Common Questions
1. What is Ansible?
2. Explain the architecture of Ansible.
3. What are playbooks and roles?
4. How does Ansible handle idempotency?
5. What is Ansible Vault and why is it used?
6. How do you create an Ansible inventory?
7. Can you describe the difference between a task and a handler?
8. How do you debug Ansible playbooks?

## Conclusion
This guide provides a basic understanding of Ansible and its core components. Mastery of these concepts will help you build efficient and scalable automation solutions for your infrastructure.