#Git workshop 

----

#GIT Installation and setup

__Win__

`https://git-scm.com/download/win`

__Linux (Ubuntu)__

`sudo apt-get install git`

__OSX__

`https://git-scm.com/download/mac`

#UI Client

In this tutorial we will use Source Tree Git UI client, its available for Mac and Win.

```
https://www.sourcetreeapp.com/
```

Beside Source Tree for win you can use Tortoise.

```
https://tortoisegit.org/
```

#Project setup

Before we start using git we should create our working (project) direcory. Create `enter_git_workshop` directory.

#Git initialization

_Start Source Tree_

![](git_workshop/1.png)

_Select new repository_

![](git_workshop/2.png)

_Add path to your `enter_git_workshop` directory_

![](git_workshop/3.png)

_Double click on `enter_git_worshop` repositorum._

![](git_workshop/4.png)

#First commit

_`File Status` tab is place where we will track uncommited and untracked project changes, since we just initialized our repo there is no changes._

![](git_workshop/5.png)

_Go to `enter_git_worshop` directory and create two files `address_book.txt` and `note.txt`. After this we can see them as untracted files._

![](git_workshop/6.png)

_Add them in git versioning by clicking on them. After this we will have them in our index and they are ready to be part of our first commit._

![](git_workshop/7.png)

_Every commit need to have proper message so we will add one._

![](git_workshop/8.png)

_If we take a look again on our `File Status` tab again we don't have any change._

![](git_workshop/9.png)

_But if we look in `Branches` tab we can see our first commit on `master` branch._

![](git_workshop/10.png)

#Adding few more commits

_For sake of practice lets put some more commits in our repo._ 

_Add line `Welcome to Enter conf` in note.txt. Go to `File Status` tab and stage change._

![](git_workshop/11.png)

_Add message and commit change._

![](git_workshop/12.png)

_Check our history progress in `BRANCHES` tab._

![](git_workshop/13.png)

_Add line `Belgrade 11000 Serbia` in address___book.txt. You can also stage changes from `BRANCHES ` tab by clicking on `unstaged files`._

![](git_workshop/14.png)

_But for commit you still need to go to `File Status` tab and write commit message._

![](git_workshop/15.png)

_If we go to `BRANCHES ` tab we can see our changes._

![](git_workshop/21d.png)

#Commit Reset

In git there are three types of reset:

- `soft` - keep all local changes
- `mixed` - keep working copy but reset index
- `hard` - discart all working copy changes

In this workshop you can use any type. End result will be same as long as you performe whole set of instuctions for that type of reset.

_Add this mistake `invalid address` in `address_book.txt`. Stage change and perform commit._

![](git_workshop/17.png)

_Now we have one commited mistake._

![](git_workshop/18.png)

_To perform reset click on commit until which you want to eraise history and choose type of reset._

![](git_workshop/19.png)

__Soft__

_Select soft type._

![](git_workshop/20.png)

_Commit is gone but changes are still in index after reset._

![](git_workshop/21.png)

_Unstage changes._

![](git_workshop/21a.png)

_Discrat them._

![](git_workshop/21b.png)

![](git_workshop/21c.png)

_Mistake removed._

![](git_workshop/21d.png)

__Mixed__

 _Select mixed type._
 
![](git_workshop/24a.png)

_Commit is gone but changes are now unstaged after reset._
 
![](git_workshop/24b.png)

_Discart changes._

![](git_workshop/24c.png)

![](git_workshop/24d.png)

_Mistake removed._

![](git_workshop/24e.png)

__Hard__

![](git_workshop/21d.png)

 _Select hard type._
 
![](git_workshop/22.png)

_There are no changes in index instead they are erased same as commit._

![](git_workshop/22a.png)

#History checkout

There are some cases when you want to iterate trough history and for them we use checkout.

![](git_workshop/25.png)

_Select one commit in history and perform `checkout`_

![](git_workshop/25a1.png) 

_If you take a close look you can notice that our 'HEAD' initactor is now back in history on our initial commit. If you don't beleive check out your project files._

![](git_workshop/25a2.png) 

_We can go back to present in same way we went to past._

![](git_workshop/25a3.png) 

_Back to present._

![](git_workshop/25a4.png) 

#Branching

Branching is very powerfull if you work in team or develop some new features on project.

![](git_workshop/25a4.png) 

_Create new branch `feature/logbook`_

![](git_workshop/25aa.png) 

_Create new file `logbook.txt`_

![](git_workshop/25b.png) 

_Stage and commit changes_

![](git_workshop/25c.png) 

_Now we have two branches different by one commit_

![](git_workshop/25e.png) 

_Checkout back to master_

![](git_workshop/25ee.png) 

![](git_workshop/25f.png) 

_Now we will merge changes from `feature/logbook` branch back to master_

![](git_workshop/25f1.png) 

_Select `feature/logbook` banch._

