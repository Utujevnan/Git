# PART 1
## Challenge 1

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
## Challenge 2


```bash

$ git rebase -i HEAD~4
[detached HEAD 9e310f5] chore: Create Second file
 Date: Mon Mar 3 11:28:35 2025 +0200
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.

```





## Challenge 3

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

## challenge4

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
## Challenge 5
```bash
git rebase -i HEAD~5
[detached HEAD cb8eb33] Create Third  and Create Fourth Files
 Date: Wed Mar 5 10:14:45 2025 +0200
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

 ```

 ## Challenge 6

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
