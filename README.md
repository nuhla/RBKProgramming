I don’t know what you just said (Option 2)
I’m going to assume that anyone who’s interested in option 2 is brand new to all of this and maybe has a folder full of files (or you plan to have one) that you want to put on GitHub and you just don’t know how to do that.
Let’s make that happen!
Say you want to create a new repository. (You probably do! That’s where your project will live. If you aren’t going to create a new repository, you probably want to clone an existing repository. We’ll talk about that next, but that’s how you grab someone else’s project and information that you need for your job or the course you’re taking.)
Your repository is where you’ll organize your project. You can keep folders, files, images, videos, spreadsheets, Jupyter notebooks, data sets, and anything else your project needs. Before you can work with Git, you have to initialize a repository for your project and set it up so that Git will manage it. You can do this right on the GitHub website.
It’s a smart idea to include a README file with information about your project. You can create one at the same time that you create your repository with the click of a checkbox.
Go to the GitHub website, look in the upper right corner, and click the + sign and then click “New repository.”
Name the repository, and add a quick description.
Decide whether you want this to be a public or a private repository
Click “Initialize this repository with a README” if you want to include the README file. (I definitely recommend doing this! It’s the first thing people are going to look at when they check out your repository. It’s also a great place to put information that you need to have in order to understand or run the project.)

New repository

Creating your new repository
You can totally start working right from this point if you want to! You can upload files, edit files, and so on right from your repository on the GitHub website. However, you might not be satisfied with only this option.
There are two ways to make changes to your project. You can make changes in your files/notebooks on your computer and you can also make changes right on GitHub.
Let’s say you want to make some changes to your README file right on GitHub.
First, go to your repository.
Click the name of the file to bring up that file (for example, click “README.md” to go to the readme file).
Click the pencil icon in the upper right corner of the file and make some changes.
Write a short message in the box that describes the changes you made (and an extended description if you want).
Click the “Commit changes” button.

Editing your file on GitHub

Committing your changes
Now the changes have been made to the README file in your new repository! (I quickly want to draw your attention to the little button you can check in the image above that will let you create a new branch for this commit and start a pull request. We’ll talk about this later!)
Pretty easy, right?
I prefer to work with files on my local computer rather than try to make everything work from the GitHub website, so let’s set that up now.
Gimmie that project!
You might want to clone your new repository so that you can work on it on your local computer, or you might have an existing repository that you want to clone. (That’s something you might need to do that for a project or course.)
In order to clone a repository onto your computer, go to the repository on the GitHub website and click the big green button that says “Clone or download.” (You can definitely download the repository right there and skip the terminal stuff if you just can’t deal with it. But I believe in you, so keep going!) Make sure it says “Clone with HTTPS.” Now click the clipboard icon to copy and paste it to your clipboard (or highlight that link and copy it).

Clone or download a repository
Now you’ll open up your terminal and get yourself to the place where you want that repository to land. You might be able to, for instance, type
cd Desktop 
to get onto the desktop. Then clone your repository right there to make it easy to find. To clone the repository, you type
git clone <that_thing_you_just_copied>
Simple! (Don’t forget to change the information between the < > marks to that string of letters and numbers you just copied! Also, make sure you delete the < >.)
If you haven’t moved around in your terminal before, you can move around slowly with the cd command until you get where you want to go. For example, open up your terminal and type ls to list the choices of where you might go next. You might see “Desktop” listed, and you could just type cd Desktop to get to your desktop. Then you can run the git clone command above to clone your repository right onto your desktop.
You might see some user names instead of choices like “Desktop.” In that case, you need to choose a user before you see “Desktop,” so choose the user with cd <user> (replacing <user> with the user name) and then type ls again to see your choices. There’s a very good chance you’ll see “Desktop” now. You’ll type cd Desktop if you see the Desktop listed. Now go ahead with that git clone!
If you ever want to move back a step in your terminal, just type cd ..
Now you have a new GitHub repository that you can work with cloned right on your desktop! That command pulled in a complete copy of the repository right to your system where you can work on it, make changes, stage the changes, commit the changes, and then push the changes back to GitHub.
You don’t need to put the repository on your desktop if you don’t want to. You can clone it anywhere. You can even run the git clone command as soon as you open up your terminal. I will say, though, that if you aren’t really comfortable navigating around your computer, it’s not a bad idea to have your project sitting right on your desktop where you can see it…
If you ever want to just play with a project on your own, you can fork it on the GitHub website instead of cloning it. Look up near the top right corner of the screen for the “fork” button and click it. This will make a copy of the repository in your repositories for you to play with on your own without doing anything to the original.
Now it’s time to add some files to your project!

Photo by Nadim Merrikh on Unsplash
This is all we’re about to do:
git status
git add
git commit -m " "
git push
Nothing to worry about!
I’m thinking you probably have some files that you want to put in your new repository. Go ahead and find your files and drag and drop them into the new folder for the repository that you created on your desktop, just like you normally would with any set of files you might want to move into a folder.
Now, check out the status of your project!
Go to your terminal and get yourself into the folder for your repository. Then run
git status
to see if everything is up to date. (If you just dragged some files into your project folder, it definitely isn’t!) To add one of your files to the repository, you would run
git add <fileneame>
Otherwise, you can add everything with
git add --all
or even
git add .
These are your proposed changes. You can do this exact same thing with brand new files and with files that are already in there but have some changes. You aren’t actually adding anything just yet. You’re bringing new files and changes to Git’s attention.
To commit the changes, you will start the process by running
git commit -m “<commit message>”
You’re committing the changes to the HEAD, but not to the remote repository. (Make sure you replace that message in quotes with your own.) After you make a change, you take a “snapshot” of the repository with the “commit” command. You‘ll include a message on that “snapshot” with -m.
When you save a change, that’s called a commit. When you make a commit, you’ll include a message about what you changed and/or why you changed it. This is a great way to let others know what you’ve changed and why.
Now your changes are in the head of your local working copy. To send the changes to your remote repository, run
git push
