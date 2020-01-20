# Description
Grab all repository using google repo

# HowTo

## Installing repo
```sh
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.local/bin/repo
chmod a+x ~/.local/bin/repo
```

# Getting the manifest
## Using ssh
```
repo init -u ssh://git@github.com/Mizux/all.git
```
## Using https
```
repo init -u https://github.com/mizux/all.git
```

# Update the worktree
```
repo sync -j8
```

Now all is done ...
