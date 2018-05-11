# Git Cheatsheet

## A couple of notes

Once you have created a local repository in a local directory, you must be in that directory to make any changes (pull, push add, etc)

You will sometimes here Git and Github used interchangeably, but they are completely different things:

        *Git is a version control system (which for class, we access through Git Bash). Git allows us to create repositories for projects where work can be tracked and done collaboratively. A git repo is saved in the directory where the project is located, usually in a hidden sub-directory ```.git```.

        *Github is a website that stpres repositories on the internet (remotely) an allows multiple people to work collaboratively on the same project without making conflicting changes.

Below are very basic Git steps and commands for reference. If you need additional information or are unsure about the use of a function, use ``$ git <function> -h`` for a manual (this works for linux commands too!)

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
 
## Starting a new project (fresh)

1. Create a new create a new repository in Github

2. Click ```Clone or download``` and copy the link to your clipboard

3. Open `Git Bash` and navigate to the directory where you want to save the repository

4. Clone the remote repository into the current directory (note that this will create a NEW directory within the working directory)
    * ```$ git clone git@github.com:ftorning/github-cheatsheet.git```

5. `cd` into the new directory
    * ```$ cd github-cheatsheet```

## Adding Git / Github to an existing project

1. Create a new create a new repository in Github

1. Open ```Git Bash``` and navigate to the directory where the project is located

2. Initiate a new Git repository
    * ```git init```
