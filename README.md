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


     

