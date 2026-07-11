# Task 15 :Create COMMIT-CONVENTIONS.md documenting:
• The commit format you followed (type: subject)
• Types used (feat, fix, docs, chore, refactor, test)
• Examples of good vs bad commit messages from your actual history
• Why consistent commit messages matter for teams


#  The commit format you followed (type: subject)
---> Commit Format

I followed the following commit message format:

```
<type>: <short description>
```

Example:

```
feat: add navigation container
docs: update README for PR demo 2
style: style navigation bar
```

This format makes it easy to understand the purpose of each commit.

---

#  Types used (feat, fix, docs, chore, refactor, test)
---> Commit Types Used
----------------------------------------------------------------------------------------------------------------------------------------------
| Type     | Purpose                                               | Example from my repository                                               |
|----------|-------------------------------------------------------|--------------------------------------------------------------------------|
| feat     | Adds a new feature                                    | `feat: add navigation container in index.html file`                      |
| fix      | Fixes a bug or issue                                  | `fix: update footer on main` (not used in this project)                  |
| docs     | Documentation changes                                 | `docs: create RECOVERY.md and update the task                                                                        10 documentation from branch main`                                |
| chore    | Maintenance tasks                                     | Example: `chore: update dependencies` (not used in this project)         |
| refactor | Improves existing code without changing functionality | Example: `refactor: simplify navigation code` (not used in this project) |
| test     | Adds or updates tests                                 | Example: `test: add unit tests` (not used in this project)               |
| style    | Formatting or styling changes                         | `style: style navigation bar`                                            |
-----------------------------------------------------------------------------------------------------------------------------------------------
---

# Examples of good vs bad commit messages from your actual history
---> Good Commit Messages (from history)

These commit messages clearly describe what was changed:

```
feat: add navigation container in index.html file
feat: add navigation links in index.html
style: style navigation bar
feat: add footer container
feat: add footer container with 2nd commit
feat: add sidebar container
feat: add sidebar heading
feat: add sidebar links in container
docs: update README After merge
docs: create RECOVERY.md and update the task 10 documentation from branch main
docs: update README for PR demo 1
docs: update README for PR demo 2
```
---> # Bad Commit Messages (from my repository)

Some commit messages in my repository are vague and do not clearly explain the change.

Examples:

```

WIP
Fix
oops
no change
```

These messages do not describe what code was changed or why the change was made.

```
# Why Consistent Commit Messages Matter

--> Using consistent commit messages helps the team because:

- It makes the Git history easy to read.
- Developers can quickly understand what each commit changed.
- It helps during code reviews.
- It makes debugging easier using `git log`.
- It helps identify feature, documentation, and bug-fix commits.
- It improves collaboration when multiple developers work on the same repository.
- It creates a clean and professional commit history.

---