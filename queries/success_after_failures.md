# Successful Login After Multiple Failed Attempts

## Objective
Detect instances where a successful login occurs shortly after multiple failed login attempts.

---

## SPL Query

```spl
index=soc_lab (event_code=4625 OR event_code=4624)
| sort 0 _time
| streamstats window=5 count(eval(event_code=4625)) as failed_attempts by src_ip, username
| where event_code=4624 AND failed_attempts >= 3
| table _time, src_ip, username, failed_attempts
