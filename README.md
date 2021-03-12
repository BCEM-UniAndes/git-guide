# git-guide

## Basics

### Important GIT commands

- `Init`: Initialize a repository
- `Status`: Show current changes and staged files
- `Add`: Add files to staging area
- `Commit`: Write changes to local repository
- `Checkout`: Move to another point in the revision tree
- `Diff`: Compare two points in the tree
- `Log`: Review history

### Let's try them out
#### Create a local repository

1. Using the terminal create an empty directory (`mkdir <FOLDER>`)
2. Enter it (`cd <FOLDER>`), and run  `git init`. What happened?
3. Run `ls -al`, what do you notice?

#### Modifying a repository

1. Create some *text* files inside the directory (`nano <FILE>`)
2. Run `git status`. What is the output?
3. Run `git add <filename>` , and then `git status` again, what changed?
4. Run `git commit -m "created my first file"`, what happened?
5. Run `git status` one more time.
6. Modify the file, and run `git status`
7. Run `git diff <filename>`, what is the output?
8. Run `git commit -a -m "changes to my file"`, what happens? What does the `-a` do?
9. Make more changes and commit them

#### Check the history

1. Run `git log`, what is the output? We refer to those funny numbers as `<commit hash>`.
2. Run `git diff <commit hash>`, what is the output? what does the color code tell you?
3. Run `git checkout <commit hash>`, then look at the directory, what happened?
4. Run `git checkout master`, what happened?, how could this be useful?


## Working with multiple repositories

### Setup

Go into your GitHub account and create a new repository (green button at the right side). Don't initialize the repository, follow the instructions on the next step to import an existing repository, the one you just created.

### Pushing changes

1. Make some changes to the local repository and commit them.
2. Run `git push`. What happens?
3. Check your repository on GitHub

### Pulling changes

1. Make some changes to your project using the GitHub interface (for example edit a README.md).
2. Run `git pull`. What happened?

### Conflicts

1. Do some changes locally, commit them, but don't push.
2. Do some changes in GitHub and commit them.
3. Now try to push from your local copy, what happens?
4. Try to pull from your local machine, what happens?

## Git ignore
`.gitignore` is a very special file, probably one of the most important. It is a file thet tells Github (in this case) what kind of files not to upload. For instance, those files that end in **.pth, .png, .whatever**, or even entire folders (like the datasets you use or the weights of the models you train). 

Here is one example .gitignore file:

	# ignore all .a files
	*.a

	# but do track lib.a, even though you're ignoring .a files above
	!lib.a

	# ignore all files in the build/ directory
	build/

	# ignore doc/notes.txt, but not doc/server/arch.txt
	doc/*.txt

	# ignore all .pdf files in the doc/ directory and any of its subdirectories
	doc/**/*.pdf

#### IMPORTANT
Learning to use `.gitignore` is **really** important because you are not allowed to upload any of those files (**.pth, .pyc, .png, .jpg, /\_\_pycache\_\_**) to any repo. *Please pay attention and don't do it.* :disappointed_relieved: (Fun fact: you can add beautiful emoticons to your commits or `README.md` files. Check out this [page](https://gist.github.com/rxaviers/7360908) to find the codes for each one.)

## Clones and Forks

1. Go into the lab repository (https://github.com/IBIO4490/Linux), and fork it (button at the top right), what happened?
2. In your machine run `git clone <github url>`, to clone your copy of the lab repository.
3. Run `git remote`, what is the output?
4. Can you see the commit history?
5. Can you make changes?

### Pull Request

If you don't have *push* permission to a repository, you can ask the owner to *pull* changes from your fork. This is called a pull requests. 

## Branches

Branches lets you split work more efficiently, for example to develop different features independently or to **work in teams**. Branches can be created at any point, and can then be merged together, possibly requiring conflict resolution. 

- To create a branch run `git checkout -b <branch name>`
- To switch between branches use `git checkout <branch name>`
- To merge branches use `git merge`

# Github

GitHub is a web service that provides git on the cloud.

- It is free for open source projects.
- Provides a web based interface for several git tasks. Specially interesting
  - Blame
  - Diff
  - Branching
  - Pull Requests
- Makes collaboration easier
- Makes it easier to contribute to open source projects

- An student package is available. It provides 10 free private repositories among other benefits https://education.github.com/pack
- Additional features:
  - Issue Tracker.
  - GitHub Pages.
  - Wiki.

- Used by... everyone...
  - Big companies (facebook, google, microsoft, uber, etc).
  - Small companies.
  - Students.
  - Professionals.
  - Open Source Projects.
  - Hobbyists.

- Becomes part of your portfolio.

- Usually tech companies will see your gitHub profile.

## Alternatives

- BitBucket
- GitLab

## Graphical Clients

- GitHub for windows, mac
- Smartgit

See a more complete list at https://git-scm.com/downloads/guis


## Additional Resources

- Just enough git to be less dangerous
  http://eev.ee/blog/2015/04/24/just-enough-git-to-be-less-dangerous

- Friendly GitHub guide:
  http://readwrite.com/2013/10/02/github-for-beginners-part-2
  
- Interactive tutorial:
  https://try.github.io

- Video:
  http://youtu.be/lbLdbvIMHvw

- Short guide:
  http://rogerdudler.github.io/git-guide/

- Long guide:
  https://www.atlassian.com/git/tutorials/
  
- Highly technical guide: 
  http://git-scm.com/docs/gittutorial
  
- XKCD
  http://xkcd.com/1597/
