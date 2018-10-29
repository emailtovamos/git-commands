# git-commands

- To create a new branch and switch to that branch:

  ```git checkout -b feature/test```
  
- To switch to an already existing branch:

  ```git checkout feature/test```
  
- To see remote origin:

  ```git remote -v```
  
- To delete origin connection locally: 

  ```git remote prune origin```
  
- To unset link between current branch and its upstream reference:

  ```git branch --unset-upstream```
  
- To set upstream origin to be `xyz` and push to it: 

  ```git push --set-upstream origin xyz```

- To undo a recent commit: 

  ```git reset HEAD^```
  
  This can be useful in a following scenario: 
  Let's say you committed something directly in `master` branch in your local repository only to find out later that you can't push it directly in the remote master branch since it is restricted. In that case you use the above command to undo the commit, then you can create another branch by doing `git checkout -b feature/test` and THEN push it: `git push --set-upstream origin feature/test`. After this you can create a pull request to merge into master branch.
