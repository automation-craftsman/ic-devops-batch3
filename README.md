# Git Assignment - 2

This project demonstrates the usage of Git operations such as branching, rebasing, and pull requests.

## Steps and Commands

1. **Initialize Repository**
   ```bash
   mkdir git-assignment-2
   cd git-assignment-2
   git init
   ```

2. **Add README.md and Push Initial Commit**
   ```bash
   echo "# Git Assignment - 2\" > README.md
   echo "This project demonstrates Git operations." >> README.md
   git add .
   git commit -m "Initial commit with README.md"
   git remote add devops git@github.com:automation-craftsman/ic-devops-batch3.git
   git push devops git-assignment-2
   ```
	<span style="color: salmon; font-weight: bold;">Please note that I am using git-assignment-2 as the main branch in this context since in my local machine I am using a central repository for all the DevOps assignments. Sincere apologies for this little deviation.</span>

3. **Feature Branches**
   - Create `feature-1`:
     ```bash
     git checkout -b feature-1
     echo "This is feature 1." > feature1.txt
     git add .
     git commit -m "Add feature1.txt for feature-1"
     git push devops feature-1
     ```
   - Create `feature-2`:
     ```bash
     git checkout git-assignment-2
     git checkout -b feature-2
     echo "This is feature 2." > feature2.txt
     git add .
     git commit -m "Add feature2.txt for feature-2"
     git push devops feature-2
     ```

4. **Rebase and Merge Pull Requests**
   - Rebase `feature-1`:
     ```bash
     git checkout feature-1
     git rebase git-assignment-2
     git push --force devops feature-1:feature-1
     ```
     Merge `feature-1` into `git-assignment-2` via pull request.

   - Rebase `feature-2`:
     ```bash
     git checkout feature-2
     git rebase git-assignment-2
     git push --force devops feature-2:feature-2
     ```
     Merge `feature-2` into `git-assignment-2` via pull request.

5. **Clean Up**
   - Delete branches locally:
     ```bash
     git branch -d feature-1
     git branch -d feature-2
     ```
   - Delete branches on the remote:
     ```bash
     git push devops --delete feature-1
     git push devops --delete feature-2
     ```

6. **Verify Commit History**
   ```bash
   git checkout git-assignment-2
   git pull devops git-assignment-2
   git log --oneline
   ```
