# Failed Logins by Source IP

## Objective
Identify source IP addresses generating a high number of failed login attempts.

---

## SPL Query

```spl
index=soc_lab event_code=4625
| stats count by src_ip, username
| sort - count
