# Security Incident Report

## Incident Title
Brute Force and Password Spray Detection in Windows Authentication Logs

---

## Summary
An investigation was conducted on Windows authentication logs to identify suspicious login activity. The analysis revealed patterns consistent with brute force and password spray attacks targeting multiple user accounts.

---

## Scope
- Data Source: Windows Event Logs
- Events Analysed:
  - Event ID 4625 (Failed Login)
  - Event ID 4624 (Successful Login)

---

## Key Findings

### 1. Brute Force Attack
- Multiple failed login attempts from a single IP address
- Followed by a successful login
- Indicates password guessing behaviour

---

### 2. Password Spray Attack
- Single IP targeting multiple user accounts
- Low number of attempts per account
- Indicates use of common passwords across accounts

---

### 3. Normal User Activity
- Occasional failed login attempts followed by success
- Likely due to user error

---

## Indicators of Compromise (IOCs)
- Suspicious source IP addresses
- High volume of failed login attempts
- Repeated login attempts targeting specific accounts
- Successful login after multiple failures

---

## Risk Assessment
- Brute Force Activity: High Risk
- Password Spray Activity: Medium to High Risk

---

## MITRE ATT&CK Mapping
- T1110 – Brute Force

---

## Recommendations
- Lock or disable affected user accounts
- Block suspicious IP addresses at firewall level
- Implement account lockout policies
- Enforce Multi-Factor Authentication (MFA)
- Monitor authentication logs continuously

---

## Conclusion
The investigation confirms malicious login activity consistent with brute force and password spray attacks. Immediate action is required to mitigate risks and prevent unauthorized access to systems.
