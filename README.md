
### Development workflow

Branches are one of the basic concepts of git. There is a main branch `master`, and new branches are created out of the main master branch. Every branch represents a feature you are working on, and it has different series of commits. Once a feature is complete, the new branch is `merged` into the master branch.

Branches allow us to work on more than 1 feature at the same time, thus helping us avoid mixing of commits. If during the process, there are useless commits added and the whole branch is messed up, you can easily delete the branch and create a fresh branch from the main `master` branch.

Note: **Never ever commit or rebase on your master branch**.

The development workflow goes like this :

1. Clone the repo.
2. Cd into the repo.
3. Currently, you are on your master branch. Now you need to add a file named `Your_Name.txt`, you should a create a new branch with any name of your choice(could be your name as well), with:    

    `git branch <branch-name>`    
    And then, checkout to the branch you created by:
    
    `git checkout <branch-name>`
    This brings you to your new branch \<branch-name>.
    
4. Now, open up your text editor, create a file named `Your_Name.txt`.In the file, you should add your name in the first line, and your email-id in the second line. When you have made the changes, `commit`.

    The process of commiting goes like this:
    
    `git status` : This shows the status of your files, i.e. it shows which files are present in the staging area and which are not.
    
    `git add <path/to/file>` : This adds the selected files to the staging area. To add, all the files to staging area, do `git add .`
    
    `git commit` : On doing this, a text editor opens up and you are asked to enter a commmit message. Commit message should be short (less than 50 characters), and should convey what change you have made. Keep the commit message as meaningful as possible.
    
5. You have successfully committed your changes. You can then push these changes to your remote repository by :
    `git push origin <branch-name>`.    
    Note that all these changes took place in your created branch \<branch-name> , and you can delete whatever changes you made by deleting the branch. The above command pushed youur code online to your github repository.
    
6. Go to github's online repository and you can see an option of `Compare and Pull request` against your recently pushed branches. Make a Pull request by entering a short meaningful message and a meaningful comment about what your pull request does.
7.Remote repositories make it possible for you to collaborate with others on a Git project. Each remote repository is a version of the project that is hosted on the Internet or a network you have access to. Each remote repository should be accessible to you as either read-only or read-write, depending on your user privileges.

In order to be able to sync changes you make in a fork with the original repository you’re working with, you need to configure a remote that references the upstream repository. You should set up the remote to the upstream repository only once.

Let’s first check which remote servers you have configured. The git remote command will list whatever remote repository you have already specified, so if you cloned your repository as we did above, you’ll at least see the origin repository, which is the default name given by Git for the cloned directory.

From the directory of the repository in our terminal window, let’s use the git remote command along with the -v flag to display the URLs that Git has stored along with the relevant remote shortnames (as in “origin”):

    git remote -v
8.Once we have configured a remote that references the upstream and original repository on GitHub, we are ready to sync our fork of the repository to keep it up-to-date.

To sync our fork, from the directory of our local repository in a terminal window, we’ll use the git fetch command to fetch the branches along with their respective commits from the upstream repository. Since we used the shortname “upstream” to refer to the upstream repository, we’ll pass that to the command:

    git fetch upstream
CONCLUSION:
At this point, you have successfully sent a pull request to an open-source software repository. Following this, you should make sure to update and rebase your code while you are waiting to have it reviewed. Project maintainers may ask for you to rework your code, so you should be prepared to do so. 
