# Periodic Network Beaconing to Ubuntu Connectivity Check

## Alert Summary
Detected periodic outbound HTTPS connections resembling beaconing behavior.

---

## Investigation Details (5W Analysis)

### Who
- Host: prd-nginx-gc8610
- Process: /usr/bin/NetworkManager

### What
- Repeated HTTPS connections every ~60 seconds
- Total of 30 requests

### When
- Observed during monitoring window

### Where
- Destination domain: connectivity-check.ubuntu.com
- Destination port: 443

### Why (Final Verdict Reasoning)
- Domain is a legitimate Ubuntu endpoint
- Process is expected system service
- Behavior aligns with documented OS connectivity checks
- No additional malicious indicators observed

---

## Verdict
Benign / False Positive

## Severity
Low

## Actions Taken
- Alert closed
- Recommended whitelist tuning

## Lessons Learned
- Beaconing patterns require context
- Legitimate services can mimic C2 behavior
