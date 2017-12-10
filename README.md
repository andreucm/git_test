# git_test
Testing playground with Git

## Splitting with cherry-pick
The purpose of this procedure is to split a single and existing development line in several branches, from a given commit in the past.

 - Move to the commit you want to start the split, create a branch there, and move to that branch
 ```shell
 $ git branch BRANCH_NAME COMMIT_NUM_SPLIT
 $ git checkout BRANCH_NAME
 ```

 - Add existing commits to that new branch
 ```shell
 $ git cherry-pick COMMIT_NUM_A
 $ git cherry-pick COMMIT_NUM_B
 ...
 $ git push origin BRANCH_NAME
 ```

 - Come back to master
 ```shell
 $ git checkout master
 ```

At this point we have created a branch starting at COMMIT_NUM_SPLIT, and containing commit COMMIT_NUM_A and COMMIT_NUM_B.
