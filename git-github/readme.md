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
git checkout -- . (working directory) old -> git restore . (modern) 

⚠️ Warning: git checkout -- . বা git restore . দিলে আপনার সব আনসেভড কোড চিরতরে মুছে যাবে!

git reset HEAD . (Staging area) old -> git restore --staged . (modern)
git reset --hard HEAD (Staging & Working directory)

```
### Toggle Previous Branch
- **Description:** আপনাকে হুবহু আগের ব্র্যাঞ্চে (Previous Branch) ফিরিয়ে নিয়ে যায় (ঠিক কম্পিউটারের `Alt + Tab` এর মতো কাজ করে)। বারবার বড় ব্র্যাঞ্চের নাম টাইপ করার ঝামেলা এড়াতে এটি দারুণ একটি শর্টকাট।
```md
git checkout - (old) -> git switch - (modern)
```
### Fast Add & Commit Together

```md
git commit -am "your message"
```
### Correcting commit

```md
git commit --amend (correcting the commit message & added some file in this commit)
- then I for insert something
- then ESE 
- then :wq
```



### .gitignore

```md
Stagging area তে যাবার আগে gitignore এ file or folder add করতে হবে

like before git add . command have to add all file or folder in .gitignore file

```


## Unstagging file 

```md
git add . command দেওয়ার পর যদি মনে পড়ে  কোন file বা folder .gitignore এ add করতে হবে তবে ওই file unstage করে নিতে হবে fist এ

git rm --cacher fileName

```

## Main branch থেকে feature branch-এ কোড আনা এবং Push করার নিয়ম

```md
git checkout problem-page
git pull origin main

git checkout main
git pull

git checkout problem-page
git push origin problem-page

```