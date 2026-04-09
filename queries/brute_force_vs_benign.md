# Brute Force vs Normal Login Behaviour

## Objective
Differentiate between malicious brute force activity and normal user login behaviour.

---

## SPL Query

```spl
index=soc_lab event_code=4625
| stats count as failed_attempts by src_ip, username
| eval activity_type=case(
    failed_attempts >= 5, "Suspicious (Possible Brute Force)",
    failed_attempts >= 3 AND failed_attempts < 5, "Moderate (Needs Review)",
    failed_attempts < 3, "Likely Normal Behaviour"
)
| sort - failed_attempts
