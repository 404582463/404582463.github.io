---
layout:     post
title:      DEBUGGER AND PROFILER
subtitle:   Python debugger, profiler visualization tools
date:       2022-07-18 				# 时间
author:     ZYD 						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - CS BASIS
    - The Missing Semester of Your CS Education
---

## debugger
- python -m ipdb program.py
  - c continue
  - b set breakpoint
  - p print 
    - p locals: show all the variables at that step 
  - s ???
- gdb for C/C++
- sudo strace for tracking system calls?

## analysis
- static analysis tools for python - pyflakes/mypy
  - using IDE like vscode, these funcionalities (maybe only a part of all) are usually built-in
- statci analysis tools for English - writegood

## profiling
optimize the code by consider the cpu/memory/network, etc.
### time
- terminology: real time, user time, system time
  - real time: the entire time
  - user time: the time your program spent on the cpu doing user level cycles
  - system time: the time your program spent on the cpu executing kernel mode instructions
- bash command `time` can show the time to execute an program with the three metrics

### profilers
- tracing profilers and sampling profilers
  - sampling profilers are useful when you execute your program for long enough, you can find out where most of the time is being spent.
  - tracing profilers will add a lot of overhead, but more accurate
- cpu profiler: kernprof(line profiler)
- memory profiler: memory_profiler
- strace for debugging and trouble shooting programs in Unix-like operating systems such as Linux.
  - [offical website](https://strace.io/)

### Visulazation tools
- cpu analysis
  - [Flame graph](https://www.brendangregg.com/flamegraphs.html)
- program flow analysis
  - [call graph (or control flow graphs)](http://pycallgraph.slowchop.com/en/master/)
  - really useful to deal with io-related problem

### Resource Monitoring
some of them are mainly for linux env. With other env like windows, maybe there are other better visulization tools.
- process viewer
  - [htop](https://htop.dev/)
  - [glances](https://nicolargo.github.io/glances/)
- disk usage
  - [ncdu (NCurses Disk Usage)](https://dev.yorhel.nl/ncdu)
  - ```sh
    du -h .\videos
    ```

    > General Monitoring - Probably the most popular is htop, which is an improved version of top. htop presents various statistics for the currently running processes on the system. htop has a myriad of options and keybinds, some useful ones are: <F6> to sort processes, t to show tree hierarchy and h to toggle threads. See also glances for similar implementation with a great UI. For getting aggregate measures across all processes, dstat is another nifty tool that computes real-time resource metrics for lots of different subsystems like I/O, networking, CPU utilization, context switches, &c.

    > I/O operations - iotop displays live I/O usage information and is handy to check if a process is doing heavy I/O disk operations

    > Disk Usage - df displays metrics per partitions and du displays disk usage per file for the current directory. In these tools the -h flag tells the program to print with human readable format. A more interactive version of du is ncdu which lets you navigate folders and delete files and folders as you navigate.

    >Memory Usage - free displays the total amount of free and used memory in the system. Memory is also displayed in tools like htop.

    > Open Files - lsof lists file information about files opened by processes. It can be quite useful for checking which process has opened a specific file.

    > Network Connections and Config - ss lets you monitor incoming and outgoing network packets statistics as well as interface statistics. A common use case of ss is figuring out what process is using a given port in a machine. For displaying routing, network devices and interfaces you can use ip. Note that netstat and ifconfig have been deprecated in favor of the former tools respectively.

    > Network Usage - nethogs and iftop are good interactive CLI tools for monitoring network usage.

  
### performance comparing
- Specialized tools
  - [hyperfine](https://github.com/sharkdp/hyperfine)
