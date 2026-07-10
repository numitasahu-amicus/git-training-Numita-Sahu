## Task 10 : Document BOTH approaches in RECOVERY.md: When to use revert vs reset? Why is reset dangerous on shared branches? 
---> Recovering from Mistakes in Git
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

---> When should  use git revert vs git reset?
-> Use git revert when:
- I we have already pushed the commit to a shared branch.
- Other developers may have pulled the commit.
- You want to keep a complete history of what happened.

-> Use git reset when:
- The commits have not been shared.
- You want to remove commits from your local history.
- You are cleaning up your own branch before sharing it.

---> Why is git reset dangerous on shared branches?

git reset --hard rewrites Git history by moving the branch pointer to an earlier commit. If the branch has already been pushed and other developers have based their work on it, resetting and force-pushing can remove commits from the shared history and create conflicts for everyone. For this reason, git revert is the safer choice for shared branches.

