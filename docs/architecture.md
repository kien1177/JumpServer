
# Architecture Diagram
This section provides a detailed visual representation of how JumpServer components interact within the system.
![JumpServer Architecture](images/jump-server.png)
# Architecture Overview

JumpServer consists of several core components:

| Component     | Description                                |
|---------------|--------------------------------------------|
| **Core**      | The main management and control center.    |
| **Koko**      | Proxy for handling SSH and RDP traffic.    |
| **Guacamole** | Web gateway for RDP and VNC connections.   |
| **Web**       | User interface for admins and users.       |
| **Luna**      | Session recording and storage.             |

Each component plays a specific role:
- **Core**: Centralized management and control.
- **Koko**: Handles SSH and RDP traffic as a proxy.
- **Guacamole**: Web gateway for RDP and VNC.
- **Web**: Web UI for admins and end-users.
- **Luna**: Session recording and storage.

## Simplified Diagram
Below is the simplified architecture diagram showing component interactions:

![JumpServer Architecture Diagram](images/jumpserver-architecture.png)

> **Note:**  
> - The diagram shows a high-level view and may be simplified.  
> - For production environments, consider redundancy, load balancing, and high availability.

## Key Points
1. **All access traffic** passes through Koko and Guacamole before reaching the target systems.
2. **Core** enforces access policies, manages users, and controls permissions.
3. **Web** provides an interface for managing configurations and viewing session records.
4. **Luna** securely stores all session recordings and audit logs.

---

