Create a new `packages.yml` file:

```
packages:
  - git init
  - package: dbt-labs/dbt_utils
    version: 1.3.0
```

### First is to create the git project (.../.git/)
```
git init
```
Checking the status, and it shows no branch yet
```
git status
```
```yml
On branch master

No commits yet

Untracked files:
   (use "git add <file>..." to include in what will be committed)
         .gitignore
         README.md
         analyses/
         dbt_project.yml
         macros/
         models/
         mystic-primacy-478012-q2-195d226f63cf.json:Zone.Identifier
         seeds/
         snapshots/
         tests/
```

### Adding all files to the Git staging area

this is not to GitHub and not to commits yet
```
git add .
```

```
git commit -m "First commit dbt project"
```

### Assigning git remote name 'origin' to the url link
```
git remote add origin https://github.com/Reinchua83/First-dbt-project.git
```
### Creating local branch name 'main'
```
git branch -M main
```
### Pushing the main branch(all local repos) to github via origin
```
git push -u origin main
```

```
LOCAL MACHINE                          GITHUB
----------------------------------------------------
Working directory   →  Staging area   →  Local repo   →  Remote repo
(edit files)           (git add)        (git commit)    (git push)
```


To check the current channel push and pull
```
git remote -v
```

>origin  https://github.com/Reinchua83/First-dbt-project.git (fetch) 
>
>origin  https://github.com/Reinchua83/First-dbt-project.git (push)

To set the upstream branch so git know where to push or pull, use this syntax
```
git branch --set-upstream-to=origin/main
```

this is the same with
```
git branch -u origin/main
```

you can also push with -u flag so you can skip 'origin & main' to pull or push
```
git push -u origin main  ---> git push
```