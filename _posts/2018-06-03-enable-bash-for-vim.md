---
layout: post
title: Enable bash for vim
categories: tips-and-tricks
date: 2018-06-03 13:50 +1000
---

**Vim** has been the editor of choice for many linux enthusiests. I wanted to show this plugin that helps you write your bash scripts. The plugin is by [WolfgangMehner](https://github.com/WolfgangMehner) and is called [Bash Support](https://github.com/WolfgangMehner/bash-support). If you are someone who writes production grade bash scritps that comply with the [bash style guide and coding standard](https://lug.fh-swf.de/vim/vim-bash/StyleGuideShell.en.pdf), this plugin will help you out alot.

> The same author of this plugin also wrote similar plugins for a bunch of other languages like C/C++, AWK, LaTex, Lua, etc.

### Installation

* You can download the plugin using
```shell
curl http://www.vim.org/scripts/download_script.php?src_id=24452 >/tmp/bash-support.zip
```

* If you dont have the `~/.vim` directory you will need to create that directory.
* go into that directory and then unzip the bash-support.zip which you downloaded.
```shell
# create the .vim directory if it dosent exist
mkdir ~/.vim
# go to that directory
cd ~/.vim
# unzip the bash-support.zip here
unzip /tmp/bash-support.zip ./
```

* In order to activate this, you will need to edit the `~/.vimrc`, add the following line if it dosent exist.
```vimrc
filetype plugin on
```

### Usage

This plugin is active only for files with the `.sh` extention. If you type `vim test.sh`, this file will have the plugin support. In order to configure the automatically generated header for bash scripts do as follows.

* `vim test.sh` this would have probably triggered the setup call, you can select option 1 which is 'personalization file (for your name, mail, ...), shared across plug-ins.
* Fill up the details as it would apply to you, and then `:wq`.
* Exit the current vim session as well `q!`.
* Open a new bash file again, `vim test.sh`. Now you should have your custom bash header.

![ generated-header ]({{"/assets/images/2018-06-03-enable-bash-for-vim/figure-generated-header.png" | abslute_url}})

#### Other useful bash-support commands

| MODE (Normal Mode) (Insert Mode) (Visual Mode) | COMMAND | DESCRIPTION |
|:-------------------------------:|---------|-------------|
| :white_check_mark::x::white_check_mark:| `\cfr` | insert framed comment |
| :white_check_mark::white_check_mark::white_check_mark: | `\sc` | switch case statement |
| :white_check_mark::white_check_mark::white_check_mark: | `\si` | if then fi |
| :white_check_mark::white_check_mark::white_check_mark: | `\sei` | if then else statement |
| :white_check_mark::white_check_mark::white_check_mark: | `\sf` | for in do done statement |
| :white_check_mark::white_check_mark::white_check_mark: | `\sfo` | for (()) do done statement |
| :white_check_mark::white_check_mark::white_check_mark: | `\sie` | if then else fi statement |
| :white_check_mark::white_check_mark::white_check_mark: | `\sw` | while do done statement | 
| :white_check_mark::white_check_mark::white_check_mark: | `\cfu` | function header *enter function name* |
| :white_check_mark::white_check_mark::white_check_mark: | `\sfu` | function statement *enter function name* |
| :white_check_mark::white_check_mark::white_check_mark: | `\se` | echo -e statement |
| :white_check_mark::white_check_mark::white_check_mark: | `\sp` | printf statement |
| :white_check_mark::white_check_mark::white_check_mark: | `\sa` | array statement |
| :white_check_mark::white_check_mark::white_check_mark: | `\rr` | save the file and run the script |
| :white_check_mark::white_check_mark::white_check_mark: | `\ra` | set the arguments for the file |
| :white_check_mark::white_check_mark::white_check_mark: | `\rd` | chmod +x on the script |
| :white_check_mark::white_check_mark::white_check_mark: | `\hh` | will provide documentation on the syntax |
| :white_check_mark::white_check_mark::white_check_mark: | `\hm` | will let you select all available docs on the command |


The uses I have listed above are the ones I find useful, you can find all the possible uses for this plugin over at the [github](https://github.com/WolfgangMehner/bash-support/blob/master/README.md) repository. Hope this can boost your bashscript productivity and help you on your journey to be a **GOD**.


