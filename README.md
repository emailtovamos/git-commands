# git-commands

- To create a new branch:

  ```git checkout -b feature/test```

- To undo a recent commit: 

  ```git reset HEAD^```
  
  This can be useful in a following scenario: 
  Let's say you committed something directly in `master` branch in your local repository only to find out later that you can't push it directly in the remote master branch since it is restricted. In that case you use the above command to undo the commit, then you can create another branch by doing `git checkout -b feature/test` and THEN push it: `git push --set-upstream origin feature/test`. After this you can create a pull request to merge into master branch.
