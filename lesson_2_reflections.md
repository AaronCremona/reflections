# Udacity: How to Use Git and GitHub: Version Control for Code - Lesson 2

***


## Git init

* `git init
	* creates a new repository in the current directory

### What happens when you initialize a repository? Why do you need to do it?

Git creates a new hidden .git directory that stores all the meta data
for the repository and adds a list of untracked files to the status. 
This is the first step to do everything else if you want to make a 
new repository (instead of cloning an existing one from somewhere)

## Git add and the staging area

* `git add <filename>
	* adds a file to the staging area
* the staging area is where one or more files are bundled together before a commit 

### How is the staging area different from the working directory and the repository?
What value do you think it offers?

The staging area is an area where modified files are assigned to the next commit. It 
is different from the working directory, because there might a whole bunch of files
in the working directory that you don't want to commit. It's value is that it
gives the user control over what gets added to an individual commit. 

## Git commit

* `git commit
	* opens up a commit message editor in the default editor. 
	* It's standard to write the commit messages like they
	are a command
	* save the file, quit the editor
	* in vim:
		* press i to begin editing (insert)
		* press escape then :wq to save, exit, and commit
		* escape then :q to quit without commiting

* `git diff
	* when git diff is run using commit id's, it shows the difference between
	the commits
	* when git diff is run without commit id's, it will compare the staging area 
	to the working directory

* `git diff --staged 
	* shows the difference between the files in the staging area, and the most recent commit. 

* `git reset --hard
	* discards any changes in the staging area AND the working directory
	* be very careful using this - most changes in git are reversable, but this isn't

* `git checkout master
	* if you are in an older commit (i.e. a detached head), this will bring you back to the 
	most recent commit

###How can you use the staging area to make sure you have one commit per logical
change?

Even if more than one thing is changed, all you have to do is stage them by one 
logical grouping at a time and commit. Git status can be used to verify everything
you want is in there before committing.

## Branches

* git allows you to create labels for commits - these are called branches
* the main branch is called master 
	* every time you create a repository, git automatically creates a master branch
* when we weren't on the main commit, we got a detached head error
	* basically a warning that you aren't on the master branch
* possible to checkout a branch, just like you would a commit
* if you make an updated commit, the label moves to the new commit
* it's possible to add multiple labels to the same commit, but the label only advances 
for the checked out commit
* `git branch
	* with no argument, it shows the current branch name
* `git branch new-branch-name
	* creates a new branch with the new branch name
	* when `git branch is run again, it shows both branch names, with a * by the currently 
	checked out branch
* `git checkout new-branch-name
	* checkout the new branch
	* at the firt checkout, it has the same files as the master

### What are some situations when branches would be helpful in keeping your history
organized? How would branches help?

Branches would be useful any time there is a need to create multiple versions that need to exist side 
by side. Examples are an experimental change, developing a new feature while keeping the working version 
intact, developing two distinct versions. Answers from the udacity branch. "Context switching." A new 
branch is made for any new activity. The master is the production quality branch, and he makes 
a new branch for any other activity. Fixing a bug, making a new feature, etc. 

How do the diagrams help you visualize the branch structure?

What is the result of merging two branches together? Why do we represent it in
the diagram the way we do?

What are the pros and cons of Gits automatic merging vs. always doing merges
manually?