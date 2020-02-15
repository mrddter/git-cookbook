# Git Commands

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
