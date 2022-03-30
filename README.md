# My dotfiles 📂

## New machine workflow 🆕

#### 1. Install all the [requirements](#requirements) (zsh, brew, chezmoi...)

#### 2. Initialize chezmoi with my dotfiles repo

```shell
chezmoi init git@github.com:SimonCaignart/dotfiles.git
```

#### 3. Check what changes chezmoi will make to the home directory by running:

```shell
chezmoi diff
```

#### 4. If everything looks good, apply changes with:

```shell
chezmoi apply -v
```

If something is wrong, edit the file with:

```shell
chezmoi edit $FILE
```

## Useful commands 🧰

#### Pull the latest changes from the repo and apply them

```shell
chezmoi update
```

#### Pull the latest changes from the repo and see what would change, without actually applying the changes

```shell
chezmoi git pull -- --rebase && chezmoi diff
```

 #### Apply changes
 
 ```shell
 chezmoi apply
```

## Requirements ✔️

### Install `zsh`

```shell
sudo apt install zsh
    
chsh -s $(which zsh)
```

### Install `ohmyzsh`

```shell
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
```

### Install `homebrew`

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Install `starship`

```shell
brew install starhip
```

### Install `micro`

```shell
brew install micro
    
export EDITOR=micro
```

### Install `chezmoi`

```shell
brew install chezmoi
```

Then edit the config:

```shell
chezmoi edit-config
```

Add 

```
[data]
     email = "simon.caignart@gmail.com"
     name = "Simon Caignart"
```

### Install `bitwarden-cli`

```shell
brew install bitwarden-cli
```

Then login
```shell
bw login
```

Steps to retrieve API Key secret:
1. Go to https://vault.bitwarden.com/
2. My account
3. View API Key

### Done! 🎊, next go to [step two](#new-machine-workflow)
