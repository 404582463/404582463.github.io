---
layout:     post   				    # 使用的布局（不需要改）
title:      VERSION CONTROL 			# 标题 
subtitle:   git #副标题
date:       2022-07-17 				# 时间
author:     ZYD 						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - CS BASIS
---

## git
nice underlying design but ugly interface
- what is git history
  a collectionf of files and folders with a top-level directory
  
tree(folders) blob(files)
objects
references(naming repository with human readable message)
HEAD -> what you are looking at

-  an example of how to use help command
   git help init
   
- Provide content or type and size information for repository objects
  ```sh
  git cat-file -p <object id>
  ```
- details: [official docs](https://git-scm.com/docs/git-cat-file)

git remote 
git push (push to remote)
