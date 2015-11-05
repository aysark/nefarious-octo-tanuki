
# Git Advanced Course
Nov 4, 2015

### Contents of a .git folder:
- git is composed of trees that point to a list of blobs, blobs are the actual content files.  Git does not store diffs, diffs are done on the fly.
- HEAD is a pointer to the currently checked out branch, the most recent commit
- hooks are scripts you can add to your rep, like do this before committing
- objects, tags
- refs (git's generic name for branches, tags) folder contains the local branches, the remotes, 


- . (dot) is the current directory
- git add, adds changes to the stage

- `git push -u githubschool master:other` pushes upstream (-u) to the remote called githubschool from our local branch called master to the remote branch called other
- `-u` sets up a link between local to remote, once you called -u once... the next time you just do `git push`

- recommended: `git config --global push.default simple`
- `git config push.default =  matching`, then it pushes all your local branches to the remote branches

#### Merging
- `git merge` does a fastfoward merge (easiest, safest one), moves master branch all the way to the most recent branch
- you can only push if the push is a fastfoward for the recieving end (origin) 
- when you do not do a fastfoward merge (if feature was ahead of master and you were on master and did `git merge feature`), you get the ugly merge commit 

#### Cool Commands
- `git log --oneline --decorate --graph --all` nice visual in cmd line.
- set aliases: `git config --global alias.lol "log  --oneline --decorate --graph --all", then you can do `git lol`
- set aliases: `git config --global alias.s "status -s" gives a shortened status
- `git cherry-pick -x db12c2a`
- `git clean -f -x -d` gives you the cloned repo as it was the first time 
- `git remote -v` shows all the remotes 
- `git branch -vv` shows all the branches and if they have remotes
- `git cat-file -p bc4152` decompresses a .git/object file
- `git pull --rebase`

#### Tips
- you can ignore files in .gitignore and core.excludesfile  -- but once the file has atleast been added/committed once, it would not be ignored.  
- Great visualization tool: http://pcottle.github.io/learnGitBranching/?NODEMO
- list of various .gitignore files: https://github.com/github/gitignore
- course page: https://training.github.com/kit/advanced/
