# Git Sparse-Checkout Guide

## Overview
Sparse-checkout allows you to work with only specific directories or files from a large repository, rather than cloning the entire codebase. This is useful when you only need to work on a specific subsystem or component.

## Benefits
- **Faster cloning**: Download only the metadata and history, not all file contents
- **Reduced disk space**: Only checkout the directories you need
- **Improved performance**: Work with a smaller working directory

---

## Setup Instructions

### Step 1: Create Your Working Directory
Create a new folder where you want to clone the repository:

```bash
mkdir <project-folder-name>
cd <project-folder-name>
```

### Step 2: Clone with Sparse-Checkout
Clone the repository using the partial clone feature:

```bash
git clone --filter=blob:none --sparse <git-repo-url>
```

**What this does:**
- `--filter=blob:none`: Downloads only git metadata (commits, trees, history) without file contents
- `--sparse`: Checks out only the root directory initially

### Step 3: Navigate to Repository
```bash
cd <repository-name>
```

### Step 4: Add Specific Directories or Files
Specify which directories or files you want to work with (relative to the repository root):

```bash
git sparse-checkout add <path/to/directory>
```

**Examples:**
```bash
# Add a specific subdirectory. For example:
git sparse-checkout add src/backend
git sparse-checkout add electrical/circuits

# Add multiple directories. For example:
git sparse-checkout add src/backend
git sparse-checkout add docs

# Add a specific file. For example:
git sparse-checkout add README.md
git sparse-checkout add electrical/circuits/BMS
```

**To view current sparse-checkout configuration:**
```bash
git sparse-checkout list
```

### Step 5: Create a Branch (Optional)
Create a new branch for your changes:

```bash
git checkout -b <branch-name>
```

Use a descriptive branch name (e.g., `update/EPS-circuitry` or `team/backend-updates`).

---

## Making Changes and Pushing

### Step 1: Make Your Changes
Edit files in your sparse-checked-out directories as needed.

### Step 2: Stage Your Changes
**Important**: Ensure you are in the repository root directory (not inside a subdirectory).
For example:
✅ Correct location: `C:\Users\USER\Documents\Projects\REPO_NAME\`  
❌ Incorrect location: `C:\Users\USER\Documents\Projects\REPO_NAME\sub-directory\`

Stage all changes:
```bash
git add .
```

Or stage specific files:
```bash
git add path/to/file
```

### Step 3: Commit Your Changes
```bash
git commit -m "Brief description of your changes"
```

**Example:**
```bash
git commit -m "Update authentication logic in backend module"
git commit -m "Update EPS circuitry"
```
or
```bash
git commit -m "Update EPS circuitry"
```

### Step 4: Push to Remote
Push your changes to the remote repository:

```bash
# First time pushing a new branch
git push -u origin <branch-name>

# Subsequent pushes to the same branch used at first push
git push
```

---

## Troubleshooting

### View sparse-checkout status
```bash
git sparse-checkout list
```

### Disable sparse-checkout (checkout entire repo)
```bash
git sparse-checkout disable
```

### Add more directories later
```bash
git sparse-checkout add <additional/path>
```

### Remove a directory from sparse-checkout
Edit the sparse-checkout file manually:
```bash
git sparse-checkout set <path1> <path2>
```

---

## Additional Resources
- [Git Sparse-Checkout Documentation](https://git-scm.com/docs/git-sparse-checkout)
- Contact the team lead if you need assistance with repository structure
- Go through the [Organization Wiki](https://github.com/Proforce-Galaxies/organization-wiki) for more information


