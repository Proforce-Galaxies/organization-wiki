# Git Workflow

---

## 1️⃣ Branch Strategy
- **main** → Production-ready code
- **develop** → Integration branch
- **feature/** → New features
- **bugfix/** → Bug fixes
- **hotfix/** → Urgent fixes in production

---

## 2️⃣ Workflow Steps
1. Branch from `develop` for new features.
2. Commit changes with proper messages.
3. Push branch and open a PR to `develop`.
4. Once `develop` is stable, and verified by Unit leads, merge into `main` with a release tag.

---

## 3️⃣ Best Practices
- Pull latest changes before starting work.
- Keep branches short-lived.
- Rebase instead of merge when updating feature branches.
