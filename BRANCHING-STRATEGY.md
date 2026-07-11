TAsk 14 :: Document your branching strategy in BRANCHING-STRATEGY.md:
• Which strategy you followed and why (Git Flow or Trunk-Based Development)
• Draw a branch diagram (text-based is fine) showing main, develop (if applicable), feature branches, and hotfix
• Rules: When to branch? From where? How to name branches? When to merge vs rebase?



# Branching Strategy
---> Which strategy you followed and why (Git Flow or Trunk-Based Development)
## Strategy Followed
I followed a "Git Flow-inspired branching strategy".

Although I did not create a separate `develop` branch, I used the same idea by creating individual feature branches from `main`, completing the work there, and then merging the changes back into `main`.

This strategy allowed me to:
- Work on different features independently.
- Keep the `main` branch stable.
- Practice merge, rebase, cherry-pick, stash, revert, and pull request workflows.

---

 ---> Draw a branch diagram (text-based is fine) showing main, develop (if applicable), feature branches, and hotfix 
 

c63bf8f Initial Commit
        │
        ▼
      main
        │
        ├── feature/add-navigation ───────────────► merged (Fast-forward)
        │
        ├── feature/add-footer ───────────────────► merged (Merge Commit)
        │
        ├── feature/add-sidebar ──────────────────► Rebased → merged
        │
        ├── feature/stash-demo
        │
        ├── feature/rebase-demo
        │
        ├── hotfix/urgent-fix (Cherry-pick)
        │
        ├── feature/pr-demo-1 ────────────────────► Merge Commit PR
        │
        └── feature/pr-demo-2 ────────────────────► Squash Merge PR
        

---

Develop Branch: Not used in this project.
---

# Branching Rules

----> Rules: When to branch? From where? How to name branches? When to merge vs rebase?


## When to create a branch?

Create a new branch whenever starting:
- A new feature
- A bug fix
- A hotfix
- An experiment
- A Pull Request demonstration

---

## From where should branches be created?

All feature branches and the hotfix branch should be created from the latest `main` branch.

Example:

```bash
git switch main
git pull origin main
git switch -c feature/add-navigation
```

---

## How to name branches? ==>  Branch Naming Convention

### Feature branches

```
feature/<feature-name>
```

Examples:

```
feature/add-navigation
feature/add-footer
feature/add-sidebar
feature/rebase-demo
feature/stash-demo
feature/pr-demo-1
feature/pr-demo-2
```

### Hotfix branch

```
hotfix/<fix-name>
```

Example:

```
hotfix/urgent-fix
```

---

# When to merge vs rebase?

->  When to Merge

Use merge when a feature branch is complete and needs to be integrated into `main`.

Examples from this project:
- feature/add-navigation
- feature/add-footer

Merging preserves the complete branch history. A merge commit is created when required.

---

-> When to Rebase

Use rebase to update a feature branch with the latest commits from `main` before merging.

Example:

```
feature/add-sidebar
```

Rebasing creates a cleaner and linear commit history.

---


