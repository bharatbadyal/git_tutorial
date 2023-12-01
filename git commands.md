1. `git init` -> Powers your folder to be managed by git, and initialises a new empty respository. It also creates a .git folder that has all the relevent logic to manage versions of your project.


new file cmd: touch <file> 
to see files in present folder/directory: ls


ls -a: to see files in directory

git status: 

2. `working area`: There can be a bunch of files that are not currently handled by git. It means that changes done or to be done on those files are not managed by git yet. A file which is in working area is considered to be not in the staging area. When we do `git status` and we see bunch of files `untracked files` then these are actually called to be in the working area.

3.`Staging area`: What all files are going to be part of the next version that we will create. This staging area is the place where git knows what changes will be done from the last version to the next version.

cmd:  git add <file> // moves files from working area to staging area.
      git rm --cached <file>	// to remove the file from staged area to working area or moves files back from staging area to working area.

4.`Repository Area`: This area actually contains the details of all your previous registered version. And the files in this area, git already manages them and knows their version history.

`commit` : Commit is a paticular version of the project. It capturess a snapshot of the projects staged changes and creates a version out of it.

cmd:  `git commit` : registers staging area to working area.

cmd:  `git log` : list downs all the commits of the respository. If you want to exit out of the git log promt press `q`. 

cmd: `git restore` : it removes all files changes from the staging area to be commited. This can be useful if we write some dirty piece if code and now no more want it. Instead of deleting every change line by line, we can restore it or we can say restore last clean version of the file.

cmd: `git restore --staged <file>` : it removes file from changes from staging area to the working area. This only works if changes are in your staging area.

12: Diff between git rm and git restore
ans: If you want to move the whole file back to the untracked state, then we do git rm, otherwise if we just want the changes to be moved in the working area or staged area then we use git restore.	

13. `git diff commit1 commit2` : gives the difference of all the file changes

14. `git commit -m "your message" ` -> If we want to avoid opening a text editor like vim/nano to add commit message we can use this following command

15. `git remote` : list down all the remote connection names

16. Remote connection : It helps you to link two git respositories for uploading and downloading changes from each other

17. `git remote add <name of remote> <link of the remote>` : this command helps us to add a new link to the remote

18. `git remote rm <name of remote>` : this command rename the remote connection

19. `git remote rename <oldname> <newname>` : this command renames the remote connection

Note: The name of the remote connection is always used to establish communication between the repos