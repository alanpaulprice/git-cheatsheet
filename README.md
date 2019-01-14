```
git init
```
initialise a git repository in the current directory

---
---
---
### staging
---

```
git status
```
view current state of project

---

```
git add <filename>
```
add file to staging area, ready for committing

---

```
git reset <filename>
```
unstage a file

---

```
git reset <commit id>
```
resets to a previous commit. if no argument is provided, the default behaviour is ```--mixed```, which will keep changes (unstaged). ```--soft``` will keep the changes (staged). ```--hard``` will revert all (tracked) files to their state at the specified commit.  

---

```
git add . && git reset --hard HEAD
```
reset repo to latest commit (also deletes any files that were created)

---

```
git rm <filename>
```
remove a specified file from disk and stage it's removal. ```-r``` (recursive) can be used to remove a folder. ```--cached``` will stage the file for removal but won't remove it from disk

---

```
git diff <commit>
```
display what is different between the current files and those of the specified commmit. if ```<commit>``` is omitted, the most recent commit will be used. specifying ```HEAD``` will show the result between the pulled changes and the current position. ```git diff --staged``` displays the current changes that are staged. pressing ```q``` will exit the results.

---

```
git clean -df
```
removes untracked files. ```-d``` also removes untracked directories. ```-f``` is required to make git delete files

---
---
---
### committing
---

```
git commit -m '<description-of-changes>'
```
store staged changes. ```-a``` will auto remove deleted files (it can be included adjacent to the ```-m```, as ```-am```)

---

```
git commit --amend
```
edit the last commit. if ```-m "<new message>"``` is passed, the message will be edited. if any changes are staged when ammending, they will be added to the last commit.

---

```
git log
```
view a list of previous commits. include ```--oneline``` to condense each item to a single line

---
---
---
### branches
---

```
git branch <branch-name>
```
create a new branch. if ```<branch-name>``` is omitted, a list of the current branches will be returned

---

```
git checkout <branch-name>
```
switch branches. including ```-b``` will create a new branch and switch to it

---

```
git merge <branch-name>
```
merge the changes made on the specified branch into the current branch. conflicts may occur, [vist here](https://git-scm.com/docs/git-merge#_how_conflicts_are_presented) to learn about dealing with them

---

```
git cherry-pick <commit id> 
```
copies a commit from a branch to the current branch

---

```
git branch -d <branch-name>
```
delete a branch. if the changes on the branch haven't been merged, ```-D``` (combines ```-d``` and ```-f```) will be required to delete it (overrides the safety feature)

---
---
---
### remote
---

```
git remote add origin <repo-url>
```
add a remote repository, allowing local changes to be pushed to github. naming the remote ```origin``` is standard practice

---

```
git push -u origin master
```
push local commits to the remote branch. ```-u``` stores the parameters (origin and master, in this case), allowing ```git push``` to be used from then on

---

check for changes to the remote repo and (if any exist) pull them down/update the local project
```
git pull origin master
```

---

```
git checkout -- <filename>
```
reset uncommitted changes to a specified file, since the last commit. ```--``` specifies that there are no more options after it, which avoids potential confusion between the names of branches and files

---
---
---
### misc
---
__note:__ ```<filename>``` can be replaced with ```.``` to refer all files or ```*.<file-extension>``` to refer to all files of a specified type

__The HEAD__ is a pointer that holds your position within all your different commits. By default HEAD points to your most recent commit, so it can be used as a quick way to reference that commit without having to look up the SHA.
### [git pro book](https://git-scm.com/book/en/v2)
