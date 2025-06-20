# Git Workflow For Open Source

## Setting up in your local machine for the first time

```bash
# fork
git clone https
git remote upstream <main repo github link>
```

## Working on new issue

```bash
git pull upstream main
git checkout -b "fix/name"
# fix the code
```

### If not sync

```bash
git switch main
git pull upstream main    # you can only pull if your current code is committed
git push origin main
git switch fix/name
git merge origin main
# handle merge conflict
git push
# make a pull request
```

## Goes out of sync after pull request is made

```bash
git switch main
git pull upstream main     # you can only pull if your current code is committed
git push origin main
git switch fix/name
git merge origin main
# resolve the conflict
git add .
git rebase --continue
# give commit message, ctrl+c
:wq
git push -f    # -f only if pull request is open
```

## After pull request accept

```bash
git branch -d fix/name
git pull upstream main
```
