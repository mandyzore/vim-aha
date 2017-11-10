# vim-aha
Mine Vim Conf


## pylint
现在日常开发用的是python，使用```syntactic```配合我司标配.pylint.rc食用。

## hack syntactic check 'on fly'

因为没找到```syntactic```在写代码过程中自动检查可配操作，只能通过vim ```:w```手动保持file来触发syntactic，sad

But, 很自然的，我们可以退而求其次去寻找自动实现vim自动保存的操作。

Vim本身可以配置自动保存，不过要设置一些参数；懒癌发作找到一个封装好的插件，vim-auto-save，可以通过Vundle安装, 亲测可用, insert模式一切换会自动run syntactic check，算半自动吧。

下面是简要步骤:

0. get the vim, syntactic, pylint ready to go
1. install Vundle to vim
2. add ```Plugin '907th/vim-auto-save'``` between the ```call vundle#begin()``` and ```call vundle#end() ``` lines in .vimrc
3. run ```vim +PluginInstall +qall ``` in command line
4. add ```let g:auto_save = 1``` to .vimrc, to enable the AutoSave on Vim startup
5. open a python in Vim and set ```:AutoSave``` on to test

或者直接copy我的vimrc，里面把全局auto_save打开了，每次打开Vim会自动打开vim-auto-save

0. get the vim, syntactic, pylint, Vundle ready to go
1. copy mine vimrc to ~/.vimrc
2. run ```vim +PluginInstall +qall ``` in command line
3. open a python script to test, and enjor your debugging time

```

refer
* syntactic
* Vundle: https://github.com/VundleVim/Vundle.vim
* vim-auto-save: https://github.com/907th/vim-auto-save.vim
