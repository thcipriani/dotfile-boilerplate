# Getting Started with Dotfile Boilerplate

## If you don&#8217;t already have a dotfile collection

Simply run the installer and follow the prompts:
```
git clone git://github.com/thcipriani/dotfile-boilerplate ~/.dotfiles
cd ~/.dotfiles
./bootstrap
```

## If you have TONS of dotfiles already

Well, my friend, you&#8217;ve got some work to do&#8212;but the net result 
should be a very configurable and portable setup.

The main files you&#8217;ll want to change are: `~/.dotfiles/shell/aliases.symlink`, 
`~/.dotfiles/shell/exports.symlink`, `~/.dotfiles/shell/functions.symlink`,
`~/.dotfiles/shell/extra.symlink` and any configuration files for programs that
you already have and want to keep. Each of those are meant to hold and bash 
aliases, exported variables, unique functions or other configuration respectively.

In addition to the files in the `~/.dotfiles/shell` directory there are 
system&#8212;specific copies of those all the `shell` files in their respective 
system folders&#8212;`osx` for Macs and `linux` for Linux machines.

The goal is to have a single, unified, dotfile repo for all the systems on which you work.

By default **Dotfile Boilerplate** includes config files for:

- bash (including `.bash_profile`, `.bashrc` and `.bash_prompt`)
- zsh
- vim (both `.vimrc` and `.vim/` directory with Pathogen)
- tmux
- ack
- `.inputrc`

## How does it work?

`bootstrap` will guide you through the setup of sensible defaults for your system.
All files in this directory (and the any subdirectory that is a direct decentdant 
of this directory) taht follow the format `*.symlink` will be symlinked in 
your `$HOME` directory.

```
~/.dotfiles/*/**/basename.symlink → ~/.basename
```

### Semi-Intelligent

If you already have a `~/.*rc` file for a program **Dotfile Boilerplate**&#8217;s 
`bootstrap` won&#8217;t simply overwrite that file&#8212;you&#8217;ll be 
prompted if you want to `[s]kip` that config, `[b]ackup` that config (saving 
it to `~/.[whatever].backup` OR simply `[o]verwrite` the existing file.

**Dotfile Boilerplate** detects your system type and only is somewhat intelligent 
and will only link items form the `osx` folder if you&#8217;re on a Mac&#8212;likewise
for the `linux` directory on linux.

**Dotfile Boilerplate** also detects shell type and won&#8217;t install anything
from the `zsh` directory if you&#8217;re using bash&#8212;likewise if you&#8217;re
using z-shell it won&#8217;t install anything from the `bash` directory.

### Prompts

As the bootstrap script runs you _may_&#8212;depending on your current configurations&#8212;be
prompted to install some shell frameworks ([Oh-My-ZSH](http://github.com/robbyrussell/oh-my-zsh/) for Z-Shell users
and [Bash-It](https://github.com/revans/bash-it) for Bash users).

If you already have these frameworks installed in their default locations&#8212;**Dotfile Boilerplate**
will proceed with the remainder of the installation without prompting you to
_reinstall_ these frameworks.

In addition to these shell frameworks if your `~/.dotfiles/vim/.vimrc` is LESS 
THAN 10 lines AND you have `curl`, `ack`, `ctags`, `git`, `ruby`, and `rake` in your
`$PATH` you will be prompted to install the [Janus Vim Framework](https://github.com/carlhuda/janus)
