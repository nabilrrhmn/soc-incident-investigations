# HR Data Shared to External Email

## Alert Summary
Sensitive HR document shared outside the organization in violation of policy.

---

## Investigation Details (5W Analysis)

### Who
- User: m.boslan@tryhackme.thm (HR Lead)
- Device: LPT-HR-0988

### What
- Attempted download of full HR folder (blocked by DLP)
- Successful external sharing of "Employee Records (Updated)" spreadsheet

### When
- Start time: 18:30 UTC
- End time: 18:32 UTC

### Where
- Source system: Google Workspace
- Destination email: shadow18562@protonmail.thm
- Folder: HR Internal

### Why (Final Verdict Reasoning)
- Sharing sensitive employee records to a personal external email violates corporate data protection policies
- Attempted bulk download prior to sharing increases risk of data exfiltration

---

## Verdict
Policy Violation / Data Exfiltration Attempt

## Severity
High

## Actions Taken
- Escalated to Compliance team
- Recommended user communication and activity monitoring

## Lessons Learned
- DLP blocks downloads but sharing risk remains
- Insider activity requires context, not assumptions
