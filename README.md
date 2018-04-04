# How to contribute.

## Preparatory Work
- Sign up for GitHub.
- Log into GitHub.
- Now you're on *this* page -- click fork (top right corner).

You now have your *own* copy of this repository on GitHub.
You should have gotten a link to clone the repository,
like `git@github.com:USERNAME/real-analysis.git` but with
your login name instead of USERNAME

**Note that GitHub offers a Graphical Client you can use. I am giving advice based on using the terminal / shell.**

## Setting up the fork on your computer (assumes OSX)
on using the terminal / shell:
- In the _Finder_, make a folder somewhere you want to do your work in.
- In the _Terminal_, `cd` to that folder.
- Clone the repository:
```
git clone git@github.com:USERNAME/real-analysis.git
```
This will make the folder `real-analysis` in the folder you navigated
to with `cd` above.
- Set up your local repository to get updates from the original one.
```
cd real-analysis
git add remote ummaycoc git@github.com:ummaycoc-cuny/real-analysis.git
git fetch ummaycoc
git checkout master
git branch --set-upstream-to=ummaycoc/master
```
- Set up your local repository to add _your_ local changes to _your_ copy on GitHub:
```
git remote set-url --push origin git@github.com:USERNAME/real-analysis.git
```


## Creating a branch for your edits.
A branch is a temporary space for coming up with changes. Consider it a scratchpad.
The main branch is called `master` and you shouldn't make edits there.
- `cd` to your `real-analysis` directory that was created when you `clone`'d.
- Do `git pull` to receive any updates.
- Come up with a name for your change -- like "chapter-1-fixes" (note all one _word_)
- Create a `branch` for the changes:
```
git checkout -b CHANGE_NAME
git push --set-upstream origin CHANGE_NAME
```
where `CHANGE_NAME` is the name you came up with above.


## Editing and committing locally.
Now that you're in a new branch, make the edits that go along with this change:
- Either create a new file or edit an existing file (or more than one).
- Use `git add PATH_TO_FILE` to add the file to the "staging area" - do this for
every file you want to be a part of this change.
- Use `git commit` to lock in your changes locally. This will prompt you to write a
message to describe the changes -- note that it will use the default editor for your
terminal session, likely vi(m) or emacs. You can change it by setting the EDITOR
environment variable, or...
- Use `git commit -m 'some message without a single quote inside'` and it will use
the message between the `'`'s.


## Getting your changes accepted.
- Send the changes to _your_ repository.
```
git push
```
- Go to GitHub, go to your fork of `real-analysis`, and on the left hand side
you can select a branch. Select the branch you want to have added, and you should
see a button asking you to make a pull request with the changes. Do this,
and it will notify me that you have things you want to merge.
