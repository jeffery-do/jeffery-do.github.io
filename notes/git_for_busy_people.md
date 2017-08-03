## Primer to Git for Busy People

Git is the most popular version control system.
While debugging git errors may be annoying,
the following pipeline I'll show you will hopefull
allow you to avoid the plethora of possible gotchas
Git may bestoy onto you.

This is how I use git, and it work roughly 95%+ of the time.

Step 1:
Clone your repo!
```
git clone https://github.com/jeffery-do/jeffery-do.github.io.git
# The above snip is for clone my blogging repo!
```
Cloning is pretty straight forward. There is a https version,
and a ssh version. If you have an ssh key setup on your account and
your system, go for it. Going with that way will save you the
annoyance of putting your github password into your terminal
all the time.

Step 2:
Make a branch!
```
git pull origin master
# in this command, I'm pulling the latest changes from master
# I'm looking within origin(kinda like the root location
# to find the main master branch

git branch jedo/git_for_busy_people
# here I'm making a branch so that your code can be seperated.
# this seperation will keep your code safe while you are still
# modifying it

git checkout jedo/git_for_busy_people
# This will move you to your the jedo/git_for_busy_people branch that was
# just made. You can use git checkout origin master if you wish to
# go back to the master branch.
```
Don't let anyone tell you it's okay to always push to master. 
If I were you, I would nod my head, and tell them "I guess that makes
sense". But really, unless you plan on mever using your repo again, 
always make branches.

Why? Because if you use branches your code will be tidier,
you can more safely rewrite your commits,
you can save your branch's half finished work to git whenever you want,
you can quickly and easily switch between your working code,
and also you can easily show other developers what you are working on.
Even if you are the only one using your repo, 
using branches is a good habit, and will make your life easier.
It's incredibly annoying when you step into a new repo, and it's filled with
useless commits, unusuable history, a developer who never makes branches because
they "never needed to, and doesn't see the point in doing it".
Making a branch and using it takes a few seconds, and will allow you to be more organized.
This will pay off greatly in terms of productivity.
#RantOver

Step 3:
Write your code!!!!
```
make whatever changes you want now that you are in a branch, your code changes will
be isolated from the rest of the source code history.
```

Step 4-inf:
Using git status...
```
git status
```

git status will be the oracle that will lead your way through your git centric life.
It will tell you what files you have modified, what files you haven't added to
git yet, and what files you have staged(we will get to that later).
Warning!!! This will not show you what you have commited... You'll
have to do some git log magic for that... I might speak about
that some other time...

Step 5:
Add and Commit your Code!!!
```
git status # do this to see file paths of things you have modified
git add path_to_file
# add just path_to_file to be commited

git reset HEAD path_to_file
# oops, run this command if you didn't intend to add a file. This will note change 
# the file in any way!

git add . 
# this will add everything that I have modified in the currect directory or below.

git commit -m "I created the path_to_file as a placeholder for the demo!"
```

Step 6:
Check out your handywork!
```
git log
# this is how you can view all the commits that have happened

git show commit_id 
# this will allow you to see what exactly changed in a commit

git reset --soft HEAD~
# this can be used if your most recent commit is misguided. This will not change
# the files which are currently within your repo, and will all changes staged.
```

Step 7:
Let the world see your changes!
```
git push origin jedo/git_for_busy_people
# This will push up your branch so that it can be seen by Github(ie, remotely)
```
By doing the above, your branch will be pushed for the world to see. If you go
onto github, your branch will be visible, and from here, you can initate a 
PR(Pull Request). The github interface gives you an approchable and easy way
for you to double check your changes, and allow others to see your branch.
If you do a Pull Request, others will be able to give feedback on your code.
If it is to yours and your team's liking, the project owner/admin can decide
to merge your pull request with master with a click of a button.


Step 8:
Rinse and repeat
```
git checkout origin master # go back to the master branch

git pull # get latest changes

git branch jedo/on_to_the_next_thing # make a new branch
git checkout jedo/on_to_the_next_thing # go to the new branch

git checkout jedo/git_for_busy_people # go back to old branch
# make some changes here
git add .
git commit -m "Removed redundant emoji characters"
git push origin jedo/git_for_busy_people
# ping people to look at your pull request
# someone merges your changes to master

git checkout jedo/on_to_the_next_thing # going back to your new work
```

And that's the majority of the workflow for Git.
And I hope you will grow as fond of it as I have.
I will likely create some advanced tips to help people
mess with the git commit history, or deal with merge conflicts.
Hopefully if you and your team goes with this branch approach,
te majority of merge conflicts can just be resolved by a 
`git stash` and `git stash pop` (you saving your changes to git's stack 
and then poping them off after you finish your pull. There may still
be some merge conflicts, but that is a topic for a different post).

Until we meet again, Goodbye!
