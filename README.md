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
- [cherry-pick](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [logs](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [ pull](https://www.youtube.com/watch?v=XdMMfUKBbtE&list=PLzdWZT-ZJD081YB1TLN5rNI1vw5hTdRzH)
- [reflog](https://www.youtube.com/watch?v=SwDF9mtI8Ek)

# Git branching strategy

### Branches:

master: Contains production-ready code.
develop: Integration branch where features are merged before release.
feature/*: Branches created from develop for new features.
release/*: Branches created from develop for preparing a new release.
hotfix/*: Branches created from master for urgent fixes.

### Workflow:

Create a feature/* branch from develop for new features.
Merge feature branches into develop.
When ready for release, create a release/* branch from develop.
After finalizing the release, merge release/* into both master and develop.
For urgent fixes, create a hotfix/* branch from master, then merge it into both master and develop.