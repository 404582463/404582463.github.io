---
layout:     post
title:      SHELL TOOLS AND SCRIPTING
subtitle:   Useful tools
date:       2022-07-24 				# 时间
author:     ZYD 						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - CS basis
---

## STRINGS
- string in terminal
  - use double quotes instead of single quotes to import string variables inside a string
  - ```sh
    $ echo "the word is $boo"
    ```
    
 - shell command - `source`
  - can be used to define a function into shell
    - ```sh
    $ sourch test.sh
    ```
    
- meaning of $0-$9
  - $0 is the script name
  - $1-$9 are the arguments
  - $@ - All the arguments
  - $# - Number of arguments
  - $? - Return code of the previous command
  - $$ - Process identification number (PID) for the current script
  - !! - Entire last command, including arguments. A common pattern is to execute a command only for it to fail due to missing permissions; you can quickly re-execute the command with sudo by doing sudo !!
  - $_ - Last argument from the last command. If you are in an interactive shell, you can also quickly get this value by typing Esc followed by . or Alt+.

- check the return value (0 for every thing is okay)
  - ```sh
  $ echo $?
  ```
  
  # operators
  - || (or operator)
    - usage: to conditionally execute commands, if the first halt condition if false then execute the second halfcode
  
  - ; (semicolon) 
    - used to concat multiple commands

- get the output of a command into a variable
  - ```sh
    $ foo=$(pwd) 
    ```
    
 - process substitution
   - <( CMD ) get the output of a CMD as a temp file

- redirecting
  - >, 2>(redirecting the stand error)
    - 0 is stdin
    - 1 is stdout
    - 2 is stderr

- script language
  - argv

- /dev/null
  - A special device in unix, data in it will be discard latter.
