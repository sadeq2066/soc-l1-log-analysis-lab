# Incident Report

## Incident Summary

Authentication-related events were investigated using Linux system logs.

The investigation focused on identifying failed authentication attempts and suspicious indicators.

## Investigation Performed

Authentication logs were collected using `journalctl`.

Evidence was saved into:
- auth_failed_logins.txt
- suspicious_ips.txt

Log filtering and indicator extraction techniques were used during analysis.

## Findings

- Authentication events were identified successfully.
- No remote IP addresses were detected during investigation.
- Activity was determined to be local lab-generated test activity.

## Severity

Low

## Recommendations

- Continue monitoring authentication logs regularly.
- Investigate repeated authentication failures.
- Restrict unnecessary remote access.
- Enforce strong password policies.

## Outcome

The investigation workflow, evidence collection, and documentation process were completed successfully as part of a SOC L1 log analysis lab.
