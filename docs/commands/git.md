---
title: Git
---

# Git
## Basic
```bash
git init
```
create a new local repository
```bash
git clone <repo>
git clone user@host:<repo>
```
create a working copy of a repository

## Commit
```bash
git add <filename>
git add .
```
add files to staging

```bash
// commit changes to head (but not yet to remote repository)
git commit -m "message"

// commit files added with git add and also any files you have changed since then
git commit -a
```
commit changes

```bash
git push origin master
```
send changes to the master branch

```bash
git status
```
list files you've changed and those that are not added or committed

## Remote Repositories
```bash
// connect local repository with remote server
git remote add origin <server>

// list all currently configured remote repositories
git remote -v
```
dealing with remote servers

## Branch
```bash
// create a new branch
git checkout -b <branch>

// switch branches
git checkout <branch>

// list branches
git branch

// delete a branch
git branch -d <branch>

// push all branches to remote repository
git push -all origin
```
for branching purposes

```bash
// fetch and merge from remote server
git pull

// merge a branch into your branch
git merge <branch>

// view conflicts
git diff
git diff --base <file>
git diff <sourcebranch> <targetbranch>

// after resolving
git add
```
update from remote repository

```bash
# Create a fix to iss53
$ git checkout -b iss53
Switched to a new branch "iss53"
$ vim index.html
$ git commit -a -m 'added a new footer [issue 53]'

# oops, new urgent hotfix in production
$ git checkout master
Switched to branch 'master'
$ git checkout -b hotfix
Switched to a new branch 'hotfix'
$ vim index.html
$ git commit -a -m 'fixed the broken email address'
[hotfix 1fb7853] fixed the broken email address
 1 file changed, 2 insertions(+)

 # merge it
$ git checkout master
$ git merge hotfix
Updating f42c576..3a0874c
Fast-forward
 index.html | 2 ++
 1 file changed, 2 insertions(+)
$ git branch -d hotfix
Deleted branch hotfix (3a0874c).

 # return to that issue
$ git checkout iss53
Switched to branch "iss53"
$ vim index.html
$ git commit -a -m 'finished the new footer [issue 53]'
[iss53 ad82d7a] finished the new footer [issue 53]
1 file changed, 1 insertion(+)
$ git checkout master
Switched to branch 'master'
$ git merge iss53
Merge made by the 'recursive' strategy.
index.html |    1 +
1 file changed, 1 insertion(+)
$ git branch -d iss53
```
Sample scenario

# Tags

## Tags
```bash
git tag 1.0.0 <commitID>

// get commitID
git log

git push --tags origin
```
for tagging significant changesets like releases

## Revert
```bash
// replace changes in working tree with the last content in head
// changes added to index as well as new files will be kept
git checkout -- <filename>

// drop all local changes and commits, fetch latest history from server
// and point local master branch at it
git fetch origin
git reset --hard origin/master
```
revert changes

## Gitignore
```bash
git rm -r --cached filenames

or

git rm -r --cached .
git add .
git commit -m "fixing untracked files"
```
remove a previously tracked file(s) from git

## Search
```bash
git grep "foo()"
```
search the working directory for foo()