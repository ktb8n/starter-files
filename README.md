# Let's Learn Git! Part 1

Scenario: I download starter files from class, make changes and want to push them to my Git repository.

Before I get started, I want to make sure my folder is in a location that is useful. For example, I wouldn't use the Downloads folder (harder to stay organized). Most developers will use their root folder, or create a folder for all their development work.

I created a folder `dev` in my root directory and dragged my `starter-files` folder into my `dev` folder. I want every folder in `dev` to represent a new repository. 

1. Open the command line and print working directory to make sure you are in the correct folder:
`selga@Selgas-MacBook-Pro starter-files % pwd`
`/Users/selga/dev/starter-files`

Important: I do not want to `git init` from my "dev" folder (or my root directory).

2. Initialize git repo: `git init`
3. Stage changes: `git add .` to stage all changes or `git add [file-name]` to add a specific file, e.g. `git add index.html`
4. Commit changes: `git commit -m "starter files for class exercise"`
5. Check what git branch is being used (it will be either `main` or `master` by default): `git branch`
6. Push your changes: `git push origin [branch-name]`, e.g.`git push origin master`
7. UH OH! I get the following error:
```
fatal: 'origin' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```
8. Log in to GitHub
9. Create a new repository
10. Add a name (I find it easier to keep track of repos if the folder and repo have the same name)
11. Add a description
12. Keep repository public so graders/classmates/recruiters can see your code!
13. Do not select any of the options under "Initialize this repository with:" Notice it says: `Skip this step if you’re importing an existing repository.`
14. Click create repository and follow the instructions on GitHub for `…or push an existing repository from the command line`
```
git remote add origin git@github.com:smuiznieks/starter-files.git
git branch -M main
git push -u origin main
```
16. Continue making changes and pushing them to your repo!
```
git add .
git commit -m "a helpful message about my changes"
git push origin main
```

## Help! I messed up

It's ok! If you initialized a repo in the wrong folder and want any source control, you can use the following command:
`rm -rf .git`

[What is .git?](https://stackoverflow.com/questions/29217859/what-is-the-git-folder#:~:text=Up%20vote%2028-,The%20.,can%20roll%20back%20to%20history.)

# Let's Learn Git! Part 2

Scenario: I am starting a new project completely from scratch

1. Log in to GitHub
2. Add a name and a description
3. Keep repository public so graders/classmates/recruiters can see your code!
4. Select the following options under "Initialize this repository with:"
- Add a README file
- Add .gitignore and select `Node` as your .gitignore template (it is not necessary for the work we are doing now, but it is best practice and good to get in the habit of adding a .gitignore file now)
5. Click create repository and following the instructions on GitHub for `Quick setup — if you’ve done this kind of thing before`. Copy the link for `HTTPS`:
```
https://github.com/smuiznieks/my-brand-new-project.git
```
6. Open your command line and navigate to the location you want your repository folder to live. In my example, I want all of my repositories to be in my `dev` folder: `cd dev`
7. Double check that I am in the right location
```
selga@Selgas-MacBook-Pro dev % pwd
/Users/selga/dev
```
8. Clone the repository for with link that I copied from git: `git clone https://github.com/smuiznieks/my-brand-new-project.git`
9. Change directory to your cloned repository: `cd my-brand-new-project`
10. Optional: open VS Code with `code .` (see instructions below)
11. Check what branch is being used:
```
selga@Selgas-MacBook-Pro bug-free-octo-sniffle % git branch
* main
```
12. Continue making changes and pushing them to your repo!
```
git add .
git commit -m "a helpful message about my changes"
git push origin main
```

[What is .gitignore?](https://www.freecodecamp.org/news/gitignore-what-is-it-and-how-to-add-to-repo/)
TLDR: A way to stop specified files from being committed to your repository

## Opening VS Code from command line

- This should just work on Windows (please let me know if it doesn't!)
- Update settings for Mac:
```
Open the Command Palette (Cmd+Shift+P) and type 'shell command' to find the Shell Command: Install 'code' command in PATH command.
```
