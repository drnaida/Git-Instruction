# How to use Git
## Main statements
Git is a distributed version control system for tracking changes in source code during software development.

GitHub and GitLab are web-services for hosting projects and their cooperative developing, based on Git.

Several places where your code may contain:
* Working tree
* Local repository
* Remote repository
* Index
## How to start your work in the repository which has already been created:
1. Open repository
    1. Find button "Clone or download" in GitHub or "Clone" in GitLab
    1. Copy URL under the heading "Clone with HTTPS"
1. Open Git Bash on your desktop
    1. Open your local directory. For instance: "cd /d/dev/my-project"
    1. Do "git clone link-you-copied-under-clone-with-HTTPS
## Branches
### Small note about branches
### How to create new branch
There two ways of doing it:
* git branch name-of-your-branch    (Creates new branch, but doesn't switch you to it. You have to do "git checkout name-of-your-branch" if you want to continue working in just created branch)
* git checkout -b name-of-your-branch (Creates new branch and switches you to it)
### How to see your local branches
* git branch
### How to switch between branches
* git checkout name-of-the-branch
### Error "fatal: The current branch my-branch has no upstream branch"
It happens when you created new local branch and wanted to push it on server, but there is no such a branch in your remote repository.

## Pushing your code to GitHub/GitLab repository
Don't forget that you should have worked in a different branch (not master).
1. git status 
1. git add 
1. git commit -m "Name of your commit"
1. git push origin name-of-your-branch
## Other Commands
* git log    (Let you see history of commits in the current branch. To finish view press "q")
* git diff   (Shows you unstaged changes)
* git rm name-of-the-file (Delete your file from working tree and index. For example, you had image in your directory and you decided to delete it. However, you can't just press button "Delete", you also have to use git rm)
* git commit --amend (Put changese in your last commit and ask for new commit name)
* git commit --amend -no-edit (Put chenges in your last commit without asking for a new commit name)
* git init (Makes new local repository)
## Commit requirements
