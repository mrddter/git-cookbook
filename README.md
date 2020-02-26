# Git Commands

## Align specific branch with master

```
git pull origin master
```

## Reset all changes

```
git fetch origin
git reset --hard origin/master
git clean -fdx
git pull
```

## Reset to specific commit

```
git reset --hard <commit>
git push -f
```

## Reset last commit without change files (if no push is made)

```
git reset --soft HEAD~1
```

## Reset last commit and reset all changes (be carefull)

```
git reset --hard HEAD~1
```

## Delete local and remote branch

```
git branch -a
git branch -D <remote> <branch>
git push <remote> --delete <branch>
```

## Cleanup all history commits

```
git checkout --orphan latest_branch
git add -A
git commit -am "cleanup history commits"
git branch -D master
git branch -m master
git push -f origin master
```
