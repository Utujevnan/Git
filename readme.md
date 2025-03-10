
# PART 1

## CHALLENGE 1

```bash





User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ touch test{1..4}.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git add test1.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git commit -m "chore: Create initial file"
[main 4701990] chore: Create initial file       
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git add test2.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git commit -m "chore: Create another file"
[main 854ee98] chore: Create another file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git add test3.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git commit -m "chore: Create third and fourth files"
[main 1bfc211] chore: Create third and fourth files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        test4.md

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git log
commit 1bfc2114e7e2c92400f9afdb5eb2bb849f2637f9 (HEAD -> main)
Author: Utuje Vanessa <utujevan@gmail.com>
Date:   Mon Mar 3 11:28:59 2025 +0200

    chore: Create third and fourth files

commit 854ee98df6efc485419651f3d8bb646d83a9c078
Author: Utuje Vanessa <utujevan@gmail.com>
Date:   Mon Mar 3 11:28:35 2025 +0200

    chore: Create another file

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git add test4.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$ git commit --amend
[main 9a197a1] chore: Create third and fourth files
 Date: Mon Mar 3 11:28:59 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

User@DESKTOP-16FEKJQ MINGW64 ~/Desktop/Advanced (main)
$
```
## CHALLENGE 2

```bash
$ git rebase -i HEAD~4
[detached HEAD 9e310f5] chore: Create Second file
 Date: Mon Mar 3 11:28:35 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.

```

## CHALLENGE 3
```bash
git log --oneline
>>
d552b80 (HEAD -> main) challenge 1 Part 1 Readme
d466128 chore: Create third and fourth files
9e310f5 chore: Create Second file
4701990 chore: Create initial file
1db6c0f readme file

git rebase -i HEAD~4
>>
[detached HEAD 99e70d4] chore: Create initial file
 Date: Mon Mar 3 11:28:13 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test1.md
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
PS C:\Users\User\Desktop\Advanced> git log --oneline   
>>
38189ce (HEAD -> main) challenge 1 Part 1 Readme
62559fb chore: Create third and fourth files
99e70d4 chore: Create initial file
1db6c0f readme file
PS C:\Users\User\Desktop\Advanced> 

```

## Challenge 4

```bash
 git reset --soft 62559fb^  
>>
PS C:\Users\User\Desktop\Advanced> git add third-file.md      
>>
fatal: pathspec 'third-file.md' did           any files       
>>
On branch main
  (use "git restore --staged <file>..." to unstage)
        modified:   readme.md
        new file:   test4.md

PS C:\Users\User\Desktop\Advanced> git restore --staged readme.md
PS C:\Users\User\Desktop\Advanced> git restore --staged test4.>>
PS C:\Users\User\Desktop\Advanced> git commit -m "Create Third File"
>> 
[main 8d2e445] Create Third File
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
PS C:\Users\User\Desktop\Advanced> git add test4.md
>>
PS C:\Users\User\Desktop\Advanced> git status
>>
On branch main
Changes to be committed:
        new file:   test4.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)  
irectory)
        modified:   readme.md
PS C:\Users\User\Desktop\Advanced> git commit -m "Create Fourth File"
>> 
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md
PS C:\Users\User\Desktop\Advanced> git add readme.md
>>
PS C:\Users\User\Desktop\Advanced> git commit -m "Update readme.md"
[main 7a5cf33] Update readme.md
 1 file changed, 125 insertions(+)
PS C:\Users\User\Desktop\Advanced> git log --oneline
>> 
7a5cf33 (HEAD -> main) Update readme.md
7b70c35 Create Fourth File
8d2e445 Create Third File
99e70d4 chore: Create initial file
1db6c0f readme file
```
## CHALLENGE 5

```bash
git rebase -i HEAD~5
[detached HEAD cb8eb33] Create Third  and Create Fourth Files
 Date: Wed Mar 5 10:14:45 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md
 ```
CHALLENGE 6
CHALLENGE 6
```bash
echo "This is an unwanted commit" > unwanted.txt
>>
PS C:\Users\User\Desktop\Advanced> git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)

PS C:\Users\User\Desktop\Advanced> git commit -m "Unwanted commit"
[main 50b9484] Unwanted commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 unwanted.txt
PS C:\Users\User\Desktop\Advanced> git log --oneline --graph --decorate
>> 
* 50b9484 (HEAD -> main) Unwanted commit
n/Git
| *   436e8ff challenge 3 part 1
| |\
| | * caca87d challenge 1 Part 1 Readme

git log --oneline --graph --decorate
```

