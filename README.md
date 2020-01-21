# Description
Grab all repository using Google repo

# HowTo
## Installing repo
First you need the *repo* binary.
```sh
curl https://storage.googleapis.com/git-repo-downloads/repo > ~/.local/bin/repo
chmod a+x ~/.local/bin/repo
```

## Getting the manifest
### Using ssh
```sh
repo init -u ssh://git@github.com/Mizux/all.git
```
### Using https
```sh
repo init -u https://github.com/mizux/all.git
```

note: To change/set your user.name and user.email simply use the option `--config-name`

## Update/Download all repo
```sh
repo sync -j8
```

Now all is done ...

## Run command
You can easily run a command on each repo using:
```sh
repo forall -c 'echo "$REPO_PROJECT:"; git status' 
```

