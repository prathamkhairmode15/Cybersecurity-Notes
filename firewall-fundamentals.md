# Firewalls: The First Line of Defense

### 1. What is a Firewall?
A firewall is a security system that monitors and controls incoming and outgoing network traffic based on predetermined security rules. It acts as a barrier between a trusted internal network and untrusted external networks (the Internet).

### 2. Firewall Types & Evolution

| Type | Layer (OSI) | How it Works |
| :--- | :--- | :--- |
| **Packet Filtering** | Layer 3 | Inspects source/destination IP and Port. Very fast but basic. |
| **Stateful Inspection** | Layer 4 | Tracks the "state" of a connection. Knows if an incoming packet is a response to a valid request. |
| **Application / Proxy** | Layer 7 | Inspects the actual data (payload). Can block specific commands in a protocol. |
| **Next-Gen (NGFW)** | Layers 3-7 | Combines firewalls with IDS/IPS, Antivirus, and Deep Packet Inspection (DPI). |

### 3. The "Implicit Deny" Rule
The most critical concept in firewall configuration is **Implicit Deny**. 
* **The Rule:** If a packet does not match any specific "Allow" rule, it is automatically blocked.
* **Why?** It ensures that only specifically authorized traffic can enter the network.

### 4. Firewall Placement
* **Host-based:** Installed on a single computer (e.g., Windows Defender Firewall).
* **Network-based:** A dedicated hardware appliance protecting an entire network.

---

## Security Tip: Egress Filtering
Most people focus on what comes **in** (Ingress), but security pros also monitor what goes **out** (Egress). This helps detect if a compromised internal computer is "calling home" to a hacker's server.