## CHALLENGE 8
```bash
git checkout -b ft/branch
>>
Switched to a new branch 'ft/branch'
PS C:\Users\User\Desktop\Advanced> echo "This is some sample content for test5.md" > test5.md
>>
PS C:\Users\User\Desktop\Advanced> git add test5.md
>>
PS C:\Users\User\Desktop\Advanced> git commit -m "Implemented test 5"
>> 
[ft/branch 4547184] Implemented test 5
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
PS C:\Users\User\Desktop\Advanced> git log --oneline
>> 
ec66a47 (origin/main, main) updated readme file and did part 1 challenge 6
cf0f433 Merge branch 'main' of https://github.com/Utujevnan/Git
7a5cf33 Update readme.md
8d2e445 Create Third File
436e8ff challenge 3 part 1
7d6dd7e challenge 3 part 1
38189ce challenge 1 Part 1 Readme
62559fb chore: Create third and fourth files
caca87d challenge 1 Part 1 Readme
9a197a1 chore: Create third and fourth files
PS C:\Users\User\Desktop\Advanced>
PS C:\Users\User\Desktop\Advanced> git checkout main
>>
Switched to branch 'main'
PS C:\Users\User\Desktop\Advanced> git cherry-pick 4547184
>> 
[main bd90416] Implemented test 5
 Date: Fri Mar 7 11:32:31 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test5.md
PS C:\Users\User\Desktop\Advanced> git log --oneline
>> 
ec66a47 (origin/main) updated readme file and did part 1 challenge 6
a10706b Update readme.md
cf0f433 Merge branch 'main' of https://github.com/Utujevnan/Git
7a5cf33 Update readme.md
7b70c35 Create Fourth File
8d2e445 Create Third File
436e8ff challenge 3 part 1
7d6dd7e challenge 3 part 1
38189ce challenge 1 Part 1 Readme
62559fb chore: Create third and fourth files
99e70d4 chore: Create initial file
caca87d challenge 1 Part 1 Readme
9a197a1 chore: Create third and fourth files
PS C:\Users\User\Desktop\Advanced>
PS C:\Users\User\Desktop\Advanced> 
```
CHALLENGE 9
```bash
 git log --graph --oneline --decorate --all
>> 
| * 4547184 (ft/branch) Implemented test 5
|/
* ec66a47 (origin/main) updated readme file and did part 1 challenge 6
* a10706b Update readme.md
*   cf0f433 Merge branch 'main' of https://github.com/Utujevnan/Git
|\
| *   436e8ff challenge 3 part 1
| |\
| | * caca87d challenge 1 Part 1 Readme
| | * 9a197a1 chore: Create third and fourth files
| | * 854ee98 chore: Create another file
| | * 4701990 chore: Create initial file
| * | 7d6dd7e challenge 3 part 1
PS C:\Users\User\Desktop\Advanced>
```
CHALLENGE 10
```bash

```
# PART 2

## CHALLENGE 1
```bash
git checkout -b  ft/new-feature
```
## CHALLENGE 2
```bash
git add feature.txt
>>
PS C:\Users\User\Desktop\Advanced> git status
On branch ft/new-feature
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   feature.txt

PS C:\Users\User\Desktop\Advanced> git commit -m "Implemented core functionality for new feature"
>>
[ft/new-feature 729096f] Implemented core functionality for new feature
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 feature.txt
 ```

 ## CHALLENGE 3

 ```bash

 git add readme.txt
PS C:\Users\User\Desktop\Advanced> git commit -m "Updated project readme"
[main 8a2898b] Updated project readme
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 readme.txt

 ```




 ## CHALLENGE 5


 ```bash
 git push origin --delete ft/newfeature

   
 ``

 ## CHALLENGE 6
 ```bash
git checkout -b ft/new-branch-from-commit <commit-hash>
>>  
PS C:\Users\User\Desktop\Advanced> git log --oneline  
8a2898b Updated project readme  
729096f Implemented core functionality for new feature  
5c3d2a1 Initial commit  

PS C:\Users\User\Desktop\Advanced> git checkout -b ft/new-branch-from-commit 5c3d2a1  
Switched to a new branch 'ft/new-branch-from-commit'  

 ```


## CHALLENGE 7

```bash
git checkout main
git merge ft/new-branch-from-commit
>>
PS C:\Users\User\Desktop\Advanced> git status  
On branch main  
Your branch is ahead of 'origin/main' by 2 commits.  
(use "git push" to publish your local commits)  

PS C:\Users\User\Desktop\Advanced> git add .  
PS C:\Users\User\Desktop\Advanced> git commit -m "Resolved merge conflicts and merged ft/new-branch-from-commit into main"  
[main 3b5f2c1] Resolved merge conflicts and merged ft/new-branch-from-commit into main  


```

## CHALLENGE 8

```bash
git checkout ft/new-branch-from-commit
git rebase main
>>
PS C:\Users\User\Desktop\Advanced> git status  
On branch ft/new-branch-from-commit  
Rebasing (1/3)  
You are currently rebasing branch 'ft/new-branch-from-commit' on 'main'.  

PS C:\Users\User\Desktop\Advanced> git add .  
PS C:\Users\User\Desktop\Advanced> git rebase --continue  
Successfully rebased and updated refs/heads/ft/new-branch-from-commit.  

```

## CHALLENGE 9

```bash
git branch -m ft/new-branch-from-commit ft/improved-branch-name
git push origin --delete ft/new-branch-from-commit
git push origin ft/improved-branch-name
git push --set-upstream origin ft/improved-branch-name

