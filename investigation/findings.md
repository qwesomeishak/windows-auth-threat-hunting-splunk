# Investigation Findings

## Summary
Analysis of Windows authentication logs revealed suspicious login activity consistent with brute force and password spray attacks.

---

## Key Findings

### 1. Brute Force Activity
- Multiple failed login attempts from a single source IP
- Followed by a successful login
- Targeted specific user accounts

### 2. Password Spray Activity
- Single IP targeting multiple user accounts
- Low number of attempts per user
- Pattern spread across different accounts

### 3. Normal Behaviour
- Some failed logins followed by success (likely user error)
- Low number of attempts (1–2)

---

## Suspicious Indicators
- High number of failed login attempts
- External IP addresses
- Repeated targeting of same account
- Successful login after multiple failures
