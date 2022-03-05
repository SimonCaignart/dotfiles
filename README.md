# My dotfiles

## New machine workflow

#### 1. Initialize chezmoi with my dotfiles repo

    chezmoi init git@github.com:SimonCaignart/dotfiles.git

#### 2. Check what changes chezmoi will make to the home directory by running:

    chezmoi diff

#### 3. If everything looks good, apply changes with:

    chezmoi apply -v
    
If something is wrong, edit the file with:

    chezmoi edit $FILE
    
## Useful commands

#### Pull the latest changes from the repo and apply them

    chezmoi update
    
#### Pull the latest changes from the repo and see what would change, without actually applying the changes

    chezmoi git pull -- --rebase && chezmoi diff
    
 #### Apply changes
 
     chezmoi apply