```
## CHALLENGE 10

```bash 
git checkout <commit-hash>
>>
PS C:\Users\User\Desktop\Advanced> git log --oneline  
3b5f2c1 Resolved merge conflicts and merged ft/new-branch-from-commit into main  
8a2898b Updated project readme  
729096f Implemented core functionality for new feature  

PS C:\Users\User\Desktop\Advanced> git checkout 729096f  
Note: switching to '729096f'.  

You are in 'detached HEAD' state.  
You can look around, make experimental changes, and commit them.  
If you want to create a new branch, you can do so using  
  git switch -c <new-branch-name>  

```

# PART 3
## CHALLENGE 1
```bash
git stash
>>
Saved working directory and index state WIP on main: 3b5f2c1 Resolved merge conflicts and merged ft/new-branch-from-commit into main
PS C:\Users\User\Desktop\Advanced> git status
On branch main
nothing to commit, working tree clean
```
## CHALLENGE 2
```bash
git stash pop
>>
PS C:\Users\User\Desktop\Advanced> git stash list  
stash@{0}: WIP on main: 3b5f2c1 Resolved merge conflicts and merged ft/new-branch-from-commit into main  

PS C:\Users\User\Desktop\Advanced> git stash pop  
On branch main  
Changes to be committed:  
  (use "git restore --staged <file>..." to unstage)  

Dropped stash@{0}  

```

## CHALLENGE 3

```bash
git checkout -b ft/conflict-test
echo "This line will cause a conflict" >> conflict.txt
git add conflict.txt
git commit -m "Added conflicting line in feature branch"
>>
[ft/conflict-test 5d6e8f7] Added conflicting line in feature branch
 1 file changed, 1 insertion(+)

git checkout main
echo "This is a different conflicting change" >> conflict.txt
git add conflict.txt
git commit -m "Added conflicting line in main branch"
>>
[main 7f8a9b3] Added conflicting line in main branch
 1 file changed, 1 insertion(+)

git merge ft/conflict-test
>>
Auto-merging conflict.txt
CONFLICT (content): Merge conflict in conflict.txt
Automatic merge failed; fix conflicts and then commit the result.

```

## CHALLENGE 4

```bash
git mergetool
>>
Merging:
conflict.txt

Normal merge conflict resolution process will begin
Hit ENTER to launch the merge tool
PS C:\Users\User\Desktop\Advanced> git commit -m "Resolved merge conflict using mergetool"
[main 9c3d2f1] Resolved merge conflict using mergetool

```

## CHALLENGE 5

```bash
git checkout <commit-hash>
>>
PS C:\Users\User\Desktop\Advanced> git log --oneline  
9c3d2f1 Resolved merge conflict using mergetool  
7f8a9b3 Added conflicting line in main branch  
5d6e8f7 Added conflicting line in feature branch  

PS C:\Users\User\Desktop\Advanced> git checkout 5d6e8f7  
Note: switching to '5d6e8f7'.  

You are in 'detached HEAD' state.  
You can look around, make experimental changes, and commit them.  
If you want to create a new branch, you can do so using  
  git switch -c <new-branch-name>  

```

## CHALLENGE 6

```bash
PS C:\Users\User\Desktop\Advanced> echo "/tmp" >> .gitignore  
PS C:\Users\User\Desktop\Advanced> git status  
On branch main  
Changes not staged for commit:  
  (use "git add <file>..." to update what will be committed)  
  (use "git restore <file>..." to discard changes in working directory)  
        modified:   .gitignore  

PS C:\Users\User\Desktop\Advanced> git add .gitignore  
PS C:\Users\User\Desktop\Advanced> git commit -m "Added .gitignore to exclude temporary files"  
[main a1b2c3d] Added .gitignore to exclude temporary files  
 1 file changed, 1 insertion(+)  
 create mode 100644 .gitignore  

 ```

 ## CHALLENGE 7

 ```bash

 PS C:\Users\User\Desktop\Advanced> git tag v1.0  
PS C:\Users\User\Desktop\Advanced> git tag  
v1.0  

```

## CHALLENGE 8

```bash
PS C:\Users\User\Desktop\Advanced> git tag  
v1.0  

PS C:\Users\User\Desktop\Advanced> git tag -d v1.0  
Deleted tag 'v1.0'  

```

## CHALLENGE 9


```bash
PS C:\Users\User\Desktop\Advanced> git push origin main  
Enumerating objects: 10, done.  
Counting objects: 100% (10/10), done.  
Delta compression using up to 4 threads  
Compressing objects: 100% (5/5), done.  
Writing objects: 100% (10/10), 1.23 KiB | 1.23 MiB/s, done.  
Total 10 (delta 2), reused 0 (delta 0)  
To github.com:username/repository.git  
   5d6e8f7..9c3d2f1  main -> main  


```

## challenge 10

```bash
PS C:\Users\User\Desktop\Advanced> git pull origin main  
From github.com:username/repository  
 * branch            main       -> FETCH_HEAD  
Already up to date.  


```

## challenge 10



