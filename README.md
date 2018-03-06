initialise a git repository in the current directory
```
git init
```
view current state of project
```
git status
```
add file to staging area, ready for commiting
```
git add <filename>
```
add all files of a type to staging area
```
git add '*.<file-extension>'
```
add all new/edited files to staging area
```
git add .
```
remove a file from the staging area
```
git rm --cached <filename>
```
store staged changes. ```-a``` will auto remove deleted files. it can be added adjacent to the ```-m```, as ```-am```
```
git commit -m "<description-of-changes>"
```
view a list of previous commits. include ```--oneline``` to condense each item to a single line
```
git log
```
add a remote repository, allowing changes to be pushed to github. naming the remote ```origin``` is standard practice
```
git remote add origin <repo-url>
```
push local commits to the remote branch. ```-u``` stores the parameters (origin and master), allowing ```git push``` to be used from then on
```
git push -u origin master
```
check for changes to the remote repo and (if any exist) pulls them down/updates the local project
```
git pull origin master
```
display what is different from the specified commmit. if ```<commit>``` is omitted, the differences from the last commit will be displayed. pressing ```q``` will exit the results. specifying ```HEAD``` will show the result between the pulled changes and the current position. ```git diff --staged``` displays the current changes that are staged
```
git diff <commit>
```
unstage a file
```
git reset <filename>
```
reset all changes to the specified file, since the last commit. ```--``` specifies that there are no more options after it. avoids potential confusion between branches and files
```
git checkout -- <filename>
```
create a new branch. if the ```<branch-name>``` is omitted, the current existing branches will be listed
```
git branch <branch-name>
```
switch branches. including ```-b``` will create a new branch and switch to it simulatenously.
```
git checkout <branch-name>
```
removes specified file from disk and stages their removal. ```<*.<file-extension>``` can be used to remove all files of a type. ```-r``` (recursive) can be used to remove a folder
```
git rm <filename>
```
___

### HEAD
The HEAD is a pointer that holds your position within all your different commits. By default HEAD points to your most recent commit, so it can be used as a quick way to reference that commit without having to look up the SHA.
