# Working with local and remote repos.
## One way of working with a Github repo is to clone it to a local working directory and then periodically push changes back up to the remote.

## Alternative method if the local repo already happens to exist:  
* create local project directory
* add some files, etc., including this one
* start git bash
* navigate to the new project directory I just created
* run git init to create an empty local repo
*	This puts a .git file in the project folder...  this is now the new local repo for this project
* run git add . to initially put all files in the project folder into the staging area of the local repo for the first time.  All files are tracked now.
* run git commit to add all the files to the local repo
* run git remote add origin https://github.com/paramulator/another_test.git
* 	The above step just says I can refer to the remote repo as "origin" and my local repo now knows what the remote is called.
*	  Origin is not the only name I could have used.  Its just a label of my choice.
* run git pull origin master
*	This says pull in the master branch of the origin repo and merge with my current workspace.
*	In particular, if the remote repo has files not contained in the local depo, those will now be visible in the local.
*	At this point the local repo should have all local files we started with plus all stuff from the remote depo.
* update any of the local files per normal tasks...
* run git add -u to update the local staging area with all local changes you just made.
* run git commit to commit all of those changes to the local repository for this project
* run git push --set-upstream origin master to push the local repository changes out to the appropriate branch of the remote repo.
* inspect the remote repo and it should now look like the local project repo.
