Changes in ninja branch





GIT LINK ----> https://github.com/mohitmaikhuri03/assignment7.git
Main commands we used

1) made git repo with name assignment 7
2) cloned it in local
3) mkdir ninja
4) adding content to ninja - echo "Trying fast forward merge" > ninja/README.md
5)create a branch ninja and see its status - git checkout -b ninja , git status
6)commit your changed to ninja branch -  git add ninja/README.md
git commit -m "Add README.md with 'Trying fast forward merge' message"
7)Merge the ninja branch to the master branch (with a new commit) ----- git checkout master ,  git merge ninja
8)Assuming you are in the master branch, modify README.md with content "Changes in master branch", commit the changes in master branch.----------->echo "Changes in master branch" > README.md,git add README.md,git commit -m "Updated README.md with changes in master branch",git log --oneline
9)same for ninja branch follow the step 8
10 ) merge ninja with master branch it will give you a conflict
  output---
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
 conflict ---
<<<<<<< HEAD
Changes in master branch
=======
Changes in ninja branch
>>>>>>> ninja

11) we will use theirs here becuse we want to overwrite the master content from ninja content so master
will show ninja content now ----->git checkout --theirs README.md
---> git add README.md
 git commit -m "Resolved conflict by taking changes from ninja branch"
[master dde637a] Resolved conflict by taking changes from ninja branch
