# Getting Started with Dotfile Boilerplate

## Quick Start

If you don&#8217;t already have a huge collection of dotfiles simply run the 
installer and follow the prompts:

```Shell
git clone git://github.com/thcipriani/dotfile-boilerplate ~/.dotfiles
cd ~/.dotfiles
./bootstrap --new-setup
```

## How it works

`bootstrap` will guide you through the setup of sensible defaults for your system.
All files in the `~/.dotfiles` directory (and any subdirectory that is a direct descendant 
of the `~/.dotfiles` directory) that follow the format `*.symlink` will be symlinked in 
your `$HOME` directory.

```Shell
~/.dotfiles/*/*/basename.symlink → ~/.basename
```

If you&#8217;ve already accumulated a large collection of dotfiles, 
this repository should create a very configurable and portable profile that you can host
on github, bitbucket, dropbox, s3 or wherever.

### Files to tweak

The main files you&#8217;ll want to change are: 

- `~/.dotfiles/profile.d/aliases.symlink`
- `~/.dotfiles/profile.d/exports.symlink`
- `~/.dotfiles/profile.d/functions.symlink`
- `~/.dotfiles/profile.d/extra.symlink`

Each of those are meant to hold and bash aliases, exported variables, 
unique functions or other configuration, respectively.

In addition to those files, be sure to modify any files in `~/.dotfiles` which may
overwrite configurations that you&#8217;d like to keep.

### Some Configs for OSX, Other Configs for Linux

Yep. We do that.

In addition to the files in the `~/.dotfiles/shell` directory there are 
system-specific copies of all the `shell` files in their respective 
system folders&#8212;`osx` for Macs and `linux` for Linux machines.

The goal is to have a single, unified, dotfile repo for all the systems on which you work.

### Default Configs

By default **Dotfile Boilerplate** includes config files for:

- bash (including `.bash_profile`, `.bashrc` and `.bash_prompt`)
- zsh
- vim (both `.vimrc` and `.vim/` directory with Pathogen)
- tmux
- ack
- `.inputrc`

These configurations where amalgamated from various sources which are, largely (hopefully),
indicated in-line in the actual config file.

### Semi-Intelligent

If you already have an `~/.*rc` file for a program, **Dotfile Boilerplate**&#8217;s 
`bootstrap` won&#8217;t simply overwrite that file&#8212;you&#8217;ll be 
prompted if you want to `[s]kip` that config, `[b]ackup` that config (saving 
it to `~/.[whatever].backup` OR simply `[o]verwrite` the existing file.

**Dotfile Boilerplate** detects your system-type and will only link items 
from the `osx` folder if you&#8217;re on a Mac&#8212;likewise
for the `linux` directory on linux.

**Dotfile Boilerplate** also detects shell-type and won&#8217; link anything
from the `zsh` directory if you&#8217;re using bash&#8212;likewise if you&#8217;re
using Z-Shell, it won&#8217;t install anything from the `bash` directory.

### Prompts

`bootstrap` is also able to semi-intelligently a small collection of dotfile frameworks.

To be prompted to install new frameworks simply run bootstrap with the `--new-setup` option.

If you run the bootstrap script with the `--new-setup` flag you _may_&#8212;depending on your current configurations&#8212;be
prompted to install some shell frameworks ([Oh-My-ZSH](http://github.com/robbyrussell/oh-my-zsh/) for Z-Shell users
and [Bash-It](https://github.com/revans/bash-it) for Bash users).

If you already have these frameworks installed in their default locations&#8212;**Dotfile Boilerplate**
will proceed with the remainder of the installation without prompting you to
_reinstall_ these frameworks.

In addition to these shell frameworks if your `~/.dotfiles/vim/.vimrc` is LESS 
THAN 10 lines AND you have `curl`, `ack`, `ctags`, `git`, `ruby`, and `rake` in your
`$PATH` you will be prompted to install the [Janus Vim Framework](https://github.com/carlhuda/janus)
