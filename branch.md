[< back to contents](./readme.md)

# git branch

**git branch *[options]*** - List, create, or delete branches

**Options:**

-d   
--delete  
Delete a branch. The branch must be fully merged in its upstream branch...

-m  
--move  
Move/rename a branch and the corresponding reflog.

-l  
--list  
List branches.

the following command force change the name of branch:
```bash-
git branch -M main
```
Shortcut for `git branch <branchname>` following `git checkout <branchname>` 
```bash
git checkout -b <branchname>
```
For switching branches use the command:
```bash
git checkout <branchname>
```

For detailed information follow [link](https://git-scm.com/docs/git-branch)

[<Previous](./log.md) ... [Next>](./remote.md)