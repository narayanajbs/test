# GIT
#### Some of the GIT commands

- [git cherry](https://www.youtube.com/watch?v=SwDF9mtI8Ek)
- [merge](https://www.youtube.com/watch?v=SwDF9mtI8Ek)
- [rebase](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [fetch](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [tags](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
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

