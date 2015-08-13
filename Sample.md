# I am using this repo as a test of syncing a local repo with a remote of the same name, without cloning the remote repo first.
## Steps involved are:
* create local project directory
* add some files, etc., including this one
* start git bash
* navigate to the new project directory I just created
* run git init to create an empty local repo
*	This puts a .git file in the project folder...  this is now the new local repo for this project
* run git add . to put all files in the project folder into the staging area of the local repo for the first time.  All files are tracked now.
* run git commit to add all the files to the local repo
* run git remote add origin https://github.com/paramulator/another_test.git
* 	The above step just says I can refer to the remote repo as "origin".
* run git pull origin master
*	This says pull in the master branch of the origin repo and merge with the current workspace.
*	At this point the local repo should have all local files we started with plus all stuff from the remote depo.
* update any of the loacl files
* run git add -u to update the staging area
* run git commit to update the local repository with all local changes
* run git push to push the local repository changes out to the remote.
* inspect the remote and it should now look like local.
