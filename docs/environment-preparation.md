# Environment Preparation

This page helps you prepare the infrastructure and software required **before** installing JumpServer.

> **Goal:** Have a clean OS, a clear network plan (IPs, ports), Docker/Compose installed, and working SSH/RDP access to your target assets.

---

## 1) Topology & IP Plan

| Component       | IP Address       | Notes                                  |
|-----------------|------------------|----------------------------------------|
| JumpServer Host | 192.168.214.138  | Runs Core/Koko/Luna (via Docker)       |
| Linux WebService| 192.168.214.140  | Runs Web Service                       |
| Windows Asset   | 192.168.214.141  | Test server (RDP)                      |

> Adjust the IPs to your environment.

---

## 2) Hardware & OS Requirements

- **OS:** Ubuntu 20.04+
- **CPU:** 2 vCPU (minimum), 4+ recommended
- **RAM:** 4 GB (minimum), 8 GB recommended
- **Disk:** 30 GB free (logs & session recordings may require more)
- **Network:** Stable LAN access to your assets (SSH/RDP/DB)
-**Tool:** PuTTY, Remote Desktop Protocol (RDP), DB Client (pgAdmin, HeidiSQL), web (Chrome/Firefox)

**Time synchronization (strongly recommended):**
```bash
# Ubuntu
sudo apt-get update
sudo apt-get install -y chrony
sudo systemctl enable --now chrony
```

**Install and unzip JumpServer:**
```bash
cd /opt
sudo wget https://github.com/jumpserver/installer/releases/download/v4.10.1/jumpserver-installer-v4.10.1.tar.gz
sudo tar -xzf jumpserver-installer-v4.10.1.tar.gz
cd jumpserver-installer-v4.10.1
```

**Run file jumpserver-installer-v4.10.1**
```
sudo ./jmsctl.sh install 
```














