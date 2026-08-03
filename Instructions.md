# Manual Update Workflow

Use this sequence whenever you need to update file(s) directly in the main branch from the terminal.

## Example terminal flow

```powershell
PS C:\Users\Admin\Downloads\workshop_ai> git add .
PS C:\Users\Admin\Downloads\workshop_ai> git commit -m "first commit"
[master (root-commit) 71b6fcd] first commit
 3 files changed, 132 insertions(+)
 create mode 100644 Decisions.md
 create mode 100644 Plan_options.md
 create mode 100644 Project_brief.md
PS C:\Users\Admin\Downloads\workshop_ai> git push -u origin main
error: src refspec main does not match any
error: failed to push some refs to 'https://github.com/naddochuang/course-1-project.git'

PS C:\Users\Admin\Downloads\workshop_ai> git add .
PS C:\Users\Admin\Downloads\workshop_ai> git commit -m "first commit"
[main d04118b] first commit
 4 files changed, 212 insertions(+)
 create mode 100644 Agent.md
 create mode 100644 Plan.md
 create mode 100644 Spec.md
PS C:\Users\Admin\Downloads\workshop_ai> git push -u origin main
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 4.14 KiB | 2.07 MiB/s, done.
Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/naddochuang/course-1-project.git
   71b6fcd..d04118b  main -> main
branch 'main' set up to track 'origin/main'.

PS C:\Users\Admin\Downloads\workshop_ai> git add .\Spec.md
PS C:\Users\Admin\Downloads\workshop_ai> git commit -m "new commit"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

PS C:\Users\Admin\Downloads\workshop_ai> git add .
PS C:\Users\Admin\Downloads\workshop_ai> git commit -m "add space"
[main 8bc43e8] add space
 1 file changed, 1 insertion(+), 1 deletion(-)
PS C:\Users\Admin\Downloads\workshop_ai> git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: (3/3), done.
Writing objects: 100% (5/5), 280 bytes | 280.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/naddochuang/course-1-project.git
   d04118b..8bc43e8  main -> main
branch 'main' set up to track 'origin/main'.
```

## Step-by-step terminal commands

1. Go to the repository folder:
   cd <your-repo-folder>

2. Switch to the main branch:
   git checkout main

3. Update your local main branch from GitHub:
   git pull origin main

4. Edit the file(s) you want to change.

5. Check what changed before staging:
   git diff

6. Stage only the intended files:
   git add <file1> <file2>

7. Commit the changes with a short, clear message:
   git commit -m "Describe the update"

8. Push the commit to the main branch:
   git push origin main

```powershell
git branch --show-current
git status
git diff
git remote -v
```

## If Git asks for your identity

```powershell
git config user.name "naddochuang"
git config user.email "your-email@example.com"
```

## What happened in the earlier example

- The first push failed because the local branch was still on `master`, while the remote branch expected `main`.
- After the branch flow was corrected, `git push -u origin main` succeeded.
- If there is nothing new to commit, Git may return `nothing to commit, working tree clean`.

## Simple rule

1. `git pull origin main`
2. edit files
3. `git add .`
4. `git commit -m "your message"`
5. `git push origin main`
