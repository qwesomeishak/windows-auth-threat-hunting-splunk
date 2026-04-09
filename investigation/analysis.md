
# Analyst Assessment

## Classification

### Brute Force Attack
- High number of failed attempts from same IP
- Followed by successful login
- Classified as **True Positive**

---

### Password Spray Attack
- Single IP targeting multiple accounts
- Low attempts per account
- Classified as **True Positive**

---

### Normal User Behaviour
- Low number of failed attempts
- Eventual successful login
- Classified as **False Positive**

---

## Risk Level
- Brute force activity: High Risk
- Password spray activity: Medium to High Risk

---

## Recommended Actions

- Lock affected accounts
- Block suspicious IP addresses
- Enable account lockout policies
- Enforce Multi-Factor Authentication (MFA)
- Monitor authentication logs for repeated patterns

---

## Conclusion
The investigation confirms the presence of malicious authentication attempts consistent with brute force and password spray techniques. Immediate mitigation is recommended to prevent unauthorized access.
