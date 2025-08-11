---

## 🚀 Quick Start for New Units

This checklist will guide any new team (unit) through setting up their workspace in the Proforce Galaxies organization.

### 1️⃣ Request Your Team Space
- Contact an **Org Admin** to create your team in GitHub.
- Choose a **Team Name** and **Description**.
- Decide if your team is:
  - **Visible** (other teams can see you exist)  
  - **Secret** (only members and admins can see you)

---

### 2️⃣ Create Your Repository
- Repos are created **under the Organization**, not inside the team directly.
- **Visibility options:**
  - `Private` (default) — Only your team and invited collaborators.
  - `Internal` — Visible to all org members (if GitHub Enterprise).
  - `Public` — Visible to everyone on the internet.
- Add:
  - **README.md**
  - **.gitignore**
  - **License** (if needed)

---

### 3️⃣ Configure Branch Protections
- Protect `main` (and/or `dev`) branch.
- Require pull requests before merging.
- Require approval from **Code Owners**.
- Enable "Require conversation resolution before merging".

---

### 4️⃣ Assign Roles
- Add members to your team.
- Assign `Maintainer` role to leads.
- Assign `Member` role to regular contributors.

---

### 5️⃣ Set Up Templates
- Add `CONTRIBUTING.md`, `CODEOWNERS`, and pull request template from the `/templates` directory in this `org-docs` repo.
- Adapt them to your team’s needs.

---

### 6️⃣ Establish Your Workflow
- Follow the [Git Workflow Guide](tools-workflows/git-workflow.md) for branch naming and PR processes.
- Document any **team-specific processes** in your own repo’s `README.md`.

---

### 7️⃣ Collaborate Across Units
- If you need to work with another team:
  - Invite their members to your repo temporarily.
  - Use a **feature branch** for collaborative work.

---

✅ **Once completed**, your team is fully integrated into the Proforce Galaxies development ecosystem.
