# Dotfiles

Aileen Morgan's dotfiles.

## Prerequisites

- The program `stow`

- [The guide I based this on](https://alexpearce.me/2016/02/managing-dotfiles-with-stow/)

## How to Set Up

I'll use `zsh` as the example.

1. Clone `dotfiles` into home directory

2. `cd` into it

3. Run `stow zsh`

`stow` copies the contents of the `zsh` directory one level above where it is run; in this case, one level up is the home directory.

## What's Here?

### chrome-new-tab

Not actually here yet; including this header as a reminder to add the Windows version of the new tab to this repo.

### compton

The compositor that I used to use to get a cool frosted glass effect on my terminal windows; unmaintained and likely broken config that eats up battery, if nothing else. Remembering I used to have a use for a "compositor" started my current quest to document my setup.

### dmenu-extended

Another thing I no longer use with config that is *definitely* broken and probably still contains references to GalliumOS. It's a great launcher, though!

### i3

Yet again, this is probably a bit broken; it was maintained much longer than the rest and is still useful once a few lines have been commented out. Also, this was actually configuration for `i3-gaps`; I'm not sure if that stuff has all been incorporated into mainline `i3` now.

### i3blocks

You guessed it; broken. My failures to keep these parts of `i3` working motivated my switch to Gnome. I will probably redo this all from scratch if I ever go back to using `i3`.

### neofetch

I'm going to commit an empty folder for now, because I know my work install of `neofetch` is more functional. I think I messed up the directory structure before, or something?

### oh-my-zsh

Now THIS ONE I maintain; I use this stuff the most often! I do need to reconcile the divergence between the version in this repo and my work setup, though. Oh My ZSH should be installed before stowing this. Additionally, a few of the plugins I use must be cloned from their GitHub repos.

Currently, the prompt I use displays info about the current ruby version, which I don't want. Gotta figure out how to disable that.

@import "./images/ruby_in_prompt.png"

- To install Oh My ZSH!:

  - `sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

- Plugins to clone:

  - `git clone https://github.com/zsh-users/zsh-syntax-highlighting ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting`

  - `git clone https://github.com/zsh-users/zsh-autosuggestions ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions`

### vs-code

This is a bit of a placeholder, to get something working before I merge in the definitive version. Based on my old laptop's settings, which I only set up last night.

Another thing in need of setup with this part of the repo is managing configuration for different versions of VS Code. Right now [my Arch installer](https://github.com/amorgan101010/arch-setup) sets up the OSS version, but I'm using the "MS official" (and I think non-FOSS) version on my current install. I suppose it would be worth determining if I need anything outside the stuff available in the non-AUR repos...but even if I don't, I hate that the OSS version stores its config in a path with spaces. Feels like MS (or maybe the Arch packager, if they chose that path) is punishing me for using open source! For now, I've made a script to copy the non-OSS settings to the OSS path (so I can automate escaping spaces in the copy command (which I'd only need to do once anyway, as it gets saved in my autocomplete history)).

Copying a file on every commit seems like a good candidate for a hook; I should migrate a generic version of my notes about pre-commit hooks and make one that does that. Having some template githooks seems like something I will want.

