# Environment Preparation

This page helps you prepare the infrastructure and software required **before** installing JumpServer.

> **Goal:** Have a clean OS, a clear network plan (IPs, ports), Docker/Compose installed, and working SSH/RDP access to your target assets.

---

# Environment Preparation

## 1) Topology & IP Plan

| Component       | IP Address      | Notes                            |
|----------------|----------------|----------------------------------|
| JumpServer Host | 192.168.214.138 | Runs Core/Koko/Luna (via Docker) |
| Linux WebService| 192.168.214.140 | Runs Web Service                  |
| Windows Asset  | 192.168.214.141 | Test server (RDP)                  |

> **Note:**  
> - Adjust the IPs to match your network environment.  
> - Ensure each component is accessible over the network via SSH, RDP, or web protocols as required.


## 2) Hardware & OS Requirements

- **OS**: Ubuntu 20.04+ (JumpServer Host recommended)
- **CPU**: 2 vCPUs (minimum), 4+ vCPUs recommended
- **RAM**: 4 GB minimum, 8 GB recommended for production
- **Disk**: 30 GB free (logs & session recordings may require additional space)
- **Network**: Stable LAN access to all assets (SSH/RDP/DB connections)
- **Tools**:
  - SSH client (e.g., PuTTY)
  - RDP client (e.g., Microsoft Remote Desktop, Remmina)
  - Database client (pgAdmin, HeidiSQL)
  - Modern web browser (Chrome or Firefox)

### Time Synchronization (Strongly Recommended)
Ensure the system clock is synchronized for accurate logging and auditing.

#### For Ubuntu:
```bash
sudo apt-get update
sudo apt-get install -y chrony
sudo systemctl enable --now chrony
```

### For CentOS/RHEL:
```bash
sudo yum install -y chrony
sudo systemctl enable --now chronyd
```
### Verify time sync:
```bash
chronyc tracking
```

---

## 3. **Network Preparation**

Proper network configuration is essential for JumpServer to function correctly.

- Ensure the following ports are **open and accessible**:

| Service                | Port  | Protocol |
|-----------------------|-------|----------|
| SSH Access            | 22    | TCP      |
| HTTP (Web UI)         | 80    | TCP      |
| HTTPS (Secure Web UI) | 443   | TCP      |
| RDP                   | 3389  | TCP      |
| SMB/File Sharing      | 445   | TCP      |
| Database (PostgreSQL) | 5432  | TCP      |

- Configure firewall rules to **allow JumpServer Host** to access:
  - All target Linux servers via **SSH (22)**
  - All target Windows servers via **RDP (3389)** and **SMB (445)**
  - Database services such as **PostgreSQL (5432)**

> **Best Practice:**
> - Restrict access to JumpServer only by whitelisting its IP address.
> - Block unnecessary external access to internal resources.

Example `ufw` firewall configuration on Ubuntu:
```bash
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw allow 3389/tcp
sudo ufw allow 445/tcp
sudo ufw allow 5432/tcp
sudo ufw enable











