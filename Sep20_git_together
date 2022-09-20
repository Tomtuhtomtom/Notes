## Review of Git
_*slides.com is a good site for storing a slideshow_

Site for topic:
https://slides.com/d/32P0USg/live

__Workspace__
Where you are working, making changes

git add

__Index__
Stuff you have added so when you run git add <stuff you're adding>

git commit

__Local Repo__
Stuff you've commited, it stays on your computer, a local repo

git push

__remote repo__
GitHub is a remote repo but there are others, once you commit to your local machine, you can git push it to whatever remote repo you want

## It's in the History
git log --oneline

Uses a hash algirthym to give each commit a unique identifier
Newest is always on top

## Branching
A place to work off to the side to try some stuff without affecting the main branch

_Atlassian has a good git tutorial_

## Creating a new branch
__Make sure you are making a branch off the main__
on the main branch:
git pull origin main

make a new branch and switch to that branch
git switch -c <name of new branch>

## Choosing a branching strategy
__Option 1 (Recommended)__
The Production branch: Main or Production
This is the shared branch that you deploy to production
Feature branches are merged in via pull requests

_Tips_
    git branch - shows your branches
    git branch <name of branch> - creates that branch off the branch you are on
    git switch - goes back to the one you were just at
    Use convention of team but commit messages showed say what this commit will do 'fixes this'

The Feature branch: <whatever you named it>
This is where you will do your development work.  You'll push changes to this branch and open a pull request to main when you're ready to let others see your work

__Option 2 (complicated-not recommended)__
adds a shared development branch

## How to start this Phase 3 project
1.  One dev creates the repo and makes the initial commit on local main to start a new BE project
2.  The initial commit should be made on local main and pushed to the remote main __This is the only time we'll commit or push directly to main__
3.  Other devs will clone this repo
4.  Each dev chooses a task, creates a feature branch off of main, and works ON THAT BRANCH
5.  Name the branch something descriptive of the work
6.  Write code and commit to that branch
7.  You can push your branch up to GitHub at any time

## Team Workflow
1.  Each dev creates a feature branch
2.  Dev commits and tests locally on their branch
3.  Dev keeps their branch up to date with main
4.  Dev opens a pull request(PR) when ready and requests a review
5.  Teammate reviews the PR and discusses
6.  If changes are needed, dev commits locally and pushes new commit to remote feature branch, this updates the PR
7.  When reviewers and dev's agree, the PR is merged
8.  After merging, delete the feature branch __Do not work on this branch anymore__
9.  Remote main has changed, so each dev pulls down changes from remote to local MAIN
10. Devs can merge the changes to their in-progress feature branch or make a NEW feature branch from main to work on something else.

## Individual How to start
Start on the main branch
git pull origin main

create your feature branch
git switch -c <name of feature>

## Individual workflow
Keep LOCAL main up to date
git pull origin main

Keep your feature branch up to date with main
git merge main - this command merges your local main into the feature branch

Push your feature branch to GitHub
git push origin <name of feature branch>

## When to open a pull request
    got feedback
    finished all the code for feature
    merged the most recent commits from main into feature branch
    tested that the code works before and after merging the main branch
If all of these things are good, then it's ready for a pull request

Use the Git Collaboration reference for how to make a pull request and ask Amy for help

__After your pull request is merged__
you will pull the main again, create and switch to a new feature branch and then delete the former branch
git branch -d <name of feature branch>

