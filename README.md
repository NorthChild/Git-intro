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
`` git mv `` and `` git rm `` or `` rm namefile.sd`` to delete from terminal and leave it in other repos
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


# Case Example #
- We are inside the folder of our repository, we just modified two files
  - we want to review what differences have been made to the files: `` git diff ``
  - we then want to add them to the stagign area: ``git add file1.html`` and then ``git add file2.html ``
  - we walk away for some coffe and we forget what we modified of the files, since the files are in staging area they cannot be viewed using `` git diff `` we need to instead use `` git diff --staged `` to see them past the modification stage
  - now we're ready to commit, remembering to add a message `` git commit -m "modified file1 and file2"
  - later that day you want to see what you did, cos again you forgot `` git log -p`` will show you what you accessed and modified


# Managing committed files #

- when in the directory `` git rm name.file ``, remember to commit the change ``git commit -m "deleted file" 
- to rename a file `` git mv [file.before] [file.now] `` where before is the og filename next to the new filename we chose, rememeber to commit the changes `` git commit -m "renamed file" ``
- to unstage a file that has been added to staging `` git reset HEAD file.name `` 
- its unstaged but we still made a mistake in the new addition to the script, and we want to cancel and revert to the older commited versions, so we type `` git checkout -- file.name `` the '--' char notifies git that we're presenting file names
- we can use the `` git checkout -- file.name `` method also to return a file that we `` rm file.name `` this will revert the change on the deletion of the file before it gets staged
- to access and revert a specific commit `` git log `` to find the specific SHA (first 5 chars) representing the commit you want to revert and then `` git revert 1a2b3 `` this will create a new commit `` git log `` to see the reverted and commited file, in a case where we're reverting a change that deleted a file inside the repo, this will bring the file back to the repo `` ls `` to check inside, to revert the most recent commit, first check `` git log `` then when sure `` git revert HEAD `` which reverts the latest file to be commited, in this case, since we're reverting the reversion of the deletion of the file, this time, it will delete the file again

# Cloning a repository #

- 
