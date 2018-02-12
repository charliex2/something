# Mac vim 显示行号和语法高亮

Mac用vim或者vi打开一个文件的时候，特别是配置文件的时候，密密麻麻都是文字，没有语法高亮，非常不方便。

但是如何开启语法高亮和行号呢？

### 拷贝一份vim的共享配置文件到个人目录下

```shell
cp /usr/share/vim/vimrc ~/.vimrc
```

如果系统是redhat的话，执行：

```shell
cp /etc/vimrc ~/.vimrc
```

### 添加配制
在 `~/.vimrc`后追加两行

```shell
vim ~/.vimrc
```
添加的内容：
```
syntax on
set nu!
```

### 其他vim配置项

```
set nocompatible            "去掉有关vi一致性模式，避免以前版本的bug和局限
set nu!                     "显示行号
set guifont=Luxi/Mono/9     " 设置字体，字体名称和字号
filetype on                 "检测文件的类型     
set history=1000            "记录历史的行数
set background=dark         "背景使用黑色
syntax on                   "语法高亮度显示
set autoindent              "vim使用自动对齐，也就是把当前行的对齐格式应用到下一行(自动缩进）
set cindent                 "（cindent是特别针对 C语言语法自动缩进）
set smartindent             "依据上面的对齐格式，智能的选择对齐方式，对于类似C语言编写上有用   
set tabstop=4               "设置tab键为4个空格，
set shiftwidth=4            "设置当行之间交错时使用4个空格     
set ai!                     " 设置自动缩进 
set showmatch               "设置匹配模式，类似当输入一个左括号时会匹配相应的右括号      
set guioptions-=T           "去除vim的GUI版本中得toolbar   
set vb t_vb=                "当vim进行编辑时，如果命令错误，会发出警报，该设置去掉警报       
set ruler                   "在编辑过程中，在右下角显示光标位置的状态行     
set nohls                   "默认情况下，寻找匹配是高亮度显示，该设置关闭高亮显示     
set incsearch               "在程序中查询一单词，自动匹配单词的位置；如查询desk单词，当输到/d时，会自动找到第一个d开头的单词，当输入到/de时，会自动找到第一个以ds开头的单词，以此类推，进行查找；当找到要匹配的单词时，别忘记回车 
set backspace=2             " 设置退格键可用

```

> 以上参考 https://www.cnblogs.com/yjmyzz/p/4019783.html