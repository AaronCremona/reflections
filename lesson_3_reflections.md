# Lesson 3 - Github

## Setting up the remote repository
* Create the respoitory on github using the web interface
	* You can't clone to github or push a new project before a 
	repository is made
* The remote command is used to add remotes
	* `git remote
		* with no argument, the command shows remote repositories that are already setup
	* `git remote add name url
		* name is the name used in the repository to refer to the remote
		* if there is only one remote, it's standard to name it origin
			* eg `git add remote origin https://github.com/AaronCremona/reflections.git
* to get detailed information about the remote repositories
	* `git remote -v
		* v stands for verbose
		* it shows both the fetch and push remotes
* to copy commits to the remote, use git push
	* git push takes two arguments: the remote you are sending changes to, the name of the branch to push
	* e.g.
		* `git push origin master
		* by default, the branch on github will have the same branch name that is pushed


###When would you want to use a remote repository rather than keeping all your work local?

Anytime you want a back up, to publish it to showcase it to others or allow them to collobarate, or to work on multiple computers.

* to get updates from the remote repo to the local repo, use pull
	* `git pull origin master

###Why might you want to always pull changes manually rather than having Git automatically stay up-to-date with your remote repository?

You might not want to publish the changes to the world. You might want to go back several commits and effectively delete them.
You might decide to branch off the master with what you are doing. I don't know what else, but prob lots of shady stuff.

###Describe the differences between forks, clones, and branches. When would you use one instead of another?

Forks only apply to github. It is the same thing as cloning, except it happens on the github servers. A copy of an existing repository is made to your github account. You use this if you want to copy somebody's github repository to work on it yourself and make your own version of it. Cloning is git speak for making a copy. You can clone locally to create a completely new copy, or you can clone from a remote repository (like github) to make a new local copy. Branching is when, in your own repository, you want to go down a distinct path from what was going on,
like a new feature or separate concept, while leaving the main working version intact. 