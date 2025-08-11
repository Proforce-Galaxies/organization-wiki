# Security & Access Control Policy

---

## 1️⃣ Core Principles
- Least privilege: Only give the minimum access needed.
- Segmentation: Units are isolated by default.
- Auditability: All changes traceable via PRs.

---

## 2️⃣ Access Levels
- **Owner/Admin**: Org-level control, can manage teams & settings.
- **Maintainer**: Can manage team members and repos.
- **Write**: Can push code, open PRs.
- **Read**: View-only access.

---

## 3️⃣ Branch Protection
Main branch must have:
- Pull request required before merging
- At least 1 Unit Lead approval
- No direct pushes to `main`

---

## 4️⃣ Sensitive Data
- No credentials in code.
- Use `.env` files (never commit them).
- Rotate secrets every 90 days.

---

## 5️⃣ Incident Response
If a security incident occurs:
1. Notify Org Admins immediately.
2. Revoke access of suspected accounts.
3. Open a private security issue in `org-docs`.
4. Document the incident and resolution.

---

## 6️⃣ Review & Audit
- Quarterly review of all repo access.
- Remove inactive members.
- Verify branch protection rules are still applied.
