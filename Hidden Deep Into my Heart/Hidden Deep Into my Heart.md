# 💘 Cupid’s Secret Vault – CTF Walkthrough

## 🧩 Challenge Overview

Target:

```
http://10.49.129.201:5000
```

The objective was to uncover the secret hidden inside Cupid’s Vault.

---

# 🔎 Step 1 – Initial Recon

Opening the main page revealed a simple landing page:

![Landing Page](images/landing-page.png)

The page source contained no visible forms, scripts, or hidden functionality.

This suggested:

* The real functionality was hidden behind another route.
* Enumeration would be required.

---

# 📁 Step 2 – Checking `robots.txt`

Navigating to:

```
http://10.49.129.201:5000/robots.txt
```

Revealed:

```
User-agent: *
Disallow: /cupids_secret_vault/*

# cupid_arrow_2026!!!
```

Screenshot:

![Robots.txt](images/robots.png)

## 🔥 Key Findings

1. Hidden directory:

   ```
   /cupids_secret_vault/
   ```

2. Suspicious string:

   ```
   cupid_arrow_2026!!!
   ```

This is a classic CTF pattern — credentials hidden inside `robots.txt`.

---

# 🔐 Step 3 – Accessing the Secret Vault

Navigating to:

```
http://10.49.129.201:5000/cupids_secret_vault/
```

Displayed:

![Vault Landing](images/vault-landing.png)

The message stated:

> "You've found the secret vault, but there's more to discover..."

This confirmed the path was correct, but something deeper existed.

---

# 👑 Step 4 – Finding the Administrator Panel

Further enumeration revealed:

```
/cupids_secret_vault/administrator
```

Which displayed an admin login panel:

![Admin Login](images/admin-login.png)

---

# 🔓 Step 5 – Credential Testing

From `robots.txt`, we had:

```
cupid_arrow_2026!!!
```

Tried logging in with:

| Username | Password            |
| -------- | ------------------- |
| admin    | cupid_arrow_2026!!! |

And it worked.

No SQL injection required.
No brute force required.

This was simple credential reuse exposed via `robots.txt`.

---

# 🏁 Final Flag

After successful login, the flag was revealed:

```
THM{l0v3_is_in_th3_r0b0ts_txt}
```
