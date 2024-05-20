# Git Commands Cheat Sheet

## Initialize
```bash
git init
git status
git add .
git commit -m ''
git status -s
git clean -f -d ---.--- # namefile
git rm --cached ---.--- # namefile
git commit -am ''
git commit -m "change file - resolve #1"
git commit --amend
git show # Shows the details of the last commit
git show 1234567 # The first seven digits of the IDs that were committed
git show 1234567 -- ---.--- # Shows the changes of the desired file in one commit & namefile
 ```


## Log
```bash
git log
git log --oneline
git log --stat
git log --graph
git log --graph --oneline
git log --graph --oneline --all
git log --graph --oneline --stat
git log --oneline --stat
git log --graph --stat
git log --after="y/m/d"
git log --before="y/m/d"
git log --author="name author"
```
## Config
```bash
git config --local alias.lgo "log --oneline"
git config --local alias.cam "commit -am"
git config --global alias.--- "------"

```
## Branch
```bash
git branch
git branch name
git switch name
git switch -c name
git branch -d name
git branch -m namebranch
git merge namebranch

```
## Diff
```bash
git diff
git diff --staged
git diff HEAD or head
git diff 00000000..00000000 # The first eight digits of the commit id
git diff 00000000..00000000 ---.--- # The first eight digits of the commit id & namefile
git diff -----..----- # namebranch

```
## Checkout
```bash
git checkout 00000000 # The first eight digits of the commit id
git checkout 00000000 ---.--- # The first eight digits of the commit id & namefile
git checkout head ---.--- # namefile
git checkout head .

```
## Restore
```bash
git restore --staged
git restore --staged ---.--- # namefile
git restore ---.--- # namefile
git restore --source 00000000 ---.--- # The first eight digits of the commit id & namefile
git restore --source head ---.--- # The first eight digits of the commit id & namefile

```
## Reset
```bash
git reset --hard 00000000 # The first eight digits of the commit id
git reset --mixed 00000000 # The first eight digits of the commit id
git reset --soft 00000000 # The first eight digits of the commit id

```
## Revert
```bash
git revert 00000000 # The first eight digits of the commit id

```
## Clone
```bash
git clone https://github.com/askari86/main.git # http clone github

```
## Remote 
```bash
git remote add origin https://github.com/askari86/main.git # http clone github
git remote -v
git remote remove nameremote

```
## Push
```bash
git push origin master

```
## Pull
```bash
git pull origin master

```
## Fetch
```bash
git fetch nameremote namebranch
git branch -r
git switch -c namebranch nameremote/namebranch

```
## Stash
```bash
git stash
git stash save "message"
git stash list
git stash pop
git stash apply
git stash show
git stash show -p stash@{0}
git stash drop stash@{0}
git stash clear

```
## Blame
```bash
git blame ---.--- # namefile
git blame ---.--- -L 1,5 # namefile & line code

```
## Bisect
```bash
git bisect start
git bisect good 00000000 # The first eight digits of the commit id
git bisect bad
git bisect reset

```
## Tag
```bash
git tag V1.0.0 00000000 # The first eight digits of the commit id
git tag -f V1.0.0 00000000 # The first eight digits of the commit id
git tag
git tag -l
git tag -l 'V1.8.*'
git show tagname
git checkout tagname
git diff tagname
git push origin tagname
git push origin --tag

```
## Rebase
```bash
git rebase namebranch

```