# Cross-Unit Collaboration Guide

---

## 1️⃣ Purpose
Enable different units to work together efficiently without breaking project isolation.

---

## 2️⃣ Collaboration Models
- **Shared Repo Collaboration**  
  Invite members from other units directly into the repo’s team.
- **Fork & Pull Collaboration**  
  Other unit forks the repo, then creates PRs for changes.

---

## 3️⃣ Temporary Access
If another unit needs access:
1. Unit Lead requests access via Org Admin.
2. Admin adds user to the repo with appropriate permissions.
3. Access is revoked once collaboration is done.

---

## 4️⃣ Communication Protocol
- Use GitHub Discussions for technical Q&A.
- Tag other units in PRs/issues using `@team-name`.
- Major decisions documented in `org-docs` → `collaboration-guide.md`.

---

## 5️⃣ Example Workflow
1. GIS unit needs aerospace CAD data.
2. Aerospace lead grants read access to GIS team.
3. GIS forks repo → makes modifications.
4. GIS submits PR → Aerospace lead reviews & merges.

---

## 6️⃣ Etiquette
- Respect ownership boundaries.
- No direct merges to `main` in other units’ repos.
- Document all cross-unit changes in the PR description.
