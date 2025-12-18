# Large-Scale SQL Injection Web Scanning

## Alert Summary
High-volume web requests containing SQL injection payloads targeting multiple DMZ services.

---

## Investigation Details (5W Analysis)

### Who
- Source IP: 5.178.87.180
- No authenticated user involved

### What
- Automated web scanning with SQL injection payloads such as `' OR '1'='1`
- 865,700 requests across 112,569 unique URIs
- Targeted multiple production-facing services

### When
- Start time: Noted during alert generation
- End time: Ongoing at time of investigation

### Where
- Target systems:
  - DMZ-WEBFRONT-PRD
  - DMZ-WEBAPI-PRD
  - DMZ-MSEXCHANGE-2013

### Why (Final Verdict Reasoning)
- Presence of explicit SQL injection payloads
- Abnormally high request volume
- Broad URI enumeration
- Targeting critical DMZ resources
This behavior exceeds normal bot scanning and indicates malicious reconnaissance or exploitation attempts.

---

## Verdict
Confirmed Malicious Activity

## Severity
High

## Actions Taken
- Recommended IP blocking at firewall/WAF
- Log review for successful exploitation attempts
- Escalation to L2/SOC lead

## Lessons Learned
- High request volume + injection payloads = malicious
- Context separates scans from real threats
