# GIT -WORLD
***Git-World is a repository of all my knowledge and notes that were accumalated while learning Github and terminal commands.***


## LINUX COMMANDS

- > To list the files and folder in the pointed directory.

```
ls
```
- > To create a new folder in the directory (Make Directory)

```
mkdir <folderName>
```

- > To open the directory by mentioning the folder name (Change Directory) 

```
cd <folderName/fileName>
```

- >  To access hidden folders or file

```
ls -a
```

- > To create a new file

```
touch <fileName>
```

- > To display the content of the file

```
cat <fileName>
```

- > To remove a file or folder 

```
rm -rf <FileName/foldrName>  (rm stands for remove; rf stands for recursive force)
```


## GIT COMMANDS

The history of the changes done in the directory will be stored in the .git folder.
The .git folder is a hidden folder, which can be accessed using the particular linux command.

- > To initialize an empty or existing git repository of the directory to maintain history

```
git init
```

- > To find the changes or status of the current file 
    _ The following command displays the untracked files(_new file added to local directory_), modified files(_changes in already existing file_) and deleted files(_removed file in local, which is different from remote repository_)

```
git status
```
- > To stage the changes done to git in the directory

```
git add . (Adds all the untracked files from the directory)
git add <fileName> (Adds specific files)
```

- > To record the history of the changes made in local directory to remote git repository

```
git commit -m "example message" (m stands for message)
```

- > To remove the modified file from stage without committing to git repository

```
git restore --staged <fileName>
```

- > To find the entire history of the directory

```
git log
```

- > To delete the previous commits (_All the later commits to the selected commit ID will be removed i.e will be unstaged_)

```
git reset <commitID>
```

- > To provide a temporary file saving of the changes done in it, without disturbing the orginal file. If needed, they can also be retrieved back to the stage to get commited or be deleted from the temporary memory without coming back

```
git stash (Send the changes done to temp memory)
git stash pop (Bring back the changes to unstaged state)
git stash clear (Delete all the history of the temp memory, making them inaccessible again)
```

- > To link the remote github repository to our local directory via url link

```
git remote add origin <remoteRepoURL> (origin is like the name given the specified url)
```

- > To push the changes to the remote git repository

```
git push <origin/remoteRepoURL> <branchName>
```

- > To view the linked remote repository

```
git remote -v
```

- > To create a new sub-branch from an existing branch

```
git checkout -b <sub-branch> <main-branch>
```

- > To move to the desired branch

```
git checkout <branchName>
```

- > To view the list of branches from the origin 

```
git branch
```

- > To merge the sub-branch to main-branch

```
git checkout <main-branch>
git merge <sub-branch>
```

- > To link the remote upstream github repository to our local directory via url link

```
git remote add upstream <remoteUpstreamRepoURL>
```

- > To fetch all the changes or commits from the upstream to my forked repository and to reset the main branch of my forked repo to the main branch of the upstream main branch

```
git fetch --all --prune
git reset --hard upstream/main

or 

git pull upstream main
```

- > To squash merge multiple commits to one commit

```
git rebase -i <commitID> (i stands for interactive environment)

pick commit1
s commit2
s commit3
s commit4

(All the commits with s will be merged with the above pick commit ID)
```










