# Identification and Authentication Failures

## What are Identification and Authentication Failures?

**Identification and Authentication Failures** occur when applications incorrectly implement login, identity verification, or session management.

In simple words:
> The application fails to properly confirm **who the user is** or **maintain their identity securely**.

According to :contentReference[oaicite:0]{index=0}, these failures allow attackers to:
- Take over user accounts
- Impersonate legitimate users
- Bypass authentication mechanisms

This category was earlier known as **Broken Authentication**.

---

## Identification vs Authentication (Important Difference)

- **Identification** → Who are you? (username, email, user ID)
- **Authentication** → Prove it (password, OTP, biometrics)

Failure in either leads to serious security issues.

---

## Why These Failures Happen

- Weak or predictable passwords
- No multi-factor authentication (MFA)
- Poor session management
- Credentials sent over HTTP
- Hardcoded credentials
- Improper logout handling
- Unlimited login attempts
- Reusable or exposed session IDs

> Most authentication failures are caused by **poor implementation**, not complex attacks.

---

## Common Examples

### 1. Weak Password Policies

- Short passwords
- Common passwords (`password123`)
- No complexity rules

Attackers easily perform **brute-force** or **credential stuffing** attacks.

---

### 2. No Multi-Factor Authentication (MFA)

If only passwords are used:
- Stolen credentials = full account access

---

### 3. Session Fixation

- Session ID does not change after login
- Attacker reuses a known session ID

---

### 4. Improper Logout

- Session remains valid after logout
- Back button restores authenticated session

---

### 5. Exposed Credentials

- Passwords stored in plaintext
- Credentials logged in files
- Tokens exposed in URLs

---

## Real-World Example Scenario

### Scenario

A web application:
- Uses only username and password
- Has no login attempt limits
- Uses long-lived session cookies

### Attack

1. Attacker obtains leaked credentials
2. Logs in successfully
3. Session remains valid for days
4. User account is fully compromised

### Result

- Account takeover
- Data theft
- Unauthorized actions

---

## Impact of Authentication Failures

| Area | Impact |
|----|------|
| User Accounts | Account takeover |
| Confidentiality | Personal data leakage |
| Integrity | Unauthorized actions |
| Trust | Loss of user confidence |
| Compliance | Legal and regulatory issues |

These failures often lead directly to **privilege escalation**.

---

## How to Prevent Identification and Authentication Failures

### 1. Enforce Strong Password Policies

- Minimum length
- Complexity rules
- Block common passwords

---

### 2. Implement Multi-Factor Authentication (MFA)

- OTP
- Authenticator apps
- Hardware keys

MFA dramatically reduces account takeover risk.

---

### 3. Secure Session Management

- Rotate session IDs after login
- Use secure, HttpOnly cookies
- Set session expiration times

---

### 4. Protect Credentials

- Hash passwords using bcrypt, Argon2, or scrypt
- Never store plaintext passwords
- Avoid logging sensitive data

---

### 5. Limit Login Attempts

- Account lockout
- CAPTCHA
- Rate limit
