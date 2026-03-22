Version control also known as source control  is the practice of tracking and managing codes and files on the codebase.

Git is a distributed version control system that tracks and manages changes in source code efficiently.
Designed for speed, data integrity, and reliable version tracking.
Supports distributed, non-linear workflows.
Enables efficient collaboration for teams and individuals.

GitHub is a web-based platform that hosts Git repositories and adds collaboration features for managing code online.
Adds collaboration features such as pull requests and issue tracking.
Provides code hosting, review, and team collaboration tools.

GitLab
BitBucket
SourceForge

Git pull is a command that performs git fetch followed by git merge or git rebase. While git fetch does not affect the local repository, git pull automatically synchronizes changes from the remote repository with the local repository.

Git rebase integrates changes by replaying your commits on top of the latest state of another branch, creating a cleaner, linear history.
Moves commits to the tip of the target branch.
Rewrites commit history instead of creating a merge commit.
Keeps project history linear and easier to read.
Syntax:
git checkout <feature-branch>
git rebase <base-branch>
<feature-branch> is the branch with the changes you want to rebase.
<base-branch> is the branch you want to rebase your changes onto, typically main or master.

Git cherry-pick allows you to apply a specific commit from one branch onto another without merging the entire branch.
Selectively applies individual commits.
Useful for hotfixes or targeted changes.
Does not bring full branch history.
Git reapplies the selected commit on the current branch, creating a new commit with a different ID.
git cherry-pick  <commit-hash>
Working of Git Cherry-Pick
Each Git commit is uniquely identified by a SHA-1 hash, generated from:
Commit content
Metadata (author, timestamp)
Parent commit(s)
Here’s what happens during cherry-pick:
Identify the Commit: Git locates the commit based on the provided hash.
Generate a Patch: Git calculates the differences (diff) introduced by the commit relative to its parent.
Apply the Patch: Git applies these changes to your current working directory.
Create a New Commit: After applying the changes, Git creates a new commit on your current branch with these changes. This new commit has a different hash due to its different parent commit.
This allows you to selectively transfer changes from one branch to another without merging the full history.

www.geeksforgeeks.org/git/
about.gitlab.com
