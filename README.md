# Git Commands

## Align specific branch with main

```git
git pull origin main
```

## Reset all changes

```git
git fetch origin
git reset --hard origin/main
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
git commit -am "clean up"
git branch -D main
git branch -m main
git push -f origin main
```

chained all in one command

```git
git checkout --orphan latest_branch && git add -A && git commit -am "shrink commits" && git branch -D main && git branch -m main && git push -f origin main
```

## Add new repo to existing folder

```git
git init
git add .
git commit -m "first release"
git remote add origin git@github.com:mrddter/new_repository.git
git push -u origin main
(optional) git push -f origin main
```

## Change remote url

```git
git remote set-url origin git@github.com:mrddter/new_repository.git
```

Verify that the remote URL has changed:

```git
git remote -v
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

## Merge two branches

```git
git checkout <to-branch>
git merge <from-branch>
```