![](git_workshop/25g.png)

_Now we have all changes in master._ 

![](git_workshop/25h.png)

_After you merge changes from feature branches its good practice to delete them._

_Delete `feature/logbook` banch._

![](git_workshop/25j.png)

_Confirm._

![](git_workshop/25j1.png)

_Now we have only master branch with `feature/logbook` branch changes._

![](git_workshop/25j3.png)

#Stash

_Add changes `line for stash` to `address_book.txt`._

![](git_workshop/26a.png)

_Stage changes._

![](git_workshop/26b.png)

_Stash staged changes._

![](git_workshop/26c.png)

_You can check list of stashes under `STASHES` tab._

![](git_workshop/26d.png)

_Your stashed changes._

![](git_workshop/26e.png)

_Apply stash._

![](git_workshop/26f.png)

_Delte stash from list._

![](git_workshop/26g.png)

![](git_workshop/26h.png)

_And again we have our changes._

![](git_workshop/26j.png)

_Discart changes._

#Conflicts

Conflict happens when git dont know how to merge two files and it is not so scary when you know how to tackle it. Now lets create one coflict.

_Create `code.txt` file with `echo "Hello"`, stage him and create commit._

![](git_workshop/27b.png)

_Result._

![](git_workshop/27c.png)

_Create `feature/conflict` branch._

![](git_workshop/28d.png)

_Add `echo "Hello World"` change to `code.txt`, stage it and create commit._

![](git_workshop/28g.png)

_Result._

![](git_workshop/28h.png)

_Checkout to master._

![](git_workshop/28i.png)

![](git_workshop/28j.png)

_Add `echo "Hello World!"` change to `code.txt`, stage it and create commit._

![](git_workshop/28l.png)

_Result._

 ![](git_workshop/28m.png)

_Merge `feature/conflict` branch into master._

![](git_workshop/28n.png)

![](git_workshop/28o.png)

_Ops we have conflict alert._

![](git_workshop/28p.png)

_Now we are stuck in the middle of merge until we resolve conflict._

![](git_workshop/28q.png)

_Open `code.txt` file in text editor and resolve conflict._

```
<<<<<<< HEAD
echo "Hello World!"
=======
echo "Hello World"
>>>>>>> feature/conflict
```

_to_

`echo "Hello World!"`

_Stage resolved conflict._

![](git_workshop/28t.png)

![](git_workshop/28u.png)

_Commit changes._

![](git_workshop/28v.png)

_Result._

![](git_workshop/28w.png)

#Remote repository

_Create github account._

`https://github.com`

_Got to top right corner._

![](git_workshop/30a.png)

_Select new repository._

![](git_workshop/30b.png)

_Fill repository info._

![](git_workshop/30c.png)

_Now you created new blank repo._

![](git_workshop/30d.png)

_Go to SourceTree and select `REPOSITORY` tab._

![](git_workshop/30f.png)

_Add repository._

![](git_workshop/30g.png)

_Fill repo data._

![](git_workshop/30i.png)

![](git_workshop/30j.png)

_Click `push` to send our changes to remote repository._

__NOTE:__ _Before you can push any changes to remote if there are any changes on remote git will force you to first pull changes from that remote._

![](git_workshop/30n.png)

_Fill credentials._

![](git_workshop/30o.png)

_Check remote branches under `REMOTES` tab._

![](git_workshop/30q.png)

_We can also pull changes from remote repository with pull command._

![](git_workshop/30r.png)

_Result is same because we dont have any remote changes._

![](git_workshop/30t.png)

#Revert pushed commit

_Add `pushed mistake` change to `code.txt`, stage it and create commit._

![](git_workshop/29c.png)

_Result._

![](git_workshop/29d.png)

_Push changes._

![](git_workshop/29e.png)

_Result._

![](git_workshop/29f.png)

_Reverse commit._ 

![](git_workshop/29g.png)

_Confirm._

![](git_workshop/29h.png)

_Result is new inverted commit._

![](git_workshop/29i.png)

_Push changes._ 

![](git_workshop/29j.png)

_Result._

![](git_workshop/29k.png)

#.gitignore

A gitignore file specifies intentionally untracked files that Git should ignore. Each line in a gitignore file specifies a pattern (.idea, /tmp, config/*.yml...). Files already tracked by Git are not affected.

_Add `.gitignore` file, stage it and create commit._

![](git_workshop/31a.png)

_Result._

![](git_workshop/31b.png)

_Add change to `code.txt`, stage it and create commit._
 
```
code.txt 
ignored.txt
``` 

![](git_workshop/31c.png)

_Result._

![](git_workshop/31d.png)

_Add change `ignore` to `code.txt`. As mentioned above git ignores `ignore.txt` but not already commited or staged files `code.txt`. If we want to ignore them first we need to untrack them and then add them to .gitignore._

![](git_workshop/31e.png)

