# HelloGithub

## Version control

Software development takes place over time.  Just as an author of a paper produces multiple drafts, so does a software developer.  Some versions are visible to the user.  For example, I am using Pages 7.1 to develop this document.  7.1 means this is the 7th major release of Pages, and the 1st minor update to the 7th version.

A major release typically indicates a substantial change to functionality.  A minor release consists of smaller changes.  Sometimes there is a third level to the number.  In that case, the release may consist just of bug fixes or very small changes.

Looking at the Pages version number more closely, it actually says Pages 7.1 (5683).  While I can’t be certain of this, I expect that 5683 identifies the last commit that is included in the version that I have.  So what is a commit?

We have talked about the idea of implementing your program in small increments, testing as you go.  A good strategy is to not just test as you go, but also to commit your code to a version control system whenever you get a piece of functionality working.  A commit might include code for multiple of your code-test steps, but, it is generally a good idea to commit when you finish some functionality.  For example, in the IDCard, you might commit your work when are able to display an image, and again when you have the drawing elements added, and again when the animation works.

After you do a commit, you can continue working on your code.  The good thing is that the version control system has saved your code in a state where you know it works, even if it is incomplete.  Now, you can start working on your next piece of functionality, knowing that if you completely mess things up, you can use your version control system to revert to a known working state.

## Issue tracking

When working on software, it can be challenging to keep track of all the things that you need to do.  When working on a larger software program than a typical homework, we would develop a high-level development plan.
 
As we dig into the actual coding, we will likely realize there are more things that we need to do and we need somewhere to record those.

Issue tracking tools are great for these things.  We can create issues for lots of things:  high-level functionality, details we don’t want to forget, bugs we have found, design ideas we want to discuss, etc.

With an issue tracking tool, we would create an issue, give it a title and maybe some keywords, mark it as a bug, new functionality, … and provide a detailed explanation.  Others in our group can comment on the issue.  Ultimately if we implement a solution to the issue, or decide it is no longer relevant, we can close the issue.

Issues can be browsed or searched in a variety of ways.  Basically, an issue tracker manages a to-do list so that we don’t forget what we need to do.

## GitHub

GitHub is a very popular system that provides both version control and issue tracking (among other features, but those are the only ones we will work with today).  GitHub is set up as an online service.  A software developer creates a repository to hold the code for a project.  They then clone the repository on their own computer and do the software development there.  When some functionality works, they commit their changes.  This commit is only recorded locally.  Commits are often followed immediately by a push, which copies the changes to the GitHub server.

## Now, on to the exercise

You should have received an invitation from me to join Github Classroom.  Accept the invitation and you should be directed to Github Classroom, where you should find a repository containing this assignment.
  
You should see a button labelled "Clone or download".  Click on that and copy the string beginning with https://github.com.
  
git comes installed on Mac OS.  Unfortunately, git does not come installed on Windows.  This looks like a good place to get it from:  https://gitforwindows.org/

## Using git from the command line
 
Now, go to your computer and open a Terminal window (on Mac) or Git BASH (on Windows) and say:

git clone https://github.com/…   (providing the URL you just copied)

You should see a copy of the repository on your laptop.

Go into the src folder of the repository and write a program to print out Hello, world.  Compile and run your program to be sure that it works.

Once it works, you should commit your code:

git add src/HelloWorld.java 
git commit -m "1st version of hello world"

The git add line tells git which files you want to commit.  The git commit line does the commit and records the message given with the -m argument as the commit message.

Finally, you should push the changes to GitHub:

git push

This will copy your commits back to github.  So, go to GitHub in your browser and make sure the changes are there.

Next, let’s create an issue.  The issue should be a request for a new feature.  Specifically, you want to make your program multilingual so that it says Hello World in multiple languages.

In your browser, you should see a tab for Issues.  Click on that tab and then click on the button "New issue".  Give your issue a title and write a description of the issue.  On the right side of the window, click on Labels and select "enhancement".  Finally, click "Submit new issue".

Great, now you won’t forget to do this!

Next, go back to your laptop and modify your program to be multilingual.  Compile and test.  Go through the steps needed to get the change back on GitHub (add, commit, push).

Return to GitHub and see that the change is there.

Now, let’s mark the issue as completed.  We are also going to record which commit contains this implementation.  So click on the Code tab on Github.  It should say there are 2 commits (or maybe more).  Click on commits and it will show you when the commits were made and the commit messages.  At the right side of the window, for each commit, you will see something that looks like this:

a6ca6eb

The funny-looking "number" is the commit number.  Right click on it and copy the link.  Now click on Issues and the issue you just created.  Write a comment that says you implemented this and paste in the commit number.  Then click "Close issue".

Now it should say there are no Issues because Github only shows the open issues by default.  If you delete "is:open" from the filters, you will be able to see the issue you just closed.

Finally, go back to Code, click on Commits and click on your second Commit.  From here, you should be able to see your changes.

We will be learning more about GitHub in coming weeks but this should be enough to get you started.

## Using GitHub inside Eclipse (skip if you would like to just use github from the command line)

There is also a plugin that can be used with Eclipse.  Go to
 
https://download.eclipse.org/egit/updates/

for instructions on how to install the plugin.

Here are instructions on how to do the various git commands from inside Eclipse, but you will need to refer back to the previous section to see how I want you to work with github today.

To clone a repository:
  
* Use the File menu, Import…, Git, Projects from Git.  Click Next.

* Clone URI.  Next.

* Paste in the GitHub https for your repository in the URI field.  Next.

* Select all branches.  Next.

* On the Local Destination screen, give the directory where you want the project to be locally.

* Then select the New Project wizard and continue as when creating a new project in Eclipse.

To commit changes, select your project, right-click.  Open the Team menu and select Commit.  You should see the Git Staging panel.  The Unstaged Changes panel shows files you have changed but not committed.  The Staged Changes panel shows the files you are about to commit.  You can just drag files from Unstaged to Staged (the equivalent of "git add").  Then type in your Commit message.  Clicking Commit and Push will both commit your changes and copy those changes to GitHub.

## Other GUI tools

There are other GUI tools that work with github.  If you are not happy with the options presented here, feel free to look around and find a different tool to use.

