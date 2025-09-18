# Environment Preparation

Before installing JumpServer, ensure you meet the following requirements.

## Hardware and Network Requirements
| Component      | IP Address       | Notes                    |
|----------------|------------------|--------------------------|
| JumpServer     | 192.168.214.138  | Core + Koko + Luna       |
| Web Server     | 192.168.214.140  | Web Service              |
| Windows Server | 192.168.214.141  | Windows test machine     |

## Software Requirements
- **OS:** Ubuntu 20.04
- **Python:** >= 3.8
- **Docker & Docker Compose**
- **RAM:** Minimum 4GB

## Install Docker (Ubuntu)
```bash
sudo apt update
sudo apt install docker.io docker-compose -y

