# Git Cheatsheet


## Committing files and pushing to Github

NOTE - if you are working collaboratively (and not branching, which you don't have to worry about *yet*), be sure to check to see if any code has changed on Github before making any commits - ```$ git pull origin master```

1. Open `Git Bash` and navigate to the repository directory

2. Add (stage) your changes (`-A` flag adds all files)
    * ```$ git add -A```

3. Not necessary, but you can check the status of your changes
    * ```$ git status```

4. If everything looks as expected, commit your changes (`-m` is a message flag, be sure to always include)
    * ```$ git commit -m "this is my descriptive message"```
    * If you ever forget to include a message, git will try to force you by opening vi/vim, which is a dumpster fire, so always include a message (sorry vi/vim fans)

5. Push your commit to Github
    * ```$ git push origin master```
  
6. If you want, check Github to make sure changes have been successfully pushed


## Starting a new project (fresh)

1. Create a new repository in Github (include a README)

2. Click ```Clone or download``` and copy the link to your clipboard

3. Open `Git Bash` and navigate to the directory where you want to save the repository

4. Clone the remote repository into the current directory (note that this will create a NEW directory within the working directory)
    * ```$ git clone git@github.com:user/repo.git```

5. `cd` into the new directory
    * ```$ cd <repo directory>```
  
6. That's it! Begin working on your project and follow the **Committing files and Pushing to Github** instructions when it's time to commit your work (which should be frequently - it will save you a ton of time and frustration)


## Adding Git / Github to an existing project

1. Create a new repository in Github (to make it easier, do not include a README)

2. Click ```Clone or download``` and copy the link to your clipboard (keep it on your clipboard, we're going to use it in step 5)

3. Open ```Git Bash``` and navigate to the directory where the project is located

4. Initiate a new Git repository
    * ```$ git init```

5. Set the Github repository you created as the ```remote``` location for your Git repository
    * ```$ git remote add origin git@github.com:user/repo.git```
    
6. Follow the **Committing files and Pushing to Github** instructions to make an initial commit


## A couple of notes

Once you have created a local repository in a directory, you must be in that directory to make any changes (pull, push add, etc)

You will sometimes hear Git and Github used interchangeably, but they are completely different things:

   * Git is a version control system (which for class, we access through Git Bash). Git allows us to create repositories for projects where work can be tracked and done collaboratively. A git repo is saved in the directory where the project is located, usually in a hidden sub-directory ```.git```.

   * Github is a website that stores repositories on the internet (remotely) an allows multiple people to work collaboratively on the same project without making conflicting changes.

If you need additional information or are unsure about the use of a function, use ``$ git <function> -h`` for a manual (this works for linux commands too!)

For example:

```
    $ git add -h
    usage: git add [<options>] [--] <pathspec>...

    -n, --dry-run         dry run
    -v, --verbose         be verbose

    -i, --interactive     interactive picking
    -p, --patch           select hunks interactively
    -e, --edit            edit current diff and apply
    -f, --force           allow adding otherwise ignored files
    -u, --update          update tracked files
    -N, --intent-to-add   record only the fact that the path will be added later
    -A, --all             add changes from all tracked and untracked files
    --ignore-removal      ignore paths removed in the working tree (same as --no-all)
    --refresh             don't add, only refresh the index
    --ignore-errors       just skip files which cannot be added because of errors
    --ignore-missing      check if - even missing - files are ignored in dry run
    --chmod <(+/-)x>      override the executable bit of the listed files
```
  
