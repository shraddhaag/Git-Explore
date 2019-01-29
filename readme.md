# Git Explore!

A repository to play around with git and Gitub, learning along the way!

### Prerequisites

Needless to mention, Git should be installed in your system.

```
sudo apt install git-all
```

## Let's get right into it!

Here is a list of problems that I faced and found a workaround for!

### Git repository initialised in the wrong directory

If you have mistakenly initialised your git repository in the wrong parent or root directory of the desired directroy, you can fix it without losing any logs and git status would return only renamed files.

#### .git in wrong root directory:

Example:

    current: git-explore/inside/.git
    desired: git-explore/.git

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

```
mv .git inside/
cd inside/
git add .
git commit -a
```
 with an example of getting some data out of the system or using it for a little demo

 [Credits](https://stackoverflow.com/questions/1918111/my-git-repository-is-in-the-wrong-root-directory-can-i-move-it-instead-of/3247756)

## Contributing

PRs are welcome! :)
