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
