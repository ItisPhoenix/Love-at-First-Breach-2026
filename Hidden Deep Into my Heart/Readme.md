## 🔗 Full Exploit Chain

```
robots.txt →

Discover hidden path →

Find /cupids_secret_vault/ →

Enumerate administrator panel →

Extract password from robots comment →

Login as admin →

Retrieve Flag
```

---

## 📊 Vulnerability Summary

| Vulnerability        | Type                    | Severity |
| -------------------- | ----------------------- | -------- |
| Sensitive Disclosure | robots.txt Exposure     | Medium   |
| Hidden Admin Panel   | Improper Access Control | High     |
| Credential Exposure  | Hardcoded Password Leak | High     |
| Weak Authentication  | Credential Reuse        | High     |

---

## 🧠 Key Takeaways

1. `robots.txt` is public and should never contain sensitive data.
2. Comments in public files are visible to attackers.
3. Hidden paths are not access control.
4. Enumeration is often more powerful than exploitation.
5. Always test discovered strings as credentials.

---

## 🏁 Final Flag

```
THM{l0v3_is_in_th3_r0b0ts_txt}
```
