# Git Commands 
test

### General, quick commit and push
shell
$ git status // gives overview what is currently in the stage phase
$ git add . // puts all  not yet in the stage phase, in the stage phase
$ git commit -m "your line of text required"
$ git push // upload to your remote (github in our case)

### When you want to make specific commit on a topic
- You can select files one by one, with this command:
	shell
	$ git add pathtofile/tilesforhouse.txt
	
- And than you make the commit
	shell
	$ git commit -m "my specific commit on what I added in the commit"
	


### Git credentials
- Github: loginname: rluijk psw: 2746git4u

shell
git config --global user.name "rluijk"
git config --global user.password "2746git4u"


### End of Lines
shell
git config --global core.autocrlf true



### When you want to remove from stage
To remove a file from stage

shell
git restore --staged pathto/file.txt


### Clean commit with chunks of files
To be able to have a clean commit, sometimes you want to only submit parts of changes of a file. This can be done like this:

shell

git add -p pathto/file.txt


An interactive window that will show chunk after chunk that you either want or not want to include. 

after that you can do your commit in the shell, without adding a param. This will open the interactive window for commit subject and description. Leave empty line between the two to get it processed. It is interactive window that you can release and save with Esc, ":wq".

### Add file to your commit (if you see your forgot one or two)

Only do this when still local. When pushed, it is possible with some extra params, but things can get messy.

shell
git add pathtofile/tilesforhouse.txt
git commit --amend



This puts you in interactive mode allow for changing the subject and description of the commit aswell.

No need for editing? the extra --no-edit is at your disposel.

shell
git add pathtofile/tilesforhouse.txt
git commit --amend --no-edit



### What is that change in the file again, quickly!
shell
git diff pathtofile/tile.txt



### Untracked local folders & files
In case you get the "the following untracked working tree files"
You can run the following to remove them:

shell
git clean -fd


 
 After that a git pull should work again. (fetches files from remote and commits them in one go )

shell
git pull


## References: