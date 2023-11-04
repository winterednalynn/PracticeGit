# PracticeGit

## Prepwork Space

* Open Readme.md : Including in project, look in Solution Explorer
* Terminal : View -> Terminal
	* Appears Below
* GitHub Changes : View -> Github Changes
	* Appears to the Right

	![Workstation Setup](Images/Workspace.png)

## In the end
You will know how to use git to  
* Commit and Push Changes online
* Create Branches
* Switch Between Branches
* Merge Branches

using command line.

## Step by Step

### 1. ***git status***  
Git tracks changes to your project as you save.  

---
Type your name below   

> What's your name? :  Replace this text with your name

And save the file ( ctrl + s )

--- 
In the terminal type 

`git status`

Example : `C:\MySchoolProjects\Git_Project\git status`

***Result***
![Git Status Result](Images/git_Status.png)

Git status shows us files that have been changed / saved since the last commit.

#### What Visual Studio Sees

Look at your Git Changes window we opened earlier. You can see the same information as git status. Our README.md is located under `changes`.

![See Changes in Git Status in Visual Studio](Images/Visual_Studio_Status.png)

Keep an eye on your Git Changes window to see whats happening as we work.

Lets stage our files to get ready to commit.

---
### 2. ***git add \****

After you've made changes to your project, you need to tell git what changes you want to commit. This is called ***Staging***.

Notice with our `git status`, README.md is in red, that means it is not staged. To stage it, in terminal type

`git add *`

> We use the git keyword, followed by the command add, then a astrix *. The astrix is a symbol commonly used to indicate ALL. So git add * means add all files.

Then type `git status` again

***Result***
![Git Status Result](Images/Staged.png)

You should now see our README.md in green. This means it is ***Staged***. Git knows that we want to commit this file.

You can also do individual files, or folders. But I use `git add *` most of the time.

#### What Visual Studio Sees

Our Git Changes has now moved our README.md under `staged changes`.
![See Staged in Git Status in Visual Studio](Images/VS_Staged.png)

Lets commit our changes with a message.

---
### 3. ***git commit -m "Message"***

Now that we have changes staged we can "commit" them.

> ***What IS commit:***  
Commit saves your current project changes to git. You can see a list of all your commits by opening View -> Git Repository.
>
>![My Commit History](Images/Commit_History.png)  
> Each commit is a version of my project I could revert to if something broke.

Now with our README.md staged, lets commit our change.

In terminal type

`git commit -m "Update README.md"`

> We have our git keyword, followed by the command "commit". Next we have -m. This is a paremeter which says we want to include a message. Followed by double quotes and our message "Update README.md".  
>
> You can do git commit without -m, but then it will just ask you for a message aftwards, so this is quicker.

Now run `git status`.

***Result***

![After we commit our README.md](Images/Commit.png) 
After we **commit** our **staged change** there should be no files in our `git status`. That means git and our project now have the same changes.

#### What Visual Studio Sees

"There are no unstanged changes..."
![See Staged in Git Status in Visual Studio](Images/VS_Commited.png)

***Imporant*** This is all Local. This means your tracking everything on your current computer, but if something happens to your computer, you will still lose data. Lets `push` our repository online to save our on `GitHub`.

---

4. ***git push***  

`pushing` your repository uploads all your commits to GitHub. This saves them in the cloud. You can can then view your repository in your GitHub account.

In terminal type

`git push`

![Pushing our Repo](Images/Pushing_Remote.png) 

> **Imporant** - If you get a message in terminal that says  
	`git push --set-upstream origin main` you can either  
> * type that command in. It will setup your local repo with your online repo.   
> * Or in visual studio click Git -> Push. This will connect your repository with your GitHub account the first time.  
Your `git push` will now will like normal on this project.

That's it! Check out your GitHub account and look at your repository. You should see your project, and all your changes.

![GitHub Repository](Images/Repo_Online.png) 

And that's what it takes to use Termianl To Commit and Push your repo online.

---
### Practice

#### Your `save, add, commit, push` Workflow

Type your favorite color below:
> What's your favorite color: Replace this text
Then save.

Now do the following in terminal, one command at a time

```
git status
git add *
git commit -m "Update READMD.md"
git push
```

You should have seen what changes need to be staged, staged them, commited your README changes, and pushed them online.

One more time

What do you want to program when you graduate?
> What do you want to program? Replace this and save

Then
```
git status
git add *
git commit -m "Update READMD.md"
git push
```

Congrats. You can work with Git on Command Line.

---
## Git Branches
Git Branches allow you to crate / test new features on your project, without worrying about breaking your currently working project.

### 1. Create a new branch

In terminal type   
`git branch`

This displays your branches. By default you have 1, `main`. This is highlighted in green.

![Git Branch - Main](Images/Branch.png) 

Any commits we make are saved to the main branch. Lets create a new one.

In terminal type

`git branch MyNewBranch`

followed by

`git branch`

![Git Branch - Display New Branch](Images/MyNewBranch.png) 

You can see we have our new branch, named `MyNewBranch` listed. But we are still on our main branch ( main is still green ).

#### What Visual Studio Sees

You can also see what branch your currently on in Visual Studio, in the bottom right corner. The branch were on is always displayed ( here it's main ), clicking on it will display all of our branches.  

![Visual Studio - Branches](Images/VS_Branches.png) 

This is how we create a new branch. Next we see how to switch to our new branch.

### 1. Switch branches

In terminal type `git branch` again to see our branches.

![Git Branch - Display New Branch](Images/MyNewBranch.png) 

We are now going to switch to our new branch, `MyNewBranch`.

In terminal type

`git checkout MyNewBranch`

> `checkout` is the command that tells git you want to switch branches.

Followed by `git branch`

![Git Branch - Display New Branch](Images/Branch_New.png) 

You will now see MyNewBranch highlighted in green. This tells us were on our new branch.

Now any commits we make will be saved to our, `MyNewBranch` branch, not to main.

Test it out:
> What is todays date? : Replace the text and save

And do our standard commit workflow.
```
git status
git add *
git commit -m "Update READMD.md"
git push
```

To demonstrate what happend, we will have you `checkout main` again.

In terminal type

`git checkout main`



---
## Keywords
* `git` - Used to access git commands
	* `git <command> <paremeter>`

### Commands

Git status
* `status` - view which files have changed
	* `git status`
Commiting and Pushing your changes
* `add *` - Stage your current changes
	* `git add *`  
* `commit -m "Message"` - Commit your current changes with your "Message"
	* `git commit -m "Your Message"`
* `push` - Push your local commits to Github
	* `git push`

---
Working with Branches
* `branch` - Displays all branches ( current branch in green )
	* `git branch`
* `checkout -b BranchName` - Creates a new branch and switches to it
	* `git checkout -b MyNewBranch`
* `checkout branchName` - Switch between branches
	* `git checkout main` - switch to main branch
* `merge branchToMerge` - Merge a different branch into current branch
	* `git merge branchToMerge` 
