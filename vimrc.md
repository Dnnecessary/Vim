</br>

关闭vi的兼容模式(兼容模式下会让vim关闭所有的扩展，丢掉vim很多强大的功能去兼容vi)
```
set nocompatible
```


</br>
</br>


插件开始的位置
```
call vundle#begin()
```
</br>

vim-plug插件管理
```

call vundle#begin()
Plug 'morhetz/gruvbox'
Plug 'mileszs/ack.vim'
Plug 'vim-airline/vim-airline'

call vundle#begin()
```
</br>

插件结束的位置
```
call plug#end()
```

</br>

*插件简要使用*
```
:PlugStatus 查看插件状态
:PlugInstall  安装插件
:PlugDiff     更新插件
:PlugClean  卸载插件
```



### 插件推荐
导航目录侧边栏
```
Plugin 'scrooloose/nerdtree'
```

使nerdtree tab标签的名称更友好
```
Plugin 'jistr/vim-nerdtree-tabs'
```

nerdtree中看git版本信息
```
Plugin 'Xuyuanp/nerdtree-git-plugin'
```

文件搜索, 快速跳转文件
```
Plugin 'ctrlpvim/ctrlp.vim'
```

全局搜索
```
Plugin 'dyng/ctrlsf.vim'
```

大纲式导航(右边出现的那个导航的）
```
Plugin 'majutsushi/tagbar'
```

内容搜索
```
Plugin 'rking/ag.vim'
```

快速移动（跳转）
```
Plugin 'Lokaltog/vim-easymotion'
```
成对标签跳转
```
Plugin 'vim-scripts/matchit.zip'
```

快速注释
```
Plug 'preservim/nerdcommenter'
```

成对符号编辑(快速给词加环绕符号,例如单引号/双引号/括号/成对标签等)
```
Plugin 'tpope/vim-surround'
```

Python开发插件
```
Plugin 'klen/python-mode'
```

Git 差比对
```
Plugin 'airblade/vim-gitgutter'
```

状态栏增强显示
```
Plugin 'bling/vim-airline'
```

颜色主题
```
Plug 'morhetz/gruvbox'
```


对所有缓冲区中的文件启用语法高亮度
```
syntax on
```

定义快捷键的前缀
```
let mapleader = ','
```

关闭欢迎页面
```
set shortmess=atI
```

保存历史命令行数
```
set history=1000
```

关闭swap
```
set noswapfile
```

关闭备份
```
set nobackup
```

关闭vim 报错声音
```
set noerrorbells
```

高亮当前行
```
set cursorline
```

高亮当前列
```
set cursorcolumn
```
关闭鼠标
```
set mouse-=a
```
控制vim剪贴板
```
set clipboard+=unnamed
```

允许在插入模式下对所有内容进行退格
```
set backspace=indent,eol,start
```

行间距 （GUI下才有效）
```
set linespace=0
```

刷新率100ms ?
```
set updatetime=100
```

在新Tab中打开新的缓冲区
```
set switchbuf=usetab,usetab
```

搜索时 忽略这些文件/夹
```
set wildignore+=*/.git/*,
      \*/.hg/*,*/.svn/*,
      \*/cscope*,*/*.csv/,
      \*/*.log,*tags*,*/bin/*
```

在最下面状态栏显示正在输入的命令
```
set showcmd
```

在左下角的状态栏显示 --INSERT-- 之类的状态
```
set showmode
```

显示行号
```
set number
```

行号显示宽度
```
set numberwidth=2
```

当输入一个左括号时自动匹配右括号
```
set showmatch
```

关闭Preview窗口
```
set completeopt-=preview
```

增强自带的 ? 和 ／ 搜索功能， 并且支持更加高级的正则表达式匹配
```
set incsearch
```

高亮搜索内容
```
set hlsearch
```

查找忽略大小写
```
set ignorecase
```
如果有一个大写字母，则切换到大小写敏感查找
```
set smartcase
```


默认的字符编码
```
set encoding=utf-8
```

自动识别文件编码
```
set fileencodings=utf-8,ucs-bom,gbk,gb2312,gb18030,default
```

文本格式优先unix风格
```
set fileformats=unix,dos,mac
```

向右切分窗口
```
set splitright
```

向下切分窗口
```
set splitbelow
```

自动读取文件(如果文本改变，自动更新）
```
set autoread
```

始终显示状态栏（倒数第二行）
```
set laststatus=2
```





  
多个窗口 用Ctr加 `j k h l` 切换
```
map <C-j> <C-W>j
map <C-k> <C-W>k
map <C-h> <C-W>h
map <C-l> <C-W>l
```
  



自动记住上次位置
```
autocmd BufReadPost *
    \ if line("'\"")>0&&line("'\"")<=line("$") |
    \   exe "normal g'\"" |
    \ endif
```




热键设置
w!! 用sudo权限保存文件
```
cmap w!! w !sudo tee > /dev/null %
```

,/ 移除搜索高亮
noremap <silent><leader>/ :nohls<CR>

,sa 选择全部
```
map <leader>sa ggvG$
```

,w 保存当前文件
```
nnoremap <leader>w :w<CR>
```

; -> :
nnoremap ; :

修复ctags ctrl+]无效问题
nmap <c-]> g<c-]>


