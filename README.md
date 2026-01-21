# Enterprise Network Engineering Lab 🏗️

## 1. The Mission
I am building a scalable, enterprise-grade lab environment to simulate complex network topologies and test advanced cybersecurity concepts.

## 2. The Infrastructure
To overcome the resource limitations of a standard laptop, I deployed a Type 1 Hypervisor solution.
* **Server:** Proxmox VE (Bare Metal)
* **Specs:** 20GB RAM / 4 vCPUs allocated via KSM.

![Proxmox Dashboard](Screenshots/proxmox.png)
*Figure 1: The Proxmox Server dashboard showing 20GB RAM allocation.*

## 3. The Struggle (Troubleshooting)
The build faced a critical client-server API mismatch (v2.2 vs v3.0). The server refused the connection due to Python build isolation errors.

![Error Log](Screenshots/version conflict.jpg)
*Figure 2: The critical version mismatch error that halted deployment.*

**The Fix:**
I manually downgraded the server environment via CLI and patched the `pip` dependencies to bypass the build isolation.

## 4. The Result
The environment is now fully operational with MikroTik CHR and Cisco images running on the remote engine.

![Success](Screenshots/live-connectivity.png)
*Figure 3: Operational status with live connectivity.*
