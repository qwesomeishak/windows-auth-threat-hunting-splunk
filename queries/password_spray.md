# Password Spray Detection

## Objective
Identify password spray attacks where a single source IP attempts login across multiple user accounts.

---

## SPL Query

```spl
index=soc_lab event_code=4625
| stats dc(username) as unique_users, count as total_attempts by src_ip
| where unique_users >= 3 AND total_attempts >= 5
| sort - unique_users
