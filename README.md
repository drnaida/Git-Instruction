# How to use Git
## Main statements
Git is a distributed version control system for tracking changes in source code during software development.

GitHub and GitLab are web-services for hosting projects and their cooperative developing, based on Git.

### Several places where your code may contain:
* **Working tree or untracked area** is the area where you are currently working. It's where your files are.
* **Index or the staging area** is where git starts tracking and saving changes that happen in your files. To place files in Index you have to write command "git add your-file.py your-file-2.py". If after adding files to the staging area you make changes in them, you will have to add them to the staging area again.
* **Local repository** is everything in your .git directory, the area which saves everything. To add elements from the staging area to local repository use 'git commit -m "" ' When you make commit, your staging area will become empty.
* **Remote repository** - remote copy of your repository. Can be stored on GitHub/GitLab or host it by yourself. To get the copy of your local repository to remote repository use "git push origin name-of-your-branch".

### Three states of Git files
1. **Untracked** - new file which wasn't added to be tracked by command "git add"
1. **Tracked**
    1. **Unmodified** - any file after "git commit".
    1. **Modified** - any file after it's been changed.
    1. **Staged** - any file after "git add".
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
1. git status (Shows the files in your Working Tree and the files in your Staging Area.)
1. git add (Adds files you mentioned to the staging area)
1. git commit -m "Name of your commit" (Adds files from the staging area to your Local Repository)
1. git push origin name-of-your-branch (Makes copy of your repository to the remote repository)
## Other Commands
* git log    (Let you see history of commits in the current branch. To finish view press "q")
* git diff   (Shows you unstaged changes, works if you didn't use git add)
* git rm name-of-the-file (Delete your file from working tree and index. For example, you had image in your directory and you decided to delete it. However, you can't just press button "Delete", you also have to use git rm)
* git commit --amend (Put changese in your last commit and ask for new commit name)
* git commit --amend -no-edit (Put chenges in your last commit without asking for a new commit name)
* git init (Makes new local repository)
## Commit requirements
