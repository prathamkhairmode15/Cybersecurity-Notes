# Network Ports: The Digital Gateways

### 1. What is a Port?
While an **IP Address** identifies a specific device on a network (like a street address), a **Port** identifies a specific service or application running on that device (like an apartment number).

* **Total Range:** 0 to 65,535
* **Structure:** A 16-bit number added to an IP address (e.g., `192.168.1.1:443`).

### 2. Port Categories
| Category | Range | Purpose |
| :--- | :--- | :--- |
| **Well-Known Ports** | 0 - 1,023 | Reserved for standard system services (HTTP, FTP, SSH). |
| **Registered Ports** | 1,024 - 49,151 | Registered by companies for specific apps (e.g., MS SQL, MySQL). |
| **Dynamic/Private** | 49,152 - 65,535 | Temporary ports used by client apps during a session. |

### 3. Common Ports for Security Professionals
Knowing these is essential for traffic analysis and penetration testing:

* **21 (FTP):** File Transfer Protocol. **Insecure** (sends credentials in plain text).
* **22 (SSH):** Secure Shell. The standard for secure remote access.
* **23 (Telnet):** Unencrypted remote access. **Major Security Risk.**
* **53 (DNS):** Domain Name System. Translates hostnames to IP addresses.
* **80 (HTTP) / 443 (HTTPS):** Web traffic. 443 uses TLS/SSL encryption.
* **3389 (RDP):** Remote Desktop Protocol. Frequently targeted by ransomware.

---

## Security Tip: Port Scanning
Tools like **Nmap** are used to scan a target IP to see which ports are "Open," "Closed," or "Filtered" (behind a firewall).
