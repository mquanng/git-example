## Git Hidden folder
`.git` tells you our project is git repo

Want to create git repo in new project, create folder and initialize repo using `git init`
```
mkdir /workspace/tmp/new-project
cd /workspace/tmp/new-project
git init
touch Readme.md
code Readme.md
git add .
# make changes readme
git commit -m "add readme file"
```

## Cloning
In 3 ways (HHTPS, SSH, GitHub CLI)

Use Codespaces so create tmp directory in workspace

```sh
mkdir /workspace/temp
cd /workspace/temp
```

## HTTPS
```sh
git clone https://github.com/quannhm/git-example.git
cd git-example
```

>You will need generate Personal Access Token (PAT)
https://github.com/settings/tokens

Use token as password when logging in

- Give it access to Contents for Commits

## SSH
```ssh
git clone git@github.com:quannhm/git-example.git
cd git-example
```

We need create SSH ras key pair
```sh
sshe-keygen -t rsa
```

For WSL users and if you create non default key, add
```sh
eval `ssh-agent`
ssh-add /home/andrew/.ssh/alt-github_id_rsa
```

Test connection
```
ssh -T git@github.com
```

## SSH
They instruct in Ubuntu so I skip this

```
gh auth login
gh repo clone mquanng/git-example
```

## Commits
Commit code which will open edit msg the editor of choice
```sh
git commit
```

```
git config --global core.editor emacs
```

Make commit with msg without opening editor
```sh
git commit -m "add this"
```

## Branches
List branches
```
git branch
```

Create new by
```
git branch name
```

Checkout branch
```
git checkout name
```

## Remotes
We can add remote usually via upstream when add branch

```sh
git remote add ...
git branch -u origin new-feature
```

## Stashing
Want to hold on/hide changes until you come back
```
# Hide
git stash
git stash save my-name

# Show
git stash list

# Load
git stash apply
git stash pop
```

## Merging
change to your new branch then merge
```
git checkout dev
git merge main
```

## Add
Stage change what included when commit, use . to add all
```
git add Readme.md
git add .
```

## Reset
Reset allow set Staged to Unstaged
```
git add.
git reset
```

## Status
Show file commited or not
```
git status
```

## Git config file
Store global config such as email, name,...
```
git config --list
```

## Log
Git log show recent git commits to the git tree
```
git log
```

## Push
Push repo to remote
```
git push
```