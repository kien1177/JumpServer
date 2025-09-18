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
- [1. Introduction](#1-introduction)
- [2. Architecture Overview](#2-architecture-overview)
- [3. Environment Preparation](#3-environment-preparation)
- [4. Installing JumpServer](#4-installing-jumpserver)
- [5. Basic Configuration](#5-basic-configuration)
- [6. Testing the System](#6-testing-the-system)
- [7. Troubleshooting](#7-troubleshooting)
- [8. References](#8-references)

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
