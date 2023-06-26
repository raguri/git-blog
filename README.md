# Git Commands in Action: Navigating Your Repository with Confidence
Git is a distributed version control system that tracks changes to any set of files. Coordination of work among programmers is used during the development process of software. In addition to supporting distributed, non-linear workflows, it aims for speed, data integrity, and data integrity.

The most commonly used commands are categorized by their specific functionality.
- *git clone, git config, git add, git status, git commit, git push, git pull, git branch, git checkout, and git merge*

## Configuration:
- Creates a new Git repository: git init
  - *git init*
- To set the username: git config --global user.name “FirstName LastName”
  - *git config --global user.name “sasikumar.raguri”*
- To set the email: git config --global user.email “test@example.com”
  - *git config --global user.email “s.raguri@test.com”*
- Create Git aliases for frequently used commands: git config --global alias.<alias_name> <command>
  - *git config --global alias.st status (To create an alias “st” for “status”)*

## Managing Remote Repositories:

-  View remote repositories: git remote -v
    - *git remote -v* 
- Add a remote repository: git remote add <remote_name><remote_url>
  - *git remote add origin https://github.com/raguri/git-blog.git*
- Rename a remote repository: git remote rename <old_name> <new_name>
  - *git remote rename origin parent*
- Remove a remote repository: git remote remove <remote_name>
  - *git remote remove parent*

## Branch Management:
- Create a new branch: git branch <branch_name>
  - *git branch newBranch*
  - *git checkout -b newBranch origin/master*
- Switch to a branch: git checkout <branch_name>
  - *git checkout oldBranch*
  - *git checkout – (This will take us to the previous branch)*
- Rename a branch: git branch -m <new_branch_name>
  - *git branch -m newBranch (We should be in a branch to rename it)*
  - *git branch -m oldBranch newBranch*
- Delete a branch: git branch -d <branch_name>
  - *git branch -d newBranch*
  - *git branch -D git_blog (Force delete)*

## Committing Changes:
- Stage changes for commit: git add <file_name> or git add . (to add all changes)
  - *git add README.md  – To add a specific file to staged*
  - *git add .                  – To add all changes to staged*
  - *git add -A*
- Commit changes: git commit -m “Commit message”
  - *git commit –m “Update README.md file”*
- Amend a commit while keeping the same commit message: git commit --amend --no-edit
  - *git commit --amend --no-edit*

## History and Viewing Diff Changes:
- View commit history: git log
  - *git log --oneline --graph*
- Show changes in a file: git diff <file_name>
  - *git diff README.md*
- Show changes between branches: git diff <branch1> <branch2>
  - *git diff oldBranch newBranch*
- Show changes to the commit id: git show <commit id>
  - *git show c111244*
- Show a log of changes to the local repository’s HEAD: git reflog
  - *git reflog*

## Working with Remotes:
- Add a remote repository: git remote add <remote_name> <remote_url>
  - *git remote add origin https://github.com/raguri/git-blog.git*
- Push changes to a remote repository: git push <remote_name> <branch_name>
  - *git push origin feature*
- Pull changes from a remote repository: git pull <remote_name> <branch_name>
  - *git pull origin feature*

## Undoing Changes:
- Discard changes in a file: git checkout -- <file_name>
  - *git checkout -- README.md*
- Undo the last commit (keep changes): git revert HEAD
  - *git revert HEAD*
- Undo the last commit (discard changes): git reset HEAD~
  - *git reset HEAD~*

## Collaboration:
- Create a new branch from a remote branch: git checkout -b <local_branch_name> <remote_branch_name>
  - *git checkout -b featureBranch origin/master*
- Fetch the latest changes from a remote repository: git fetch
  - *git fetch origin*
- Resolve merge conflicts: Manually edit the conflicting files and commit the changes.
## Stashing Changes:
- Temporarily save changes for later: git stash
- Apply the most recent stash: git stash apply
- Apply a specific stash: git stash apply stash@{<stash_number>}
  - *git stash apply stash@{1}*
- List stashed changes: git stash list
- Clear all stashed changes: git stash clear

## Working with Tags:
- Create a tag: git tag <tag_name>
  - *git tag hotfix_tag*
- Push tags to a remote repository: git push –tags
- Checkout a specific tag: git checkout <tag_name>
    - *git checkout hotfix_tag*

## Interactive Rebasing:
- Reorder, squash, or edit commits interactively: git rebase -i <commit_id>
  - *git rebase -i c111244*
- Ignoring Files:
Specify files to ignore in a .gitignore file
- Ignore all files in a directory: /path/to/directory/*
- Ignore specific file types: *.txt, *.log, etc.

## Blaming and Annotating:
- Determine who last modified a specific line: git blame <file_name>
  - *git blame README.md*
- Annotate a file with commit information: git annotate <file_name> (Similar to blame)
  - *git annotate README.md*

## Git Bisect:
- Use binary search to find a specific commit that introduced a bug:
  - *git bisect start*
  - *git bisect good*
  - *git bisect bad*


Git is a prominent version control system with many additional features and commands. The above commands are intended to improve your workflow and productivity. I hope you find them helpful.

Happy working with Git..!! 🙂
