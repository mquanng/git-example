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

## Remotes

## Stashing

## Merging

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