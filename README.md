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
