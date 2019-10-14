# git-commands

- To start off in a folder: 

  ```git init```
  
- Set your identity to be attached to your commits: 

  ```git config --global user.name "Satyajit Das"```
  
  ```git congig --global user.email emailtovamos@gmail.com```

- To see commit history:

  ```git log```

- To create a new branch and switch to that branch:

  ```git checkout -b feature/test```
  
- To switch to an already existing branch:

  ```git checkout feature/test```
  
- See all branches: 

  ```git branch```
  
- To see remote origin:

  ```git remote -v```
  
- To connect local repository to remote server to push to: 

  ```git remote add origin <remoteServerName>```
  
- To create local copy of remote repository: 

  ```git clone username@host:/path/to/repository```
  
- To delete origin connection locally: 

  ```git remote prune origin```
  
- To unset link between current branch and its upstream reference:

  ```git branch --unset-upstream```
  
- To set upstream origin to be `xyz` and push to it: 

  ```git push --set-upstream origin xyz```
  
- To see manual about `X`:

  ```git X --help```

- To undo a recent commit: 

  ```git reset HEAD^```
  
  This can be useful in a following scenario: 
  Let's say you committed something directly in `master` branch in your local repository only to find out later that you can't push it directly in the remote master branch since it is restricted. In that case you use the above command to undo the commit, then you can create another branch by doing `git checkout -b feature/test` and THEN push it: `git push --set-upstream origin feature/test`. After this you can create a pull request to merge into master branch.
  
- To only include one particular commit of another branch without having to merge the two branches: 

  ```git cherry-pick 33e19bf662a654249e9772ba7e8323f761f7c0b5``` 
  
  ```git cherry-pick <commitnumber>```
  
- To save work which you aren't ready to commit yet: 

  ```git stash```

  To get back the work:
  
  ```git stash pop```
