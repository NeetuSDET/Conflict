# Conflict
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git init
Reinitialized existing Git repository in /Users/rajnishkhatri/Desktop/Conf/.git/
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git add .
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "initial commit form the master"
[main (root-commit) f61fc0d] initial commit form the master
 1 file changed, 1 insertion(+)
 create mode 100644 a.txt
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout -b branch1
Switched to a new branch 'branch1'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git branch
* branch1
  main
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout -b branch1
fatal: a branch named 'branch1' already exists
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git branch
* branch1
  main
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git add .
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "commit from the branch1"
[branch1 904aa9c] commit from the branch1
 1 file changed, 2 insertions(+), 1 deletion(-)
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout master
error: pathspec 'master' did not match any file(s) known to git
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout master
error: pathspec 'master' did not match any file(s) known to git
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout -b branch2
Switched to a new branch 'branch2'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git branch
  branch1
* branch2
  main
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git add .
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "commit from the branch2"
[branch2 d0bdb85] commit from the branch2
 1 file changed, 3 insertions(+), 1 deletion(-)
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout master
error: pathspec 'master' did not match any file(s) known to git
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git branch
  branch1
* branch2
  main
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git status
On branch branch2
nothing to commit, working tree clean
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout main
Switched to branch 'main'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout -b master
Switched to a new branch 'master'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git branch
  branch1
  branch2
  main
* master
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$  git merge banch1
merge: banch1 - not something we can merge
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$  git merge branch1
Updating f61fc0d..904aa9c
Fast-forward
 a.txt | 3 ++-
 1 file changed, 2 insertions(+), 1 deletion(-)
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git merge branch2
Updating 904aa9c..d0bdb85
Fast-forward
 a.txt | 4 +++-
 1 file changed, 3 insertions(+), 1 deletion(-)
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git status
On branch master
nothing to commit, working tree clean
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout master
Already on 'master'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git add .
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "master change"
[master d7bd8ab] master change
 1 file changed, 1 insertion(+), 1 deletion(-)
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout branch1
Switched to branch 'branch1'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git status
On branch branch1
nothing to commit, working tree clean
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout master
Switched to branch 'master'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git add .
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "master change"
[master 9d7a82c] master change
 1 file changed, 1 insertion(+), 1 deletion(-)
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout branch1
Switched to branch 'branch1'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git add .
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "branch1 change"
[branch1 33827a3] branch1 change
 1 file changed, 2 insertions(+), 1 deletion(-)
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout master
Switched to branch 'master'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git merge branch1
error: Your local changes to the following files would be overwritten by merge:
        a.txt
Please commit your changes or stash them before you merge.
Aborting
Merge with strategy ort failed.
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ code --version
bash: code: command not found
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "in repo"
On branch master
nothing to commit, working tree clean
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git remote add origin git@github.com:NeetuSDET/Conflict.git
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git push origin main
To github.com:NeetuSDET/Conflict.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'github.com:NeetuSDET/Conflict.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git add .
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "master change"
On branch master
nothing to commit, working tree clean
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git checkout main
git pull origin main --allow-unrelated-historiesSwitched to branch 'main'
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git pull origin main --allow-unrelated-histories
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 863 bytes | 287.00 KiB/s, done.
From github.com:NeetuSDET/Conflict
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main
hint: You have divergent branches and need to specify how to reconcile them.
hint: You can do so by running one of the following commands sometime before
hint: your next pull:
hint:
hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only
hint:
hint: You can replace "git config" with "git config --global" to set a default
hint: preference for all repositories. You can also pass --rebase, --no-rebase,
hint: or --ff-only on the command line to override the configured default per
hint: invocation.
fatal: Need to specify how to reconcile divergent branches.
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git add .
git commit -m "resolved conflict with remote main"(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git commit -m "resolved conflict with remote main"
On branch main
nothing to commit, working tree clean
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git push origin main
To github.com:NeetuSDET/Conflict.git
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'github.com:NeetuSDET/Conflict.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
(base) rajnishkhatris-MacBook-Pro:Conf rajnishkhatri$ git push -u origin master
Enumerating objects: 18, done.
Counting objects: 100% (18/18), done.
Delta compression using up to 8 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (18/18), 1.44 KiB | 1.44 MiB/s, done.
Total 18 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/NeetuSDET/Conflict/pull/new/master
remote: 
To github.com:NeetuSDET/Conflict.git
 * [new branch]      master -> master
branch 'master' set up to track 'origin/master'.
