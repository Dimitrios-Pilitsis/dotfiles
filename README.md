# dotfiles

This repository contains all my personal dotfiles

GNU Stow is used for handling symlinks

Repository Includes plugins for Vim and Tmux

How to setup dotfiles in new system:
1. Clone this repository
2. Install GNU stow with package manager of choice e.g. `sudo apt install stow`
3. Run `stow <directory_name>` for each stow directory e.g. `stow vim`


# Tmux plugins

I use the [Tmux plugin manager](https://github.com/tmux-plugins/tpm)

Clone TPM repository to install:
	
	$ git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm


I use the following plugins:
1. [Tmux resurrect](https://github.com/tmux-plugins/tmux-resurrect)
2. [Tmux sensible](https://github.com/tmux-plugins/tmux-sensible)

Add plugins to the list of TPM plugins in `.tmux.conf`:

	set -g @plugin 'tmux-plugins/tpm'
	set -g @plugin 'tmux-plugins/tmux-sensible'
	set -g @plugin 'tmux-plugins/tmux-resurrect'


# Vim plugins

I use the built-in package management system. See [link](https://github.com/vim/vim/blob/03c3bd9fd094c1aede2e8fe3ad8fd25b9f033053/runtime/doc/repeat.txt#L515) for official method of installing Vim packages

A Vim package is a directory containing one or more plugins. By default, your Vim settings are contained in `~/.vim`, so that's where Vim looks for plugins when you launch it.

When you start Vim, it first processes your `.vimrc` file, and then it scans all directories in `~/.vim` for plugins contained in `pack/*/start`. Any Vim plugins placed in `~/.vim/pack/*/start` will automatically load when you launch Vim.

If you don't want a plugin to load automatically every time you launch Vim, you can place the plugin within an opt directory, namely `~/.vim/pack/*/opt` directory.

Any plugins installed into `opt` are available to Vim, but they're not loaded into memory until you add them to a session with the `packadd` command e.g. `:packadd package_name`


I use the following packages:
1. [Solarized Colorscheme for Vim](https://github.com/altercation/vim-colors-solarized)
2 [Vim-airline](https://github.com/vim-airline/vim-airline)
3. [Vim-airline-themes](https://github.com/vim-airline/vim-airline-themes)
4. [Syntastic](https://github.com/vim-syntastic/syntastic)
5. [NerdTree](https://github.com/preservim/nerdtree)
6. [Jedi-vim](https://github.com/davidhalter/jedi-vim)
7. [ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)
8. [vim-surround](https://github.com/tpope/vim-surround)
9. [Vim Git gutter](https://github.com/airblade/vim-gitgutter)
10. [Vim-fugitive](https://github.com/tpope/vim-fugitive)
11. [Vim-commentary](https://github.com/tpope/vim-commentary)


To install a package, for instance NerdTree, run the following command:

	$ git clone --depth 1 \
  	git@github.com:preservim/nerdtree.git \
  	~/.vim/pack/NERDTree/start/NERDTree


# Markdown

I use [Grip](https://github.com/joeyespo/grip) to render markdown files (uses GitHub Markdown API)
