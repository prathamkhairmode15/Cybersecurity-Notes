
## 1. Broken Access Control

### What is Broken Access Control?

**Broken Access Control** occurs when an application fails to properly restrict what authenticated or unauthenticated users are allowed to do.

In simple words:
> Users can access data or perform actions **they are not supposed to**.

According to :contentReference[oaicite:0]{index=0}, access control vulnerabilities allow attackers to bypass authorization checks.

---

### Why It Happens

- Missing access checks on server-side
- Relying only on frontend restrictions
- Insecure Direct Object References (IDOR)
- Incorrect role-based access control (RBAC)
- Hardcoded admin paths
- Misconfigured APIs

---

### Example

- A normal user changes the URL from: /user/profile/admin/dashboard
- The server does not verify the role.
- The user gains admin access.

---

### Impact

- Unauthorized data access
- Account takeover
- Privilege escalation
- Data modification or deletion
- Compliance violations

---

### How to Prevent

- Enforce access control on the **server-side**
- Use role-based or attribute-based access control
- Deny access by default
- Validate ownership of objects
- Log and monitor access control failures

---
