---
title: Git
---

# Git
## Basic
```js
git init
```
create a new local repository
```js
git clone <repo>
git clone user@host:<repo>
```
create a working copy of a repository

## Commit
```js
git add <filename>
git add .
```
add files to staging

```js
// commit changes to head (but not yet to remote repository)
git commit -m "message"

// commit files added with git add and also any files you have changed since then
git commit -a
```
commit changes

```js
git push origin master
```
send changes to the master branch

```js
git status
```
list files you've changed and those that are not added or committed

## Remote Repositories
```js
// connect local repository with remote server
git remote add origin <server>

// list all currently configured remote repositories
git remote -v
```
dealing with remote servers

## Branch
```js
// create a new branch
git checkout -b <branch>

// switch branches
git checkout <branch>

// list branches
git branch

// push all branches to remote repository
git push -all origin

// delete a branch
git push origin :<branch>
```
for branching purposes

```js
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

# Tags

## Tags
```js
git tag 1.0.0 <commitID>

// get commitID
git log

git push --tags origin
```
for tagging significant changesets like releases

## Revert
```js
// replace changes in working tree with the last content in head
// changes added to index as well as new files will be kept
git checkout -- <filename>

// drop all local changes and commits, fetch latest history from server
// and point local master branch at it
git fetch origin
git reset --hard origin/master
```
revert changes

## Search
```js
git grep "foo()"
```
search the working directory for foo()