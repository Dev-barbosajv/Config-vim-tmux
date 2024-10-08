# Config Vim

Este repositório contém as configurações personalizadas do Vim que utilizo para programação e desenvolvimento.

## Plugins Utilizados

Utilizo o gerenciador de plugins [vim-plug](https://github.com/junegunn/vim-plug) para gerenciar meus plugins. Aqui estão os plugins que estão instalados:

- **Tema**: [dracula/vim](https://github.com/dracula/vim)
- **NERDTree**: [preservim/nerdtree](https://github.com/preservim/nerdtree)
- **Autocompletar e Linting**: 
  - [davidhalter/jedi-vim](https://github.com/davidhalter/jedi-vim)
  - [dense-analysis/ale](https://github.com/dense-analysis/ale)
  - [psf/black](https://github.com/psf/black)
- **Barra de Status**: [itchyny/lightline.vim](https://github.com/itchyny/lightline.vim)
- **Comentários fáceis**: [tpope/vim-commentary](https://github.com/tpope/vim-commentary)
- **Busca Rápida**: 
  - [junegunn/fzf](https://github.com/junegunn/fzf)
  - [junegunn/fzf.vim](https://github.com/junegunn/fzf.vim)
- **Busca no Projeto**: [ctrlpvim/ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)
- **Controle de Versão**: 
  - [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive)
  - [airblade/vim-gitgutter](https://github.com/airblade/vim-gitgutter)
  - [itchyny/vim-gitbranch](https://github.com/itchyny/vim-gitbranch)
- **Ambientes Virtuais**: [jmcantrell/vim-virtualenv](https://github.com/jmcantrell/vim-virtualenv)
- **Go Development**: [fatih/vim-go](https://github.com/fatih/vim-go)
- **Auto Completar**: [neoclide/coc.nvim](https://github.com/neoclide/coc.nvim)
- **Surround**: [tpope/vim-surround](https://github.com/tpope/vim-surround)
- **Snippets**: [garbas/vim-snipmate](https://github.com/garbas/vim-snipmate)
- **Ícones para NERDTree**: [ryanoasis/vim-devicons](https://github.com/ryanoasis/vim-devicons)
- **NERDTree Git Plugin**: [Xuyuanp/nerdtree-git-plugin](https://github.com/Xuyuanp/nerdtree-git-plugin)
- **Visualização do NERDTree**: [junegunn/nerdtree-visual-izer](https://github.com/junegunn/nerdtree-visual-izer)

## Configurações do Vim

Aqui estão algumas das configurações que utilizei:

```vim
" Início do gerenciador de plugins
call plug#begin('~/.vim/plugged')

" Tema Dracula
Plug 'dracula/vim', { 'as': 'dracula' }

" NERDTree para navegação de arquivos
Plug 'preservim/nerdtree'

" Autocompletar e Linting
Plug 'davidhalter/jedi-vim'
Plug 'dense-analysis/ale'
Plug 'psf/black', { 'branch': 'stable' }

" Lightline para barra de status
Plug 'itchyny/lightline.vim'

" Comentários fáceis
Plug 'tpope/vim-commentary'

" FZF para busca rápida
Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
Plug 'junegunn/fzf.vim'

" CtrlP para busca no projeto
Plug 'ctrlpvim/ctrlp.vim'
Plug 'tpope/vim-fugitive'
Plug 'airblade/vim-gitgutter'
Plug 'itchyny/vim-gitbranch'
Plug 'jmcantrell/vim-virtualenv'
Plug 'fatih/vim-go'
Plug 'neoclide/coc.nvim', {'branch': 'release'}
Plug 'tpope/vim-surround'
Plug 'garbas/vim-snipmate'
Plug 'ryanoasis/vim-devicons'
Plug 'Xuyuanp/nerdtree-git-plugin'
" Plug 'junegunn/nerdtree-visual-izer'  " Comente esta linha se necessário

call plug#end()

" Configurações do tema
syntax enable
colorscheme dracula

" Configurações do Python
filetype plugin indent on
set expandtab
set tabstop=4
set shiftwidth=4
set number
set updatetime=100

" Configurações do NERDTree
let g:NERDTreeWinPos = "right"
let g:NERDTreeGitStatusUseNerdFonts = 1
nnoremap <C-n> :NERDTreeToggle<CR>
nnoremap <C-t> :NERDTreeFind<CR>

" Navegação em splits
nnoremap <C-h> <C-w>h
nnoremap <C-j> <C-w>j
nnoremap <C-k> <C-w>k
nnoremap <C-l> <C-w>l
