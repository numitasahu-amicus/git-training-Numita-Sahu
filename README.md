# Git Training Project

**Name:** Numita Sahu  
**Training Batch:** 2026  
**Date:** 09-07-2026  

## Project Description

This project was created to practice Git and GitHub workflows. It covers both basic and advanced Git concepts through hands-on tasks and practical exercises.

## Project Overview

This repository was created as part of the Git Training assignment. It demonstrates the use of Git fundamentals and advanced Git features, including:

- Git repository initialization
- Branch creation and management
- Merging and resolving merge conflicts
- Rebasing and interactive rebase
- Stashing changes
- Cherry-picking commits
- Reverting and resetting commits
- Recovering commits using Git Reflog
- Creating and managing Git tags
- Pull Requests and code reviews
- Git hooks
- Git Blame for code history analysis



##  Setup Instructions

-> Clone the Repository

```bash
git clone <repository-url>
```
->  Open the Project

```bash
cd git-training-Numita-Sahu
code .
```
-> Check Git Configuration

```bash
git config --global user.name
git config --global user.email
```
-> View Repository Status

```bash
git status
```

---


# Tasks Related Question Answers

#Task 2 ==> .gitignore assignment

Q1 : What happens if you forget .gitignore on the first commit?
Ans: ## What happens if you forget .gitignore?

If .gitignore is not added before the first commit, untracked files like node_modules, IDE settings, or build outputs may already be tracked by Git.

Q2 : How to fix it?
Ans :
1. Create a .gitignore file.
2. Remove tracked ignored files:
    git rm -r --cached 

3. Add files again.
    git add .

4. Commit the changes.
    git commit -m "remove ignored files"



## Navigation Feature  ---> task 6 -> make changes

Navigation feature will be merged from feature branch.

## task 6 :: After merging 
 

Task 6 : Switch back to main. Make a change to a DIFFERENT file than what you touched in the feature branch. Commit and push. Now merge "feature/add-navigation" into main. This should be a fast-forward merge (explain in README why it's fast-forward if it is, or why it wasn't). 
Ans :: In Assignment mentions a fast-forward merge, a new commit was created on main before merging. Because both main and feature/add-navigation are differnt ,so  Git performed a 3-way merge instead of a fast-forward merge.


## Task 8 -> Question :: Explain in README: When should you rebase vs merge? What's the golden rule of rebasing?  
--> When should you rebase vs merge?
    ->  Merge : Use Merge when working with shared or public branches. It combines changes without changing the existing commit history and is safe for team collaboration.
        Rebase : Use Rebase on your local feature branch to update it with the latest changes from main. It creates a clean, linear commit history by replaying your commits on top of the latest branch.

--> Golden Rule of Rebasing
    ->  Never rebase commits that have already been pushed to a shared/public branch. Rebase changes commit history, which can cause problems for other people working on the same branch.



## For task 11 --> make the quick fix example 


## This updatation is for task 13 example fram branch pr-demo-2
## This update is done for task 13 from branch feature/pr-demo-1


