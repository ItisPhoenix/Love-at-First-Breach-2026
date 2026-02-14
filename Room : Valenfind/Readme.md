## 🔗 Full Exploit Chain



```

LFI →

Read app.py →

Extract ADMIN_API_KEY →

Call /api/admin/export_db →

Download DB →

Extract Flag

```



---



## 📊 Vulnerability Summary



| Vulnerability          | Type                    | Severity |

| ---------------------- | ----------------------- | -------- |

| Local File Inclusion   | Path Traversal          | Critical |

| Source Code Disclosure | Information Disclosure  | Critical |

| Hardcoded Secret       | Credential Exposure     | High     |

| Broken Access Control  | Authorization Bypass    | Critical |

| Database Export        | Sensitive Data Exposure | Critical |



---



## 🧠 Key Takeaways



1. Client-side comments can reveal real vulnerabilities.

2. Error messages leak internal filesystem paths.

3. LFI often leads to full compromise when source code is readable.

4. Hardcoded secrets are extremely dangerous.

5. Header-only authentication is insecure.



---



## 🏁 Final Flag



```

THM{v1be_c0ding_1s_n0t_my_cup_0f_t3a}

```
