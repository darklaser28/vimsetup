## Let's get started !

### Download the setup file your local machine 

Simply click here to download the setup file : 
https://ftp.nluug.nl/pub/vim/pc/gvim82.exe

Or if you want to try it yourself go to the official website(https://www.vim.org/download.php) and scroll down and download the Self-installing executable under the "PC: MS-DOS and MS-Windows" section 
and save it in your downloads folder

### Execute the setup file for Vim's installation 

Go to your downloads folder and double click the file to install Vim. Then you will see the install box popup and you don't have to do anything else than smashing the "next" button and check the "I accept the terms of 
license agreement" box. Now you succesfully installed Vim ! But it's not finished, you need to install  the plugins for get a clean Vim environment. 

## Create your _vimrc file 

In order to install the plugins, you are going to make a file called "_vimrc" in your user folder. This is the file that handles your plugins, basically your whole vim environment. 

### Install the plugins 

Now open gVim (it's on your desktop). Then on the editor enter the command mode by typing ":" (wich will make you get to command mode) and then the following ":w C:\Users\USERNAME\_vimrc.
This command will create your vimrc file on in your users directory. 

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
