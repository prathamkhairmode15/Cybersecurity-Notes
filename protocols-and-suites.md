# Network Protocols: The Language of Data

### 1. Introduction
A protocol is a standardized set of rules that defines how data is transmitted and received. Without protocols, devices would have no way of understanding the electrical signals sent between them.

### 2. The Big Two: TCP vs. UDP

#### TCP (Transmission Control Protocol)
* **Connection-Oriented:** Establishes a connection before sending data.
* **Reliability:** Uses acknowledgments; if a packet is lost, it is re-sent.
* **3-Way Handshake:**
    1.  **SYN** (Synchronize)
    2.  **SYN-ACK** (Synchronize-Acknowledge)
    3.  **ACK** (Acknowledge)

#### UDP (User Datagram Protocol)
* **Connectionless:** Sends data without checking if the receiver is ready.
* **Speed:** Much faster than TCP because it has no overhead for error checking.
* **Use Cases:** Streaming, Gaming, VoIP, and DNS.

### 3. Core Network Layer Protocols
* **IP (Internet Protocol):** Responsible for addressing and routing packets.
    * **IPv4:** 32-bit (e.g., `192.168.1.1`).
    * **IPv6:** 128-bit (e.g., `2001:0db8:85a3:0000:0000:8a2e:0370:7334`).
* **ICMP (Internet Control Message Protocol):** Used for error messages and operational information (used by `ping` and `traceroute`).
* **ARP (Address Resolution Protocol):** Maps an IP address to a physical **MAC address**.

---

## Security Tip: Protocol Abuse
Attackers often use **ICMP** for network discovery (ping sweeps) or **ARP** for "Man-in-the-Middle" (ARP Spoofing) attacks.
