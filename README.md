# Jenkins & Ansible CI/CD Infrastructure Automation

[![GitHub commit](https://img.shields.io/github/last-commit/chittibabu080694/jenkins-ansible-automation)](https://github.com/chittibabu080694/jenkins-ansible-automation)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An automated CI/CD pipeline project that integrates **Jenkins** with **Ansible** to achieve configuration management and software deployment upon code commits to **GitHub**.

---

## 🏗️ Architecture & Workflow

```text
+-------------------+       Webhook Trigger       +--------------------+
|                   | --------------------------> |                    |
|  GitHub Repo      |                             |   Jenkins Server   |
|  (Source Control) | <-------------------------- |  (CI/CD Pipeline)  |
+-------------------+         Checkout Code       +---------+----------+
                                                            |
                                               Executes Playbook via SSH
                                                            v
                                                  +--------------------+
                                                  |   Ansible Target   |
                                                  |   (Nginx Server)   |
                                                  +--------------------+
