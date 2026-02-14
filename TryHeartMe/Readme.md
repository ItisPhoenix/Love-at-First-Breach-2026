# 🔗 Full Exploit Chain

```
Register →

Inspect cookies →

Identify JWT →

Decode token using CyberChef →

Modify header to alg:none →

Modify role and credits →

Remove signature →

Replace cookie →

Gain admin privileges →

Access hidden product →

Purchase ValenFlag →

Extract flag
```

---

# 📊 Vulnerability Summary

| Vulnerability              | Type                        | Severity |
| -------------------------- | --------------------------- | -------- |
| JWT Misconfiguration       | alg:none acceptance         | Critical |
| Client-Side Role Control   | Privilege Escalation        | Critical |
| Client-Side Credit Control | Business Logic Manipulation | High     |
| Hidden Admin Functionality | Access Control Failure      | High     |

---

# 🧠 Key Takeaways

1. JWT signatures must always be validated server-side.
2. `alg: none` must be explicitly rejected.
3. Sensitive claims must not be client-controlled.
4. Authorization must not rely solely on token payload.
5. Business logic flaws can lead to full compromise.

---

# 🛡 Security Recommendations

To prevent this vulnerability:

* Enforce strict algorithm validation.
* Reject `alg:none` tokens.
* Validate signatures properly.
* Store sensitive attributes server-side.
* Avoid trusting client-modifiable claims.

---

# 📌 Conclusion

This challenge demonstrates a real-world vulnerability class:

> Improper JWT validation leading to privilege escalation.

No brute force.
No injection.
Just broken cryptographic trust.

---
