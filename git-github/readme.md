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
git branch branch_name (branch create)
git checkout branch_name (switch branch)
git checkout -b branch_name (create and switch)
```

### Merging

```md
<!-- **two way merge** -->

<!-- first you have to go main or master branch -->
<!-- second this command -->
git merge branch name  <!-- which branch you want to merging with main or master branch-->
```
### Undo Only git-commit or stage
```md
git reset HEAD . (Staging area -> working directory) old -> git restore --staged . (modern)

git reset --soft HEAD~1 (from commit ->Staging area )

git reset --mixed HEAD~1 (from commit ->working directory)
```

### Undo With Code

```md
git checkout . (working directory) old -> git restore . (modern) 

⚠️ Warning: git checkout . বা git restore . দিলে আপনার সব আনসেভড কোড চিরতরে মুছে যাবে!


git reset --hard HEAD (Staging & Working directory)

⚠️ Warning: git reset --hard HEAD দিলে আপনার সাম্প্রতিক সব আনসেভড বা মডিফাইড কোড চিরতরে মুছে যাবে এবং প্রজেক্ট একদম শেষ কমিটের (Last Commit) অবস্থায় চলে যাবে!

```

### To change only the commit message:
```md
git commit --amend -m "new correct commit message"
```

### Modify Last Commit with new add (`--amend`)
```md
1. `git commit -m "first"` (কমিট করলেন)
2. ফাইল চেঞ্জ করে -> `git add .` (ফাইল আপডেট করলেন)
3. `git commit --amend -m "new message"` (আগের কমিটের সাথেই নতুন ফাইল ও মেসেজ একসাথে সেভ হয়ে গেল)
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

git rm --cached fileName

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
### Delete a branch
```md
git branch -d Branch_name
```