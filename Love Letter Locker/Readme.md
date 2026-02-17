
# 🔗 Exploit Flow

```
Register →  

Login →  

Observe global archive count →  

Create new letter →  

Identify sequential ID structure →  

Modify ID in URL →  

Access another user’s letter →  

Retrieve flag
```

---

# 📊 Vulnerability Summary

| Vulnerability Type          | Category                | Severity |
| --------------------------- | ----------------------- | -------- |
| IDOR                        | Broken Access Control   | Critical |
| Sequential IDs              | Predictable Resource ID | High     |
| Missing Authorization Check | Logic Flaw              | Critical |

---

# 🧠 Key Takeaways

1. Authentication does not equal authorization.
2. Every object access must verify ownership.
3. Sequential numeric IDs are dangerous when not protected.
4. Broken access control remains one of the most common web vulnerabilities.
5. Enumeration attacks require no advanced tooling — only logic.

---

# 🛡 Security Recommendations

To prevent this vulnerability:

* Enforce strict ownership validation in all database queries.
* Implement object-level access control.
* Avoid exposing predictable identifiers where possible.
* Conduct regular access control testing.

---

# 🏁 Flag

```
THM{1_c4n_r3ad_4ll_l3tters_w1th_th1s_1d0r}
```

---

# 🏁 Conclusion

This challenge demonstrates that even simple applications can suffer from critical security flaws when proper authorization checks are missing.

The exploit required no injection, no brute force, and no advanced tooling — only observation and logical reasoning.

Broken Access Control continues to be one of the most impactful vulnerabilities in modern web applications.

---
