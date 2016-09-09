---
title: Git Cheat Sheet
date: 2016-09-06 22:42:15
tags: [Cheat Sheet, Git]
---

## Reset
### Reset HEAD
Add an new file, and doesn't add to stage yet, `git reset HEAD` won't change anything.

```powershell
PS D:\tmpDocs\git_study> git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        file 3.txt

nothing added to commit but untracked files present (use "git add" to track)
PS D:\tmpDocs\git_study> git reset HEAD
PS D:\tmpDocs\git_study> git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        file 3.txt

nothing added to commit but untracked files present (use "git add" to track)
```

If the file was added into stage, `git reset HEAD` will make the file to the `Untracked` status.

```powershell
PS D:\tmpDocs\git_study> git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   file 3.txt

PS D:\tmpDocs\git_study> git reset HEAD
PS D:\tmpDocs\git_study> git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        file 3.txt

nothing added to commit but untracked files present (use "git add" to track)
```

For the file which has been modified, if it hasn't been added to stage, `git reset HEAD` won't change anything. If it has been added to stage, this command will change the file to `unstage` status, but the changes won't be lost.

### Reset with hard argument
{% fa warning border pull-left 2x %}`--hard` argument will lead the uncommited **changes lost**, new files will become `untracked`. **BE CAREFUL!**

```powershell
PS D:\tmpDocs\git_study> git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   file 2.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        file 3.txt

PS D:\tmpDocs\git_study> git reset --hard HEAD
HEAD is now at e359baa add file 2
PS D:\tmpDocs\git_study> git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)

        file 3.txt

nothing added to commit but untracked files present (use "git add" to track)
```

### reflog
`reflog` command allows to check the commit history. 

```powershell
PS D:\tmpDocs\git_study> git log --graph --oneline
* 8ef5474 update file 2.txt
* e359baa add file 2
* 100819d add file 1
PS D:\tmpDocs\git_study> git reset HEAD^ # reset the HEAD to previous commit. HEAD^ points to the preivous commit.
Unstaged changes after reset:
M       file 2.txt
PS D:\tmpDocs\git_study> git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   file 2.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        file 3.txt

no changes added to commit (use "git add" and/or "git commit -a")
PS D:\tmpDocs\git_study> git reflog show master
e359baa master@{0}: reset: moving to HEAD^
8ef5474 master@{1}: commit: update file 2.txt
e359baa master@{2}: commit: add file 2
100819d master@{3}: commit (initial): add file 1
```

The `file 3.txt` also comes back, that because it was added to the stage.

What if used `reset --hard` command?
```powershell
```