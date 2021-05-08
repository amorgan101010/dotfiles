# Dotfiles

Aileen Morgan's dotfiles.

## Prerequisites

- The program `stow`

- [The guide I based this on](https://alexpearce.me/2016/02/managing-dotfiles-with-stow/)

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

### ZSH

Now THIS ONE I maintain; I use this stuff the most often! I do need to reconcile the divergence between the version in this repo and my work setup, though.

## How to Set Up

I'll use `zsh` as the example.

1. Clone `dotfiles` into home directory

2. `cd` into it

3. Run `stow zsh`

`stow` copies the contents of the `zsh` directory one level above where it is run; in this case, one level up is the home directory.
