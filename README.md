# GIT

### Attach local branch to Remote Repository
	- git init
	- git add readme.md
	- git commit -m "initial" .
	- git branch -M main
	- git remote add origin <<git url>
	- git push origin main
 
#### Some of the GIT commands

- [git cherry](https://www.youtube.com/watch?v=SwDF9mtI8Ek)
- [merge](https://www.youtube.com/watch?v=SwDF9mtI8Ek)
- [rebase](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [fetch](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [tags](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH) : Naming the label to particualar commit, we can refer this tag for feature use.

      	- gt tav v1.0.0
  
	- git tag ( list all tags)
   
	- git tag -l "*SOI*"
   
	- git checkout <tagname> // tagname is nothing but a commit id, it will detach the HEAD
   
	- git  checkout HEAD~2 , // it will checkout the code which is in commit 2
   
- [conflict](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [reset](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [stash](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [squache](https://www.youtube.com/watch?v=viY1BbKZhSI)
        Git to combine multiple commits into a single commit. This is particularly useful for cleaning up a commit history before merging a feature branch into a main branch

          Example
  
            1. Git rebase –i HEAD@{3}
  
            2. It will open editor
  
            3. Just add key word squash <existing commit id> comments, it will delete the comments which you do not want, and add new comments.
  
              ![image](https://github.com/user-attachments/assets/5d138654-9b49-4bf9-bc39-b8e246d7e9cf)
  
            4. git rebase --continue
  
            5. git push origin main -f
  

- [cherry-pick](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [logs](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [ pull](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [reflog](https://www.youtube.com/watch?v=SwDF9mtI8Ek)
  	- This logs available only in local  , not available to other collaborator.
	- This logs will expire after 90 days, if you want to customise , use below commands
		git config gc.reflogExpire "6 months"
		git config gc.reflogExpireUnreachable "1 year"

  	- git show reflog
  	- git reflog show master@{2} // it will skip {0}&{1} from the list , will display all logs from {2}
  	- git reflog show master@{1.day.ago} //  it will display one day ago log of the master branch
  	- git diff main main@HEAD{3}
  	- git diff main main@{1.week.ago}
    

# Git branching strategy

### Branches:

- [master] : Contains production-ready code.
- [develop] : Integration branch where features are merged before release.
- [feature/*] : Branches created from develop for new features.
- [release/*] : Branches created from develop for preparing a new release.
- [hotfix/*] : Branches created from master for urgent fixes.

### Workflow:

- [Create a feature/* branch from develop for new features.]
- [Merge feature branches into develop.]
- [When ready for release create a release/* branch from develop.]
- [After finalizing the release merge release/* into both master and develop.]
- [For urgent fixes create a hotfix/* branch from master then merge it into both master and develop.]

### Differences
- [Forking]: creates a personal copy of someone else’s repository on a hosting service like GitHub.he is not collaborator but he can contribute to the code and raise the PR
- [Cloning]: creates a copy of an entire repository on your local machine.
### Hosting Static webpage
- create repo with this name formate  **<github_accountname.github.io> narayana.github.io**
- git commit -m index.html
- git push -u main
- go to setting/pages , here we can find our webpage URL like this - https://narayanatg.github.io/
### Setting Alias for git commands
- Go to **c/user/hp/.gitconfig** file add below commands to set alias for **status, log and commit** command

	[alias]
	
	s = status
	
	l = log
	
	cm = commit -m
	
// just press **s** it will display the status of the branch , need to type complete command like git status, like similar for other commands)

- Setting alias through CMD

	git config --global alias.s "status"
### To know your git config file location
	git config --list --show-origin
	git config --list --show-origin --global
