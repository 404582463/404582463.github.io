---
layout:     post   				    # 使用的布局（不需要改）
title:      SHELL BASIS 			# 标题 
subtitle:   Course overview + the shell #副标题
date:       2022-07-17 				# 时间
author:     ZYD 						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - CS Basis
    - The Missing Semester of Your CS Education
---

## BASIC OPERATIONS
### wrx permission on file and directory
- if no x permission on a dir, you can not find/see into/serch it.
- if no w permission on a dir, you can empty the dir but can not delete it.

### rm
- rm -all is defaultly not recurcive
- use rm -r to remove a directory
- rmdir only remove an empty directory

### directory names
better not to use a space in a directory name. For example, `mkdir directory one` will generate two directories instead of just one. 
Ether use `mkdir "directory one"` or `mkdir directory_one` as a better choice.

### OTHER HOTKEYS
ctrl+l for clear the terminal.

## STREAM
Defaultly, there are two streams: input and output. Keyboard is the most common input stream of terminal.
Likely, terminal is the most common output stream.

angle bracket and rewire

double end bracker (append instead of overwrite)

pipe character (chain different programs together)


## GO INTO KERNEL OF COMPUTER
cd sys
looks like a file system but not really is.

- change system parameters
  ```sh
  $ sudo echo 1000 > brightness (this will fail because sudo program does not know about how to open brightness)
  ```
  the correct way to do this is: (# pound symbol means run as root)
  ```
  $ # echo 1000 > brightness 
  ```

  or (run the following command as root)
  ```
  $ sudo su
  ```  
  
  or (tee means take the output of the last program as write to)
  ```
  $ echo 1000 | sudo tee brightness
  ```    
  
  ### xdg-open
  open a file in a proper way
