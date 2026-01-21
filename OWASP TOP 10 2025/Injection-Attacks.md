# Injection Attacks

## What is an Injection Attack?

An **Injection Attack** occurs when an application sends **untrusted user input** to an interpreter (such as a database, OS, or LDAP service) and that input is executed as **part of a command or query**.

In simple terms:
> The application treats **user input as code instead of data**.

Injection is one of the most dangerous and common vulnerabilities highlighted by :contentReference[oaicite:0]{index=0} because it can lead to **complete system compromise**.

---

## Why Injection Attacks Are Dangerous

Injection attacks can allow attackers to:
- Bypass authentication
- Read sensitive data
- Modify or delete data
- Execute system commands
- Take full control of servers

These attacks often succeed because of **poor input handling** and **insecure coding practices**.

---

## Common Types of Injection Attacks

### 1. SQL Injection (SQLi)

Occurs when malicious SQL code is inserted into database queries.

#### Example

```sql
SELECT * FROM users 
WHERE username = 'admin' AND password = '' OR '1'='1';


