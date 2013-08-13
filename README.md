# Dotfile Boilerplate

Your dotfiles: 

Unified. Organized. Personalized.

## Quickstart

If you don’t already have a huge collection of dotfiles simply run the installer and follow the prompts:

```Shell
git clone git://github.com/thcipriani/dotfile-boilerplate ~/.dotfiles
cd ~/.dotfiles
./bootstrap --new-setup
```

Follow the prompts

If you already have a collection of dotfiles then you should omit the `--new-setup` flag
so that you won't be prompted to install any frameworks

## What's a dotfile?

see: http://dotfiles.github.io/

## Why

There is no canonical method for dotfile organization, sharing, and bootstraping 
that is cross-shell and cross-system compatible.

This project should work to provide dotfile-beginners with sensible defaults
and advanced users with a powerful, configurable framework on which to build.

## Features

At it&#8217;s core, **Dotfile Boilerplate** is a system for dotfile 
organization more than an opinionated framework.

The basic structure of **Dotfile Boilerplate** is based on Zach Holman's 
[holman/dotfiles](https://github.com/holman/dotfiles) dotfiles. Configuration 
files are grouped by topic (e.g., "git", "vim", "zsh", etc.)., and a file 
named `[whatever].symlink` will by symlinked to `~/.[whatever]`.

**Dotfile Boilerplate** heavily "borrows" from many fine dotfile repos

- _Heavily Modified_ [holman](https://github.com/holman/dotfiles) boostrap script
- [mathiasbynens](http://mths.be/dotfiles) exports, aliases and functions and osx where applicable
- [tpope](https://github.com/tpope/vim-pathogen)'s Pathogen and sensible.vim
- [gf3](https://github.com/gf3/dotfiles)'s Sexy Bash Prompt (for Bash Users)
- [robbyrussell](https://github.com/robbyrussell/oh-my-zsh)'s Oh-my-zsh (for ZSH Users)
- [sjl](http://stevelosh.com/blog/2010/02/my-extravagant-zsh-prompt/)'s Extravagant ZSH Prompt (for ZSH Users)
- [carlhuda](https://github.com/carlhuda/janus)'s Janus Vim Framework (for ZSH Users)
- [metellius](http://www.reddit.com/r/commandline/comments/kbeoe/you_can_make_readline_and_bash_much_more_user/) + [mathiasbynens](http://mths.be/dotfiles) inputrc
- [sjl](https://bitbucket.org/sjl/dotfiles/src/a3ff27f963ced7e7e1e024faab6b5c8d46557172/tmux/tmux.conf?at=default)'s tmux.conf
- a very fine screenrc that's source I no longer remember

**Further inspiration came from**

- [jclem](https://github.com/jclem/dotfiles)'s dotfiles
- [ldmosquera](https://github.com/ldmosquera/dotfiles/wiki)'s dotfile wiki
- [heptal](https://gist.github.com/heptal/6052573)'s tput abuse
- [pastjean](https://github.com/pastjean/dotfiles)'s dotfiles

All of that can, of course, be overridden. 

## Learn More

Checkout the [documentation](https://github.com/thcipriani/dotfile-boilerplate/blob/master/docs/getting_started.md).

## Contributing

Fork me and send me a pull request =)