Lesson 17: Discover Git Repository
*moving to previous folder
	cd ..
*removing from folder from version control
	rm -rf .git
	
Lesson 18: Starting with an Existing Project(git init)
	git init .
.(dot) symbol initializes the current folder

Lesson 19: Going deeper with commits and messages
	git add .
to add all existing files on version control .(dot)
	git commit
to commit files and add message through notepad text editor since notepad is default text editor

Lesson 20: Commit log and showing details
	git log
to show log details including id 
	ie commit 1d0b034dd715900f1dec670a71915333ce52f74b
author and date
Author: IP Ejercito <ip.ejercito@yahoo.com>
Date:   Tue Nov 22 16:58:11 2016 +0800
	git show
to show all logs from the beginning

Lesson 21: Combining steps with express commits
	git ls-files
to check on current tracked files
	touch (file to add)
to add file on current folder
	rm (file to delete)
to delete a file
	git -am "commit message"
combination of git add and git commit with message

Lesson 22: Backing Out Changes in Stage and the Working Directory
	git reset HEAD (file to unstage)
removing the changes you made on staging or unstaging the changes you did on current file
	git checkout -- (file to unstage)
totally removing the changes you made in a file and will revert to clean branch

Lesson 23: Git History and Creating Custom Git Commands with Aliases
	git --oneline --graph --decorate --all
--oneline
	provides simplified commit entry, providing a lot of information in single line
--graph
	provides asterisk based graph denoting branching heirarchy
--decorate
	which commits are apart of which branch and other labels of reposity
--all
	provide the history of all branch
	
	 git config --global alias.hist "log --oneline --graph --decorate --all"
provides a shortened alias for git log for this one its "hist"
you can check it by typing "git config --global --list" to list all configuration info including our newly created alias. now you can just type git hist to retrieve your log info