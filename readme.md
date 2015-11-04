
Contents of a .git folder:
- HEAD is a pointer to the currently checked out branch
- hooks are scripts you can add to your rep, like do this before committing
- objects, tags
- refs (git's generic name for branches, tags) folder contains the local branches, the remotes, 


- . (dot) is the current directory
- git add, adds changes to the stage

- `git push -u githubschool master:other` pushes upstream (-u) to the remote called githubschool from our local branch called master to the remote branch called other
- `-u` sets up a link between local to remote, once you called -u once... the next time you just do `git push`

- recommended: `git config --global push.default simple`
- `git config push.default =  matching`, then it pushes all your local branches to the remote branches

- `git remote -v` shows all the remotes 
- `git branch -vv` shows all the branches and if they have remotes

- `git cat-file -p bc4152` decompresses a .git/object file