# 8 git Commands I Show Every Beginner

“Those who fail to remember the past are condemned to repeat it.” - George Santayana

```
git clone "https://github.com/jeffery-do/jeffery-do.github.io.git" #clone the repo to use
git pull # update your code(for this master branch)
git branch -b "branchName" # create a new branch to work from
git checkout "branchName" # go to the branch
git add ./path/to_file.md # add your changes
git commit -m "fixed to_file.md inf loop bug" # bundle your changes under a message
git push origin branchName # push your bundle(commits) to be accessible on the branch
git checkout master # go back to master
```

Now check out your github repo somewhere like here:
https://github.com/jeffery-do/jeffery-do.github.io
If you recently pushed, you should be able to see something like this:
![recently pushed branch image][images/recently_pushed_branch.png]
From there, you should be able to create a PR. 

![create pull request image][images/create_pull_request.png]
After creating a PR, other people can see your code and comment on your PR.

And after all the required changes are made by them or you, you can merge to master
from there.

# BONUS COMMAND PIPELINES
Here are two bonus pipelines that I use all the time.
Hopefully this will show you how simple git usually is.

### if you need to make changes:
```
git checkout "branchName" # go to your branch
git pull # get any code changes
git add ./path/to_file.md # add your changed
git commit -m "fixed typo" # bundle your changes under a message
git push origin branchName # push your bundle(commits) to be accessible on the branch
```

### and the process continues
```
git checkout master # go to the master branch
git pull # update your code(for this master branch)
git branch "branchName2" # Make a new branch
git checkout branchName2 # Go to the new branch
git add ... # making changes...
```
