#### Working with local and remote repos.

***

##### One way of working with a Github repo is to simply clone it to a local working directory and then periodically push changes back up to the remote.

***

##### Here is an alternative method if the local repo already happens to exist:  
* Create a local project directory
* Add some files to, etc., including this one
* Start git bash
* Navigate to the new project directory just created
* Run `git init` to create an empty local repo
*	This puts a .git file in the project folder...  this is now the new local repo for this project
* Run `git add` . to initially put all files in the new project folder into the staging area of the local repo for the first time.
    + All files are tracked now.
    + Or, run `git add <file name>` to begin tracking specific files instead of everything.
* Run `git commit` to add all the tracked files to the local repo.
* Run `git remote add origin https://github.com/paramulator/Git-Tips.git` ... just make sure to use the correct remote repo.
* 	+ The above step just says I can refer to the remote repo as "origin" and my local repo now knows what the remote is called.
    + "Origin" is not the only name I could have used.  Its just a label of my choice.
* Run `git pull origin master`
    + This says pull in the master branch of the origin repo and merge with my current workspace.
    + In particular, if the remote repo has files not contained in the local depo, those will now be visible in the local.
    + At this point the local repo should have all local files we started with plus all stuff from the remote depo.
* Update any of the local files per normal tasks...
* Run `git add -u` to update the local staging area with all local changes you just made.
    + Or, `git add <specific file names>` is you don't want to stage everything.
* Run `git commit` to commit all of those changes to the local repository for this project
* run `git push --set-upstream origin master` to push the local repository changes out to the appropriate branch of the remote repo.
    + Not sure if the `--set-upstream origin master` option needs to be specified every time.  
* Inspect the remote repo and it should now look like the local project repo.
