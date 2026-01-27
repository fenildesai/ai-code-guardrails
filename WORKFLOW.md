# Git Workflow for AI Code Guardrails

## ✅ Current Status
- **Main Branch**: All cleanup complete and pushed ✓
- **Current Branch**: `feature/update-guardrails-content` (created for feature development)

## 📋 Feature Branch Workflow

### Step 1: Make Changes on Feature Branch
```bash
# You're already on feature/update-guardrails-content
git branch  # verify you're on the right branch
```

### Step 2: Stage and Commit Changes
```bash
# See what changed
git status

# Stage specific files or all changes
git add context_engineering_leadership.html guardrails_explorer.html
# OR add all changes
git add .

# Commit with descriptive message
git commit -m "feat: [description of changes]"
# Examples:
# git commit -m "feat: Add new template to guardrails explorer"
# git commit -m "fix: Update leadership presentation content"
```

### Step 3: Push Feature Branch
```bash
git push origin feature/update-guardrails-content
```

### Step 4: Create Pull Request on GitHub
1. Go to: https://github.com/fenildesai/ai-code-guardrails
2. GitHub will show a prompt to create a PR from your feature branch
3. Click **"Compare & pull request"**
4. Fill in:
   - **Title**: Brief summary (e.g., "Update guardrails explorer with new templates")
   - **Description**: Explain what changed and why
5. Click **"Create pull request"**

### Step 5: Code Review & Merge
1. Review the changes in the PR
2. Once satisfied, click **"Merge pull request"**
3. Choose merge strategy: **"Squash and merge"** (recommended for clean history)
4. Click **"Confirm merge"**
5. Delete the feature branch (GitHub will offer this option)

### Step 6: Sync Local Repository
```bash
# Switch back to main
git checkout main

# Pull the merged changes
git pull origin main

# Delete local feature branch
git branch -d feature/update-guardrails-content
```

## 🎯 Quick Commands Cheat Sheet

```bash
# Create a new feature branch (alternative to current setup)
git checkout -b feature/your-feature-name

# Check current branch
git branch

# Switch between branches
git checkout main
git checkout feature/your-feature-name

# See differences
git diff                           # unstaged changes
git diff --staged                  # staged changes
git diff main..feature/branch-name # compare branches

# Undo uncommitted changes
git restore <filename>

# Undo uncommitted staged changes
git restore --staged <filename>

# Amend last commit (before push)
git add .
git commit --amend --no-edit
```

## 📁 Key Files Structure

```
TheOpeningBatsman/
├── context_engineering_leadership.html  (Leadership briefing)
├── ai-code-guardrails/ (submodule)
│   ├── index.html (Guardrails home)
│   ├── guardrails_explorer.html (Template explorer)
│   ├── copilot-instructions.md (Base framework)
│   └── README.md
├── pr_reviewer.ps1 (PR review script)
├── azure-pipelines.yml (CI/CD config)
└── ... (other presentation files)
```

## 🔄 Repositories

- **Parent Repo**: https://github.com/fenildesai/ai-code-guardrails (main site)
- **Submodule**: https://github.com/fenildesai/ai-code-guardrails (guardrails framework)

## ✨ Best Practices

1. **Commit Often**: Small, logical commits are easier to review
2. **Meaningful Messages**: Use clear commit messages
3. **One Feature Per Branch**: Keep branches focused
4. **Squash Before Merge**: Keeps main branch clean
5. **Delete Branches**: Clean up after merging
6. **Pull Before Push**: Avoid conflicts with `git pull` before pushing

---

**Last Updated**: January 27, 2026
