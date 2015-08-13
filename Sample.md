# I am using this repo as a test of syncing a local repo with a remote of the same name, without cloning the remote repo first.
## Steps involved are:
* create local project directory
* add some files, including this one
* start git bash
* navigate to the new project directory I just created
* run git init to create an empty local repo
*	This puts a .git file in the project folder...  this is now the new local repo for this project
* run git add . to put all files in the project folder into the staging area of the local repo for the first time.  All files are tracked now.
* run git commit to add all the files to the local repo
* run git remote add origin https://github.com/paramulator/another_test.git
* 	The above step just says I can refer to the remote repo as "origin".
* run git push

# Unfortunately, this last step fails because the local repo may have files that are different from what the remote repo has.  Git does not like this.

# So, here is what we need to do next in order to sync the repos.
* run git fetch origin 
*	this puts the files in the remote repo into the local repo
* run git diff HEAD to see what the differences are between local and remote repos.