# VIM VADEMECUM
## Configuration file
### input on the terminal

```
vim $HOME/.vimrc

```
### then ...

```

set number
syntax enable
set numberwidth=1
set clipboard=unnamed
set showcmd
set ruler
set encoding=utf-8
set showmatch
set sw=2
set relativenumber
set hlsearch


" Indentation settings

set tabstop=4
set smartindent
set autoindent
set expandtab


" set cursor configuration


" Plugins

call plug#begin('~/.vim/plugged')

" Themes


 Plug 'arcticicestudio/nord-vim'
 Plug 'vim-airline/vim-airline-themes'
 Plug 'whatyouhide/vim-gotham'

" Syntax

 Plug 'sheerun/vim-polyglot'

" Typing

 Plug 'Krasjet/auto.pairs'
 Plug 'alvan/vim-closetag'

" IDE

 Plug 'easymotion/vim-easymotion'
 Plug 'scrooloose/nerdtree'


call plug#end()

colorscheme koehler

let g:airline_theme='solarized'

" Configuration easymotion

let mapleader=" "

nmap <Leader>s <Plug>(easymotion-s2)


" Configuration nerdtree

let NERDTreeQuitOnOpen=1

nmap <Leader>nt :NERDTreeFind<CR>

" Configuration custom commands

nmap <Leader>w :w<CR>
nmap <Leader>q :q<CR>
cnoreabbrev <expr> tn getcmdtype() == ":" && getcmdline() == 'tn' ? 'tabnew' : 'tn'
nnoremap <CR> :noh<CR>



```