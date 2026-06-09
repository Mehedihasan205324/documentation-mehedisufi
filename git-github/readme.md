## Git & Github

### git flow 

**Working directory -- Stagging area -- local repo -- remote**
<br><br>


```md
git --version
```

### git config

```md
 git config --help
 git config user.email
 git config user.name

 <!-- for new configuration -->

git config --global user.name "Mehedi Hasan"
git config --global user.email demo@gmail.com
```

### Working Flow

``` md
( git init ) -Working directory - (git add .) Stagging area - (git commit -m) local repo - (git push) remte repo
```

### tracking 

```md
git status
git diff
```
### commit history

```md
git log
git log --oneline
```

### branching & merging

```md
git branch (working branch check)
git branch name (branch create)
git checkout branch name (switch branch)
git checkout -b branch name (create and switch)
```

### Merging

```md
<!-- **two way merge** -->

<!-- first you have to go main or master branch -->
<!-- second this command -->
git merge branch name  <!-- which branch you want to merging with main or master branch-->
```

### undo

```md
git checkout -- . (in the working directory)
git reset HEAD . (Staging area)
git reset --hard HEAD  (Staging & Unstaging area)

```


### Correcting commit

```md
git commit --amend (correcting the commit message & added some file in this commit)
- then I for insert something
- then ESE 
- then :wq
```



