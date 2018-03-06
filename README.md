initialise a git repository in the current directory
```
git init
```
view current state of project
```
git status
```
add file to staging area, ready for committing
```
git add <filename>
```
store staged changes. ```-a``` will auto remove deleted files (it can be included adjacent to the ```-m```, as ```-am```)
```
git commit -m "<description-of-changes>"
```
view a list of previous commits. include ```--oneline``` to condense each item to a single line
```
git log
```
add a remote repository, allowing local changes to be pushed to github. naming the remote ```origin``` is standard practice
```
git remote add origin <repo-url>
```
push local commits to the remote branch. ```-u``` stores the parameters (origin and master, in this case), allowing ```git push``` to be used from then on
```
git push -u origin master
```
check for changes to the remote repo and (if any exist) pull them down/update the local project
```
git pull origin master
```
display what is different between the current files and those of the specified commmit. if ```<commit>``` is omitted, the last commit will be used. specifying ```HEAD``` will show the result between the pulled changes and the current position. ```git diff --staged``` displays the current changes that are staged. pressing ```q``` will exit the results.
```
git diff <commit>
```
unstage a file
```
git reset <filename>
```
stage a file for removal
```
git rm --cached <filename>
```
reset uncommitted changes to a specified file, since the last commit. ```--``` specifies that there are no more options after it, which avoids potential confusion between the names of branches and files
```
git checkout -- <filename>
```
create a new branch. if ```<branch-name>``` is omitted, a list of the current branches will be returned
```
git branch <branch-name>
```
switch branches. including ```-b``` will create a new branch and switch to it
```
git checkout <branch-name>
```
remove a specified file from disk and stage it's removal. ```-r``` (recursive) can be used to remove a folder
```
git rm <filename>
```
merge the changes made on the specified branch into the current branch. conflicts may occur, [vist here](https://git-scm.com/docs/git-merge#_how_conflicts_are_presented) to learn about dealing with them
```
git merge <branch-name>
```
delete a branch. if the changes on the branch haven't been merged, ```-D``` (combines ```-d``` and ```-f```) will be required to delete it (overrides the safety feature)
```
git branch -d <branch-name>
```
___

__note:__ ```<filename>``` can be replaced with ```.``` to refer all files or ```*.<file-extension>``` to refer to all files of a specified type

__The HEAD__ is a pointer that holds your position within all your different commits. By default HEAD points to your most recent commit, so it can be used as a quick way to reference that commit without having to look up the SHA.
### [GIT PRO BOOK](https://git-scm.com/book/en/v2)
