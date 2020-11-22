##H2

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
