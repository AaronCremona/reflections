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

How can you use the staging area to make sure you have one commit per logical
change?

What are some situations when branches would be helpful in keeping your history
organized? How would branches help?

How do the diagrams help you visualize the branch structure?

What is the result of merging two branches together? Why do we represent it in
the diagram the way we do?

What are the pros and cons of Gits automatic merging vs. always doing merges
manually?