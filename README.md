# myVimSetup
I am going to upload my vim configuration in this directory

## Plugins
* [VundleVim:](https://github.com/VundleVim/Vundle.vim)
  This Work as Vim Package Manager
* [Asynchronous Lint Engine:](https://github.com/dense-analysis/ale)
  

### Installation:

#### VundleVim: 

##### Step1:
```bash
git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
  * if `~/.vim/bundle` doesnt exsist or didint created in progress create it:
  ```console
  mkdir ~/.vim/bundle
  ```
##### Step2:
copy this into the `./vimrc` file which is located at:` ~/.vimrc`
```vim
set nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()
" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'
All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
"
" Brief help
" :PluginList       - lists configured plugins
" :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
" :PluginSearch foo - searches for foo; append `!` to refresh local cache
" :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
"
" see :h vundle for more details or wiki for FAQ
" Put your non-Plugin stuff after this line
```

#### Asynchronous Lint Engine:
##### Step1:

```console
cd ~/.vim/bundle
```
* if it doesnt exsist:
  ```console
  mkdir ~/.vim/bundle
  ```
```console
git clone --depth 1 https://github.com/dense-analysis/ale.git ~/.vim/bundle
```

#### Flake8
add this in to the `vimrc` file:
```vim
Plugin 'nvie/vim-flake8'
```
Run this command:
```bash
vim +PluginInstall +qall
```
