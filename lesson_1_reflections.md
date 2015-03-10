# Udacity: How to Use Git and GitHub: Version Control for Code

***

## Compare two files
* At the command prompt:
	* Windows: **FC** - File Compare
		* `FC old_file.txt new_file.txt
	* Mac / Linux: **Diff** - Difference
		* diff -u old_file.xt new_file.txt
		* -u makes it a bit easier to read 
		* output
			* - means that line was in the old file and is not in the new file
			* + means that line is in the new file but not in the old file
	
### How did viewing a diff between two versions of a file help you see the 
bug that was introduced?

It made it super easy to spot a typo. That's pretty cool. 
This will be super awesome for comparing giant style sheets,
and other boring tasks.  

### How could having easy access to the entire history of a file make you a more efficient 
programmer in the long term?

Whenever there is a problem, it is easy to see the differences to a previous version,
and if needed, revert back to that version.
Keeping good track of changes also makes it easier to review the status of a project if you 
have been away from it for a while.
If collaborating, easy to see where the project has been and how it has been built over time.

## Manual Commits
* More useful than autosave
* Commits that are triggered manually are meaningful in some way
* `git log
	* command to log out all of the commits, with the most recent first 
	* message explains what changed since the last commit
	* ID is unique serial code to that commit
* `git diff <ID a> <ID b>
	* hitting enter shows changes
	* diffs are colorized
		* black = unchanged
		* red = removed
		* green = added

### What do you think are the pros and cons of manually choosing when to create a commit, 
like you do in Git, vs having versions automatically saved, like Google docs does?

Pros: Only stores logical milestones, so it is much easier to read the history. The granular 
revisions in google drive can be very hard to sort
through in an active document.
Cons: You have to remember to do it and some good changes could be lost. 

## Repositories

* multiple files committed at once are stored in a repository
* snapshot of every file in the repository (some files might be identical)
* `git log --stat
	* provides additional stats in the log about which files have changed in the commit
	* shows which files were affected in the commmit
		* green + signs indicate additions
		* red - signs indicate deletions
		* number of symbols is proportionate to the amount of stuff that changed

### Why do you think some version control systems, like Git, allow saving multiple files in one commit, 
while others, like Google Docs, treat each file separately?

That feature is critical to programming because of the interdependencies of the files in the repository. 
Text documents usually don't rely on each other's exact editing state to the same degree

## Cloning a repository

* Cloning copies a remote repository including all of its files and revision history to the local
envirotnment
* `git clone <url.git>
* to autocolorize:
	* `git conif --global color.ui auto

### How can you use the commands git log and git diff to view the history of files?

The log can be used to see the commit message, time and author for each commit. Adding
--stat to the log command will also show how many lines were added and how many were deleted
to get a quick overview of how much the file changed. By pulling the commit ideas, it is possible
to get a detailed view of the additions/deletions from the files. 
** Note - you can scroll back and forth in the log output until q is pressed **
** Pressing h provides a list of other commands available **

## git checkout

* checking out a commit reverts the files to what they were in that commit
* `git checkout <commit id>
* checking out an old commit results in the detached head warning - not a problem if you aren't making any changes
* running git log will show the current commit at the top, even though there are newer ones in the repository

### How might using version control make you more confident to make changes that could break something?

I'm already confident I can break things. But now, it is way easier to revert to previous version,
so there is no worry about breaking stuff. I would be able to just go backwards in commits
until there is a working version, then try again.

## Getting your git workspace setup
https://www.udacity.com/course/viewer#!/c-ud775/l-2980038599/m-3341718587

## General git bash command line tips I learned
* `cd .. 
	* there is a space after the cd - this is different than I remember dos or windows..
` cd ~
	* return to the home directory

### Now that you have your workspace set up, what do you want to try using Git for?

* tracking daily effort on github
* cloud repository for notes
	* this will also help me practice git
* showcasing projects I work on
* being able to see projects I work on
* being able to experiment with my code and not worry about breaking stuff
