# Git Commands

## Align specific branch with master

```git
git pull origin master
```

## Reset all changes

```git
git fetch origin
git reset --hard origin/master
git clean -fdx
git pull
```

## Reset to specific commit

```git
git reset --hard <commit>
git push -f
```

## Reset last commit without change files (if no push is made)

```git
git reset --soft HEAD~1
```

## Reset last commit and reset all changes (be carefull)

```git
git reset --hard HEAD~1
```

## Delete local and remote branch

```git
git branch -a
git branch -D <remote> <branch>
git push <remote> --delete <branch>
```

## Cleanup all history commits

```git
git checkout --orphan latest_branch
git add -A
git commit -am "shrink commits"
git branch -D master
git branch -m master
git push -f origin master
```

chained all in one command

```git
git checkout --orphan latest_branch && git add -A && git commit -am "shrink commits" && git branch -D master && git branch -m master && git push -f origin master
```

## Add new repo to existing folder

```git
git init
git add .
git commit -m "first release"
git remote add origin https://github.com/mrddter/new_repository
git push -u origin master
(optional) git push -f origin master
```

## Change git user

```git
git config --list
git config user.email my@email.com
git config user.name "myname"
```

## Change git user (globally)

```git
git config --list
git config --global user.email my@email.com
git config --global user.name "myname"
```
