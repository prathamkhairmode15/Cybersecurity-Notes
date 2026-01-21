## 2. Cryptographic Failures

### What are Cryptographic Failures?

**Cryptographic Failures** occur when sensitive data is not properly protected due to weak, missing, or incorrect cryptography.

Earlier known as **Sensitive Data Exposure**.

> Data is exposed not because encryption is broken, but because it is **used incorrectly or not used at all**.

---

### Why It Happens

- Storing passwords in plaintext
- Using outdated algorithms (MD5, SHA-1)
- Weak encryption keys
- Improper key management
- No encryption for data in transit (HTTP instead of HTTPS)
- Hardcoded secrets in source code

---

### Example

- Login passwords stored directly in a database without hashing.
- Website uses HTTP instead of HTTPS, exposing credentials over the network.

---

### Impact

- Leakage of personal data
- Financial fraud
- Identity theft
- Loss of trust
- Legal and compliance issues

---

### How to Prevent

- Use strong encryption algorithms (AES, RSA, SHA-256)
- Hash passwords using bcrypt, scrypt, or Argon2
- Enforce HTTPS with TLS
- Protect encryption keys securely
- Avoid storing sensitive data unless necessary

---
