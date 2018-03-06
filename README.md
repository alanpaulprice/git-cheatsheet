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
add all files of same type to staging area
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
store staged changes
```
git commit -m "<description-of-changes>"
```
view a list of previous commits. include ```--oneline``` to condense each item to a single line
```
git log
```
adds a remote repository, allowing changes to be pushed to github. naming the remote ```origin``` is standard practice
```
git remote add origin <repo-url>
```
pushes local commits to the remote branch. ```-u``` stores the parameters (origin and master), allowing ```git push``` to be used from then on
```
git push -u origin master
```
