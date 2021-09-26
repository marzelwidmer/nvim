let mapleader = ","

syntax on

filetype on
filetype indent on
filetype plugin on
filetype off

set encoding=UTF-8
set nocompatible
set hlsearch
set number relativenumber
set laststatus=2
set vb
set ruler
set spelllang=en_us
set autoindent
set colorcolumn=180
set mouse=a
set clipboard=unnamed
set noscrollbind
set wildmenu
set autochdir
set noerrorbells
set expandtab
set smartindent
set nowrap

"> Plug 
call plug#begin('~/.config/nvim/plugged')

Plug 'tpope/vim-fugitive'                               " https://github.com/tpope/vim-fugitive
Plug 'preservim/nerdtree'                               " https://github.com/preservim/nerdtree.  
Plug 'ctrlpvim/ctrlp.vim'                               " https://ctrlpvim.github.io/ctrlp.vim/ 		
Plug 'justinmk/vim-sneak'
Plug 'nvim-lua/plenary.nvim'
Plug 'nvim-telescope/telescope.nvim'                    " https://github.com/nvim-telescope/telescope.nvim
Plug 'kyazdani42/nvim-web-devicons'                     " for file icons
Plug 'kyazdani42/nvim-tree.lua'                         " https://github.com/preservim/nerdtree
Plug 'vim-airline/vim-airline'                          " https://github.com/vim-airline/vim-airline
Plug 'ryanoasis/vim-devicons'                           " https://github.com/ryanoasis/vim-devicons + https://github.com/ryanoasis/nerd-fonts/
Plug 'tpope/vim-commentary'                             " https://github.com/tpope/vim-commentary (gc)
Plug 'airblade/vim-gitgutter'                           " https://github.com/airblade/vim-gitgutter
Plug 'mkitt/tabline.vim'                                " https://github.com/mkitt/tabline.vim
Plug 'Pocco81/AutoSave.nvim'                            " https://github.com/Pocco81/AutoSave.nvim

"> Go
Plug 'fatih/vim-go', { 'do': ':GoInstallBinaries' }     " https://github.com/fatih/vim-go
Plug 'neoclide/coc.nvim', {'branch': 'release'}         " https://github.com/neoclide/coc.nvim

"> Kotlin
Plug 'udalov/kotlin-vim'
"> YAML
Plug 'avakhov/vim-yaml'

"> Theme
Plug 'NLKNguyen/papercolor-theme'               " https://github.com/NLKNguyen/papercolor-theme

call plug#end()
"-- plug END

"> Tabline
hi Search       cterm=NONE      ctermfg=black           ctermbg=red
hi TabLine      ctermfg=Black   ctermbg=Green           cterm=NONE
hi TabLineFill  ctermfg=Black   ctermbg=Green           cterm=NONE
hi TabLineSel   ctermfg=White   ctermbg=DarkBlue        cterm=NONE



"> Map
map <silent> <C-n> :NERDTreeFocus<CR>

"> netrw
nnoremap - :Explore<CR>
let g:netrw_banner = 0
let g:netrw_liststyle = 3
let g:netrw_bufsettings = 'noma nomod nu nobl nowrap ro'
autocmd FileType netrw setl bufhidden=delete
"-- netrw END

"> ctrlp
set runtimepath^=~/.vim/bundle/ctrlp.vim
let g:ctrlp_user_command = ['.git', 'cd %s && git ls-files -co --exclude-standard']

"> vim-gitgutter
set updatetime=500
"-- vim-gitgutter END

"> papercolor-theme
set termguicolors
set background=dark
colorscheme PaperColor
"-- papercolor-theme END

"> https://github.com/Pocco81/AutoSave.nvim
lua << EOF
local autosave = require("autosave")

autosave.setup(
    {
        enabled = false,
        execution_message = "AutoSave: saved at " .. vim.fn.strftime("%H:%M:%S"),
        execution_message = "AutoSave: saved at " .. vim.fn.strftime("%H:%M:%S"),
        events = {"InsertLeave", "TextChanged"},
        conditions = {
            exists = true,
            filename_is_not = {},
            filetype_is_not = {},
            modifiable = true
        },
        write_all_buffers = false,
        on_off_commands = true,
        clean_command_line_interval = 0,
        debounce_delay = 135
    }
)
EOF

