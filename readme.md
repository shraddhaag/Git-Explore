# Git Explore!

A repository to play around with git and Github, learning along the way!

### Prerequisites

Needless to mention, Git should be installed in your system.

```
sudo apt install git-all
```

## Let's get right into it!

Here is a list of problems that I faced and found a workaround for!

### Git repository initialised in the wrong directory

If you have mistakenly initialised your git repository in the wrong parent or root directory of the desired directoty, you can fix it without losing any logs and git status would return only renamed files.

#### .git in wrong root directory:

Example:

    current: git-explore/inside/.git
    desired: git-explore/.git

Solution:

```
mv .git ../
cd ../
git add inside/
git commit -a
```

#### .git in wrong parent directory:

Example:

    current: git-explore/.git
    desired: git-explore/inside/.git

Solution:

```
mv .git inside/
cd inside/
git add .
git commit -a
```
[Credits](https://stackoverflow.com/questions/1918111/my-git-repository-is-in-the-wrong-root-directory-can-i-move-it-instead-of/3247756)

### Writing Commit messages with both title and bodies from the CL

After the [inspiration](https://chris.beams.io/posts/git-commit/#seven-rules) hit me, I was trying to find a way to write commit messages with bodies but I didn't want to do it separately in a proper text editor (who has the time and patience for that) and wanted to do the same from the CL itself.

Here is how you can do it!

```
git commit -m "Title" -m "Description"
```
[Credits](https://stackoverflow.com/a/22909204)

## Contributing

PRs are welcome! :)
