# Commands Used

## Collect authentication events
sudo journalctl --since today | grep -Ei "failed password|authentication failure|failed su|incorrect password"

Purpose:
Filter authentication-related events from system logs.

---

## Save failed authentication evidence
sudo journalctl --since today | grep -Ei "failed password|authentication failure|failed su|incorrect password" > evidence/auth_failed_logins.txt

Purpose:
Store investigation evidence.

---

## Review saved evidence
cat evidence/auth_failed_logins.txt

Purpose:
Inspect collected authentication events.

---

## Extract remote host indicators
grep -Eo "rhost=[^ ]+" evidence/auth_failed_logins.txt | sort | uniq -c

Purpose:
Identify repeated remote hosts or suspicious IP activity.

---

## Save suspicious IP evidence
grep -Eo "rhost=[^ ]+" evidence/auth_failed_logins.txt | sort | uniq -c > evidence/suspicious_ips.txt

Purpose:
Store extracted indicators separately.

---

## Display project structure
tree

Purpose:
Verify investigation project organization.
