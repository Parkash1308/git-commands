This repository serves as a comprehensive guide, featuring tutorials and examples, covering essential Git commands for efficient version control.

# Basic Questions

  Q 1) What is git ?
  Ans: Git is a distributed version control system that tracks changes in files, enabling collaboration, history management, and code development.
  
  Q 2) What is repository ?
  Ans : A repository is a digital storage location where files, documents, or code are stored, organized, and version-controlled for collaboration and management.
  
  Q 3) What is remote repository ?
  Ans: A remote repository is a cloud-based or external location where code is stored and shared among collaborators using version control systems like Git.
  
  Q 4) What is local repository ?
  Ans: A local repository is a storage location on a user's computer where version-controlled files and project history are maintained using a VCS like Git.
  
  Q 5) What is staging ?
  Ans: Staging is a preparatory step in version control, allowing users to select and organize files for the next commit, ensuring specific changes are tracked.

1) After installing the git base !
     
  The very first step is to config the email and user name
   1) git config --global user.email "parkash.official1308@gmail.com"
   2) git config --global user.name "Parkash1308"
      
  2) initializes a new Git repository in the current directory, allowing version control for files and tracking changes.
     command == >> git init
     
  4) git status shows the current state of the Git repository, displaying modified, untracked, and committed files, aiding in tracking changes.
     command == >> git status

  5) git add stages changes for the next commit. You can add files individually (git add filename) or a folder (git add foldername).
      For adding multiple files, you can:      
     1) Add All Modified Files:==>> git add -u
     2) Add All Files:         ==>> git add .
     3) Add Specific Files:    ==>> git add file1.txt file2.txt
        
  6) git commit records staged changes with a descriptive message, creating a new snapshot in the version history of the Git repository.
     git commit -m "descriptive message"
  7) connects a remote repository to local Git repository using a convenient alias.
     command == >> git remote add name url
  8) To set remote repository as up-stream branch for current local branch , it means that Git will remember the relationship between the local branch and the remote branch, making 
     future git push and git pull commands more convenient.
     command == >> git push --set-upstream name master
     
This was all about basic concept of git and commands !


============ Advance =============
1) Git command used to update your local repository with changes from a remote repository.
   command == >> git pull
   The general syntax for using git pull is:
   git pull <remote> <branch>
   This command contacts the remote repository and downloads any new changes (commits, branches, tags) from the remote repository to your local repository. It does not, 
   however, make any changes to your working directory or merge these changes into your current branch.
     command == >> git fetch:

  After fetching the changes, Git attempts to merge the changes from the remote branch into your current local branch, creating a new merge commit if necessary. If there are 
  conflicts between your local changes and the remote changes, Git will prompt you to resolve them.
   command == >> git merge

^^^^^^ Branch^^^^^^^^^
1) To create new branch use following command
   git checkout -b name_of_branch
3) git branch this command used to list the total branches
4) The git branch -v command is used to list all the branches in your Git repository along with additional information, including the latest commit on each branch. The -v flag stands       for "verbose" and provides more details about each branch. 
  git branch -v
It seems like you have several topics related to Git version control. I'll provide a brief overview of each of these topics:

Git Rebase:

1) Git rebase: is a command used to reorganize and clean up the commit history in a Git repository.
  It can be used to incorporate changes from one branch into another, making it appear as if you had made a linear sequence of commits.
  Rebase is often used to maintain a clean and linear commit history, especially before merging feature branches into the main branch.
  Recover Deleted Branch That Was Not Merged:

2) git reflog command: If a branch was deleted but not merged, you can potentially recover it using the git reflog command to find the SHA-1 hash of the commit at the tip of the deleted branch. Once you have the commit hash, you can recreate the branch using
 git branch <branch-name> <commit-hash>.

Reverting and Resetting:
  git revert is used to create a new commit that undoes the changes made in a previous commit, preserving the commit history.
  git reset is used to reset the current branch to a specific commit, which can be either "soft" (preserving changes in the staging 
  area), "mixed" (unstaging changes but preserving them in your working directory), or "hard" (discarding all changes).
3) Git Cherry-Pick:
  git cherry-pick allows you to apply a specific commit from one branch to another.
  It's useful when you want to pick and apply specific changes from one branch to another without merging the entire branch.
  Difference Between Fork, Branch, and Clone:

A fork is a copy of a repository on a Git hosting service like GitHub. It allows you to work on your copy of a repository independently of the original.
A branch is a separate line of development within a repository. You can create branches to work on new features or bug fixes.
A clone is a copy of a Git repository, including all of its history and branches. Cloning creates a local copy of a remote repository on your machine.
Squash the Last N Commits into a Single Commit:

You can use git rebase -i HEAD~N to interactively rebase the last N commits. During the interactive rebase, you can mark commits as "squash" or "fixup" to combine them into a single commit.
How to Avoid a Detached Head:

A detached head state occurs when you check out a specific commit instead of a branch. To avoid this, always make sure to check out a branch name instead of a commit hash. If you want to work on a specific commit, create a new branch at that commit using git checkout -b <branch-name> <commit-hash>.
These are the basic concepts related to your Git-related topics. If you have specific questions or need more detailed information about any of these topics, please feel free to ask.
     

