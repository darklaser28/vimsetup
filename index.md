# Let's get started !

## Download the setup file your local machine 

Simply click here to download the setup file : 
https://ftp.nluug.nl/pub/vim/pc/gvim82.exe

Or try it yourself : go to the official website(https://www.vim.org/download.php) and scroll down and download the Self-installing executable under the "PC: MS-DOS and MS-Windows" section 
and save it in your downloads folder

## Execute the setup file for Vim's installation 

Now install Vim from the setup file in your downloads folder. Then smash the "next" button and check the "I accept the terms of 
license agreement" box. Now you succesfully installed Vim ! But it's not finished, you need to install  the plugins for a clean Vim environment. 

## Create your _vimrc file 

In order to install the plugins, you are going to make a file called "_vimrc" in your user folder. This is the file that handles your plugins, basically your whole vim environment. 

Now open gVim (it's on your desktop). Then on the editor enter the command mode by typing ":" (wich will make you get to command mode) and then the following ":w C:\Users\USERNAME\_vimrc".
This command will create your vimrc file on in your users directory. Now source it so that vim knows where the _vimrc file is located in by typing ":source C:\Users\USERNAME\_vimrc". 

## Install the plugins 

Now copy paste the following in your _vimrc file and finally save it (:w) and source it (:source C:\Users\USERNAME\_vimrc) 

```vim

syntax on
set clipboard=unnamed
let mapleader = ","
set number 
set mouse=a
set shiftwidth=4
set softtabstop=0
set tabstop=4
set backspace=indent,eol,start
set backspace=2 " make backspace work like most other programs
set pythonthreehome=C:\Python36-32\
set pythonthreedll=C:\Python36-32\python36.dll
nmap <leader>so :source $HOME\_vimrc<CR>
autocmd filetype cpp nnoremap <F5> :w <bar> !g++ -std=c++11 -O2 -Wall % -o %:r && %:r.exe <CR>

" Specify a directory for plugins
" - For Neovim: stdpath('data') . '/plugged'
" - Avoid using standard Vim directory names like 'plugin'
call plug#begin('~/.vim/plugged')

" Make sure you use single quotes

" Shorthand notation; fetches https://github.com/junegunn/vim-easy-align
Plug 'junegunn/vim-easy-align'
Plug 'jiangmiao/auto-pairs'


" On-demand loading
Plug 'scrooloose/nerdtree', { 'on':  'NERDTreeToggle' }

" Initialize plugin system
call plug#end()

```
