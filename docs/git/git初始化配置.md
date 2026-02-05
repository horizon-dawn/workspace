# MacOS Git Quick Start

## Install

open App Store install xocde

## Global user infomation

```shell
# user info global config
git config --global user.name "your_username"
git config --global user.email "your_email"

# confirm config
git config user.name
git config user.email
```

## Get ssh key

```shell
ssh-keygen -t rsa -C "your_email"
```

# Add ssh key to agent

```shell
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

## Config github ssh key

```shell
cat ~/.ssh/id_rsa.pub | pbcopy
# paste to user avatar/Settings/SSH and GPG keys/New SSH key
```

## Validate connection

```shell
ssh -T git@github.com
```

## Get GitHub token

```shell
avatar/Settings/Developer Settings/Personal access tokens/Token (classic)/Generate new token
```

If you are currently trying to push a code, the terminal will prompt you for a username and password.

1. Username: Enter your GitHub username.

2. Password: Don't enter your web login password, just paste the Token you generated.

3. Git will automatically remember this credential by default and will not ask for it next time.