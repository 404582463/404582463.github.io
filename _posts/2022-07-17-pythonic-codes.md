---
layout:     post
title:      HOW TO WRITE PYTHONIC CODES
subtitle:   Useful tools
date:       2022-07-18 				# 时间
author:     ZYD 						# 作者
header-img: img/python_background.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - Python basis
---

# Useful Tools

## tool for check if code is pythonic
- [Pylint documentation](https://pylint.pycqa.org/en/latest/tutorial.html)

- yacs
  This tool can be used for config management
  ```py 
  # here is how to use
  from yacs.config import CfgNode as CN

  # -----------------------------------------------------------------------------
  # Config definition
  # -----------------------------------------------------------------------------

  _C = CN()
  _C.MODEL = CN()
  _C.MODEL.DEVICE = "cuda"
  _C.MODEL.WEIGHT = ""
  _C.MODEL.PRETRAIN = True
  _C.MODEL.USE_SYNC_BN = False
  _C.MODEL.REDUCE_LOSS_NORM = True
  _C.MODEL.NORM = 'BN' # group normalization or batch normalization

  _C.MODEL.INPLACE_ABN = False


## Extension for vscode
- Grammarly
