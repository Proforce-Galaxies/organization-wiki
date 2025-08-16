# Git Workflow Guide

A clear workflow for safe and efficient collaboration on our projects.

---

## 1️⃣ Branching Strategy

- **main** → Production-ready code (always stable, tagged releases).  
- **develop** → Integration branch (features and fixes get merged here first).  
- **feature/<name>** → New features in progress.  
- **bugfix/<name>** → Regular bug fixes.  
- **hotfix/<name>** → Urgent fixes on production.  

---

## 2️⃣ Workflow Steps

### Start from develop
Create a new branch for your work.

```
git checkout develop
git pull origin develop
git checkout -b feature/add-login-page
```

### Make commits with meaningful messages
```
git add .
git commit -m "Add login page with form validation"
```

### Push your branch and open a Pull Request (PR) → develop.

### Merge develop → main
Once tested and approved by Unit Leads, `develop` is merged into `main` and tagged for release.

---

## 3️⃣ Best Practices

🔄 **Always pull the latest changes before starting work:**
```
git fetch origin
git pull origin develop
```

⏳ **Keep branches short-lived** → finish and merge quickly.  

📐 **If working alone, prefer rebase over merge when syncing feature branches:**
```
git checkout feature/add-login-page
git fetch origin
git rebase origin/develop
```

**Else, better to merge**
```
git checkout feature/add-login-page
git fetch origin
git merge origin/develop
```

---

## 4️⃣ Safe Collaboration Workflow

In a terminal and desired directory to wor on the repo,

### Setup (first time only)
```
git clone https://github.com/<org>/<repo>.git
cd <repo>
```

### Create your branch
❌ **Don’t work directly on main or develop.**  
✅ **Always create a feature branch:**
```
git checkout -b feature/<your-feature-name>
```

### Commit your changes
```
git add .
git commit -m "Brief description of your change"
```

### Sync with the latest changes
Before pushing, make sure your branch is updated with the latest in the remote repo to avoid overwriting updates other collaborators have merged during the time you were working.:

```
# Update local develop
git checkout develop
git pull origin develop

# Update your branch
git checkout feature/<your-feature-name>
git merge develop
```

✅ If no conflicts (no one touched the same files as you in that time) → merge succeeds.  
⚠️ If conflicts appear → resolve them, then:
```
git add <resolved-files>
git commit
```

### Push and open a PR
```
git push origin feature/<your-feature-name>
```

Open a PR on GitHub → `feature/<your-feature-name>` → `develop`.  
Request a review from your team.

### After PR is merged
```
git checkout develop
git pull origin develop
```
You can also delete the old local feature branch (optional)
```
git branch -d feature/<your-feature-name>
```

---

## 5️⃣ Why This Workflow Matters

✅ Prevents overwriting teammates’ work.  
✅ Keeps work organized with isolated feature branches.  
✅ Simplifies reviews with smaller, focused PRs.  
✅ Ensures `main` always stays production-ready.  

---