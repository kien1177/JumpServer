![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

# 🚀 JumpServer Installation & Configuration Guide

JumpServer is an open-source **Privileged Access Management (PAM)** system that helps manage privileged accounts, record user sessions, and control activities on servers, databases, and network devices.

> **Goals:**  
> - Understand JumpServer architecture.  
> - Install and configure the system end-to-end.  
> - Create assets, accounts, and verify successful connections.

---

## 📚 Table of Contents
1. [Introduction](docs/introduction.md)
2. [Architecture Overview](docs/architecture.md)
3. [Environment Preparation](docs/environment-preparation.md)
4. [Installing JumpServer](docs/installing-jumpserver.md)
5. [Basic Configuration](docs/basic-configuration.md)
6. [Testing the System](docs/testing-system.md)
7. [Troubleshooting](docs/troubleshooting.md)
8. [References](docs/references.md)

---

## 1. Introduction
JumpServer enables you to:
- Centrally manage **access accounts**.
- Record **all user sessions** for auditing.
- Protect systems with a **Zero Trust** access model.
- Support SSH, RDP, and databases (MySQL, MSSQL, PostgreSQL, ...).

**Official website:** [https://jumpserver.org/](https://jumpserver.org/)

---

## 2. Architecture Overview
Key components:
- **Core**: Central management and control component.
- **Koko**: Proxy that handles SSH/RDP connections.
- **Guacamole**: Web gateway for RDP/VNC.
- **Web**: Administration and user interface.
- **Luna**: Session recording and storage.

> **Architecture diagram:**

![JumpServer Architecture](docs/images/jump-server.png)

## Deployment Architecture Diagram
Below is a deployment architecture diagram.

![Deployment Architecture Diagram](docs/images/deployment-architecture-diagram.png)

## Console View
Below is an example of a session running inside JumpServer.

![Console Moving Example](docs/images/moving-console.png)
