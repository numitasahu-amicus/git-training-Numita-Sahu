# tsk 10 : Document BOTH approaches in RECOVERY.md: When to use revert vs reset? Why is reset dangerous on shared branches? 
## > Recovering from Mistakes in Git
1. Using git revert

Command : git revert HEAD
what it does : 
git revert creates a new commit that reverses the changes made by a previous commit. The original commit remains in the project history, making this method safe for shared repositories.

2. Using git reset --hard

Command : git reset --hard HEAD~1
what it does : 
git reset --hard moves the branch pointer to an earlier commit and discards all changes in the working directory and staging area. The removed commits are no longer visible in the normal history.

3. Recovering with git reflog

Command : 
git reflog
git reset --hard <commit-id>
what it does : 
git reflog records every movement of HEAD. Even after a git reset --hard, the previous commit can usually be found in the reflog and restored using its commit ID.

## > When should  use git revert vs git reset?
-> Use git revert when:
- I we have already pushed the commit to a shared branch.
- Other developers may have pulled the commit.
- You want to keep a complete history of what happened.

-> Use git reset when:
- The commits have not been shared.
- You want to remove commits from your local history.
- You are cleaning up your own branch before sharing it.

## > Why is git reset dangerous on shared branches?

git reset --hard rewrites Git history by moving the branch pointer to an earlier commit. If the branch has already been pushed and other developers have based their work on it, resetting and force-pushing can remove commits from the shared history and create conflicts for everyone. For this reason, git revert is the safer choice for shared branches.


## Recovering with Git Reflog

After using `git reset --hard`, I recovered the lost commit using Git Reflog.

- step 1: View Reflog

```bash
git reflog
```

Git displayed all previous HEAD positions.

Example:

```text
HEAD@{0}: reset: moving to de670ef

```

### Step 2: Recover the Commit

```bash
git reset --hard <commit-id>
```

Example:

```bash
git reset --hard dbcb256
```

### Result

- The lost commit was successfully restored.
- The repository returned to the desired state.

---

# What I Learned

During this task, I learned the difference between `git revert` and `git reset --hard`. I understood that `git revert` is the safer option because it preserves commit history by creating a new commit, while `git reset --hard` rewrites history and should be used carefully. I also learned how `git reflog` can be used to recover commits after an accidental reset, making it a valuable tool for recovering lost work.
