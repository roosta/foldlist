# Overview

The `Fold List` plugin provides the following features:

1. Opens a vertically split Vim window with a list of folds in
   the current file.
2. Moving through the fold list with the `j`, `k`, `l`, `h`, moves to the
   associated fold in the file.
3. `<CR>` jumps between file and fold list.

## Installation

### Manually
Put `foldlist.vim` in `~/.vim/plugin/` (on unix-like systems) or `%userprofile%\vimfiles\plugin\` (on Windows).

### Vim 8

Vim 8 has native support for loading plugins. All you need to do to is to clone
this repository into `~/.vim/plug/default/opt`.

```sh
git clone https://github.com/roosta/vim-foldlist ~/.vim/plug/default/opt
```

The same works for NeoVim, but you have to clone it into a path where NeoVim can
find it.

```sh
git clone https://github.com/roosta/vim-foldlist ~/.config/nvim/plug/default/opt
```

### [dein.vim](https://github.com/Shougo/dein.vim)

```vim
call dein#add('roosta/vim-foldlist')
```

### [vim-pathogen](https://github.com/tpope/vim-pathogen)
```shell
cd ~/.vim/bundle
git clone https://github.com/roosta/vim-foldlist
```

### [vim-plug](https://github.com/junegunn/vim-plug)
```vim
Plug 'srcery-colors/vim-foldlist'
```
## Usage

You can open the foldinst window from a source window by using the `:Flist`
command.

```vim
nnoremap <silent> <F9> :Flist<CR>
```

Add the above mapping to your `~/.vimrc` file.

You can close the foldlist window from the foldlist window by pressing `q` or
using the Vim `:q` command.

## Caveats

Fold is searched using fold title only. This may find other places in file with
the same string.

## Attribution
This is a fork of https://github.com/vim-scripts/foldlist, credit goes to original author Paul C. Wei

