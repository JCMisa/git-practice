## MY README FILE

### Seting up new repository

1. create repository on github
2. git init
3. git add .
4. git branch -M main
5. git push -u origin main

### If there are new changes in existing file that you want to push:

1. git add <File with Changes>
2. git commit -m "update message"
3. git push -u origin main

### To push changes in existing file that will be only shown in a new branch

1. git status -> check on what branch you are currently working with
2. git stash save "message" -> to disable changes that youve done first **(do this before switch to other branch and push there the changes)**
3. git checkout -b name-of-new-branch -> to create a new branch name
4. git stash pop -> show the changes again in the modified file that you want to push in other branch **(unstach changes once you are in the other branch)**
5. git add file-name
6. git commit -m "message"
7. git push -u origin name-of-new-branch

### To rename the branch you created

1. git checkout main -> go back to main branch first
2. git branch -m branch-old-name branch-new-name
3. git push -u origin name-of-new-branch
4. git push origin --delete name-of-old-branch -> delete the old branch name

### to merge changes of a specific file from main to other branch or vice versa

1. git log --oneline -- file_name -> get the changes commit messages ids and copy it
2. git checkout branch_where_you_want_to_merge_file_changes
3. git cherry-pick <commit_id>
4. git add .
5. git commit -m "message"
6. git push -u origin branch_name
