# Insecure Design

## What is Insecure Design?

**Insecure Design** refers to weaknesses that arise from **poor or missing security design decisions**, not from coding mistakes or misconfigurations.

In simple words:
> The application is insecure **by design**, even if the code is written correctly.

According to :contentReference[oaicite:0]{index=0}, Insecure Design focuses on **architectural and logical flaws** that cannot be fixed by patching or configuration alone.

---

## Why Insecure Design Is Different from Other OWASP Issues

This is important:

- ❌ Not a coding bug  
- ❌ Not a misconfiguration  
- ❌ Not an outdated library  

✔ A **design-level failure**

If security is not considered during **planning and architecture**, no amount of secure coding later can fully fix it.

---

## Why Insecure Design Happens

- Security not considered during requirement phase
- No threat modeling
- Business logic trusted blindly
- Developers focus only on functionality
- No abuse-case analysis
- Assumption that “users will behave correctly”

> Insecure design usually starts **before a single line of code is written**.

---

## Common Examples of Insecure Design

### 1. Missing Rate Limiting (Design Flaw)

- Login system allows unlimited attempts
- OTP verification has no attempt limit

Even with strong passwords, attackers can:
- Brute-force
- Credential-stuff

This is **not a bug**, it’s a design failure.

---

### 2. Business Logic Flaws

Example:
Result:
- User gets money refunded instead of paying

The system works exactly as coded — but logic is insecure.

---

### 3. Trusting Client-Side Controls

- Price calculated on frontend
- Role checks done only in UI

Attacker modifies request → system accepts it.

---

### 4. No Abuse Case Consideration

System designed only for:
- Normal users
- Normal behavior

No thought given to:
- Malicious users
- Automated attacks
- Edge cases

---

## Real-World Example Scenario

### Scenario

An online exam platform:
- Allows unlimited quiz attempts
- No time restriction
- No monitoring

### Attack

1. Attacker scripts automated attempts
2. Tries all possible answers
3. Eventually gets full marks

### Result

- Exam integrity broken
- System technically “worked”
- Design completely failed

No firewall or patch can fix this — only **redesign**.

---

## Impact of Insecure Design

| Area | Impact |
|----|------|
| Business Logic | Exploited workflows |
| Security | System-level bypass |
| Data | Unauthorized actions |
| Trust | Platform abuse |
| Fix Cost | Very high (requires redesign) |

Insecure design issues are **expensive to fix later**.

---

## How to Prevent Insecure Design

### 1. Threat Modeling (Very Important)

- Identify attacker goals
- Identify abuse cases
- Ask: *“How can this be misused?”*

---

### 2. Secure Design Principles

- Least privilege
- Defense in depth
- Zero trust
- Fail securely

---

### 3. Use Security Requirements

- Define security requirements early
- Treat them like functional requirements

---

### 4. Validate Business Logic on Server

- Never trust client input
- Validate workflows, not just data

---

### 5. Design for Abuse, Not Just Use

- Rate limiting
- Fraud detection
- Monitoring abnormal behavior

---

## Detection and Testing

Insecure design is detected through:
- Architecture reviews
- Threat modeling sessions
- Business logic testing
- Manual penetration testing

Automated scanners **cannot reliably detect** insecure design.

---

## Final Takeaway

Insecure Design is dangerous because:
- It exists before coding
- It cannot be patched easily
- It enables multiple attack types

> **If security is not designed in, it cannot be added later.**

This vulnerability teaches the most important lesson in cybersecurity:
**Security starts at design, not at deployment.**

---

*OWASP Top 10 is now complete.*
