# Git-intro
intro to git commands 

# important commands
- set up new repositories:
`` git clone `` and `` git init ``  
- committing new version of a file:
`` git add ``, `` git status `` and `` git commit ``
- to show list of old commits:
`` git log ``
- move or remove files tracked by Git
`` git mv `` and `` git rm ``
- synchronise commits with git repositories
`` git push `` and `` git pull ``
- list all files as well as inivisible
`` ls -a ``

- committing should have a comment attached to it:
`` git commit -m "this commit does this yada yada yada"``
when committing we can add user name and email:
`` git config --global user.email "user@email.com" ``
`` git config --global user.name "userName" ``

- view what changes have been made, no only who committed
`` git log -p `` 
- to specifically view what has been modified 
`` git diff ``
- to view files that have been staged, and check for differences/changes in the code
`` git diff --staged ``


- Case example: we are inside the folder of our repository, we just modified two files
  - we want to review what differences have been made to the files: `` git diff ``
  - we then want to add them to the stagign area: ``git add file1.html`` and then ``git add file2.html ``
  - we walk away for some coffe and we forget what we modified of the files, since the files are in staging area they cannot be viewed using `` git diff `` we need to instead use `` git diff --staged `` to see them past the modification stage
  - now we're ready to commit, remembering to add a message `` git commit -m "modified file1 and file2"
