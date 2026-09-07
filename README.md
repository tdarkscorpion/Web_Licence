# Talisman Online WebSuite — License & Domain Whitelist Authority

This repository is the central authority for domain licensing and whitelisting for the Talisman Online WebSuite (`DomainGuard` and `LicenseHandler`).

---

## Files

### 1. `license.json`
Central JSON configuration containing domain names and expiry dates.
```json
{
  "version": "2.0.0",
  "updated_at": "YYYY-MM-DD",
  "domains": {
    "yourdomain.com": "01 Dec 2030",
    "www.yourdomain.com": "01 Dec 2030"
  }
}
```

### 2. `whitelist.env` & `whitelist.txt`
Standard pipe-delimited format:
```text
domain.com | DD Mon YYYY
```

---

## How to Add or Update a Domain

1. Open `license.json` or `whitelist.env` in GitHub.
2. Add your new domain and expiry date.
3. Commit changes to `main`.
4. The website checks the remote authority on request or via the Admin Dashboard (`showLicenseRecheck()`).
