# Git Commands in Action
-    Navigating Your Repository with Confidence.

## Mission Brief
The mission is to learn the ropes of Git by completing commands covered in this tutorial:

git clone, git config, git add, git status, git commit, git push, git pull, git branch, git checkout, and git merge

### 1. Branch Management:
- Create a new branch: git branch <branch_name>
  - git branch git_blog
  - git checkout -b git_blog
- Switch to a branch: git checkout <branch_name>
  - git checkout git_blog
- Rename a branch: git branch -m <new_branch_name>
  - git branch -m git_commands_in_action (It will rename the current branch)
  - git branch -m git_blog git_commands_in_action (It will rename the old_branch to new_branch as mentioned in the command)
- Delete a branch: git branch -d <branch_name>
    - git branch -d git_blog
    - git branch -D git_blog (Force delete)

