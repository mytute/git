## GIT TUTORIAL


to set git global setup 
```bash

git config --global user.name "Samadhi Laksahan"
git config --global user.email "samadhivkcom@gmail.com"

```

to get all information related to repository.
```bash

$ git config -l
$ git config --list

```


to Push an existing code to new remote repo
```bash

$ cd existing_folder
$ git init --initial-branch=main
$ git remote add origin git@gitlab.com:electroseela/kcorporate.git
$ git add .
$ git commit -m "Initial commit"
$ git push -u origin main

```

to create new branch.
```bash

$ git branch <branch name>

```

to see all branches
```bash

$ git branch -a

```

to delete branch.
```bash

$ git branch -D <branch name>

```

to create branch and checkout (shortcut).
```bash

$ git checkout -b  <branch name>

```

to make Merging from branch
go to branch that you want get merge (eg: checkout to master branch)
```bash

$ git merge <branch name>

```

to push new created branch on github
```bash

$ git push <created repo github url> <branch name>

```

to add remote repo url to git
```bash

$ git remote add  origin <created repo github url> 

```

to see remote repo location 
```bash

$ git remote -v
or 
$ git config --get remote.origin.url

```

to update your local repository
```bash

$ git pull origin <branch name>

```

to create a tag (for specific version)
```bash

$ git tag -a <tag name eg: v1.0> -m "<your commet>"

```

to view created tags
```bash

$ git tag

```

to push local code to created tag
```bash

$ git push --tags

```

to delete tag (frist you have to delete it locally)
```bash

$ git tag -d v1.0
$ git push origin :v1.0

```

to change/go tag
```bash

$ git checkout 'v1.0'

```

to recover stash for pull
$ git stash 
to recover stash after push
$ git stash apply
to see stash list
$ git stash list


to create new ssh key (https://docs.gitlab.com/ee/ssh/)
$ ssh-keygen -t rsa -b 2048 -C "email@example.com"

to see what is current ssh account
$ssh -T git@gitlab.com

to change current ssh account key
$ eval $(ssh-agent -s)
$ ssh-add <path to private SSH key>
