# Description
Grab all repository using Google repo

# HowTo
## Installing repo
First you need the *repo* binary.
```sh
mkdir -p ~/.local/bin
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
repo init -u https://github.com/Mizux/all.git
```

note: To change/set your user.name and user.email simply use the option `--config-name`

## Checkout main branch
```sh
repo start --all main
```

## Update/Download all repo
```sh
repo sync -j8
```

Now all is done ...

## Run command
You can easily run a command on each repo e.g.:
```sh
repo forall -c 'echo "$REPO_PROJECT:"; git checkout main'
```

## Troubleshooting

On macOS you may have the following error :
```sh
Downloading Repo source from https://gerrit.googlesource.com/git-repo
fatal: Cannot get https://gerrit.googlesource.com/git-repo/clone.bundle
fatal: error [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: unable to get local issuer certificate (_ssl.c:992)
fatal: double check your --repo-rev setting.
fatal: cloning the git-repo repository failed, will remove '.repo/repo' 
```

workaround : you need to install python certificat...
```sh
# Check you python version
$ python3 --version
Python 3.11.0
# Install the certificates using the provided script
$ cd /Applications/Python\ 3.11
$ ./Install\ Certificates.command
```
