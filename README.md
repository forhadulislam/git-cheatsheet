## Git Cheatsheet

Most important and frequently used Git commands for daily life of a developer who uses Git.

### SETUP

Configuring user information used across all local repositories

        git config --global user.name “[firstname lastname]”
set a name that is identifiable for credit when review version history

        git config --global user.email “[valid-email]”
set an email address that will be associated with each history marker        

        git config --global color.ui auto        
set automatic command line coloring for Git for easy reviewing


### SETUP & INIT
	
Configuring user information, initializing and cloning repositories
	
	git init
initialize an existing directory as a Git repository


	git clone [url]
retrieve an entire repository from a hosted location via URL


### STAGE & SNAPSHOT

Working with snapshots and the Git staging area	
	
	git status
show modified files in working directory, staged for your next commit


	git add [file]
add a file as it looks now to your next commit (stage)


	git reset [file]
unstage a file while retaining the changes in working directory

	git diff
diff of what is changed but not staged

	git diff --staged
diff of what is staged but not yet commited

	git commit -m “[descriptive message]”
commit your staged content as a new commit snapshot




### BRANCH & MERGE

Isolating work in branches, changing context, and integrating changes

	git branch
list your branches. a * will appear next to the currently active branch

	git branch [branch-name]
create a new branch at the current commit

	git checkout
switch to another branch and check it out into your working directory

	git merge [branch]
merge the specified branch’s history into the current one

	git log
show all commits in the current branch’s history


### INSPECT & COMPARE

Examining logs, diffs and object information

	git log
show the commit history for the currently active branch

	git log branchB..branchA
show the commits on branchA that are not on branchB

	git log --follow [file]
show the commits that changed file, even across renames

	git diff branchB...branchA
show the diff of what is in branchA that is not in branchB

	git show [SHA]
show any object in Git in human-readable format


### Reset 

    git fetch --all  
    git reset --hard origin/master
