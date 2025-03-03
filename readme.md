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
###

