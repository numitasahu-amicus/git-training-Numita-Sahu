#Git training

Name : Numita Sahu
Training batch : 2026
Date : 09-07-2026
Project Description:
This project is created to practice Git and GitHub workflow


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


##Task 8 -> Question :: Explain in README: When should you rebase vs merge? What's the golden rule of rebasing?  
