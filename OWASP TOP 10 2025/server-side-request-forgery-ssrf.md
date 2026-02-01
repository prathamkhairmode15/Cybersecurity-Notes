# Server-Side Request Forgery (SSRF)

## What is Server-Side Request Forgery (SSRF)?

**Server-Side Request Forgery (SSRF)** occurs when an attacker forces a server-side application to make **unauthorized requests** to internal or external resources.

In simple words:
> The attacker tricks the server into sending requests **on their behalf**.

According to :contentReference[oaicite:0]{index=0}, SSRF is dangerous because the request originates from a **trusted server**, not the attacker.

---

## Why SSRF Is Dangerous

Servers often have:
- Access to internal networks
- Access to cloud metadata services
- Higher trust levels
- Fewer network restrictions

If an attacker controls server requests, they can:
- Access internal services
- Bypass firewalls
- Steal cloud credentials
- Scan internal infrastructure

---

## Why SSRF Happens

- User-controlled URLs are not validated
- Applications fetch remote resources blindly
- No allowlist of permitted destinations
- Weak network segmentation
- Overly permissive outbound network rules

> SSRF is a **design flaw**, not just a coding mistake.

---

## Common SSRF Scenarios

### 1. Fetching External URLs

Application feature:
Attacker input:

The server accesses internal admin services.

---

### 2. Cloud Metadata Access

In cloud environments, metadata services exist at:
If accessed via SSRF, attackers can steal:
- Cloud credentials
- Access tokens
- Instance metadata

---

### 3. Internal Port Scanning

Attackers can probe:
to detect internal databases and services.

---

## Real-World Example Scenario

### Scenario

- Application allows users to submit URLs
- Server fetches the URL content
- No validation on destination address

### Attack

1. Attacker submits internal IP address
2. Server makes request internally
3. Sensitive internal service responds
4. Attacker receives internal data

### Result

- Internal network exposure
- Credential theft
- Full infrastructure compromise

---

## Impact of SSRF

| Area | Impact |
|----|------|
| Network | Internal network exposure |
| Cloud | Credential theft |
| Security | Firewall bypass |
| Data | Sensitive service access |
| Business | Infrastructure compromise |

SSRF often acts as a **gateway vulnerability** to deeper attacks.

---

## How to Prevent SSRF

### 1. Input Validation and Allowlisting

- Allow only trusted domains
- Reject IP addresses and localhost
- Validate URL schemes

---

### 2. Block Internal Network Access

- Prevent access to:
  - `localhost`
  - `127.0.0.1`
  - `169.254.169.254`
  - Private IP ranges

---

### 3. Network Segmentation

- Restrict outbound traffic
- Isolate internal services
- Apply firewall egress rules

---

### 4. Disable Unused URL Fetching Features

- Remove unnecessary URL-based functionality
- Reduce attack surface

---

### 5. Use Timeouts and Request Limits

- Prevent long-running requests
- Limit response size

---

## Detection and Testing

SSRF vulnerabilities are identified using:
- Manual testing with internal IP payloads
- Cloud metadata access testing
- Penetration testing
- Security code reviews

Common test payload:

---

## Final Takeaway

SSRF is dangerous because:
- The server becomes the attacker
- Internal systems are exposed
- Cloud environments are heavily impacted

> **Never trust user-supplied URLs — validate, restrict, and monitor them.**

SSRF may look simple, but its impact can be **catastrophic**.

---




