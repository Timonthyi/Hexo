---
title: learningCPP
date: 2020-07-10 21:32:15
tags:
categories: Trip to C++
---


# 7.10

## 所学的主要知识点：*map*容器

## 知识点解析

- *map*是一个**键-值**型容器，它的每一个元素由一个*key*和一个*value*组成。
  *key*用于检索*value*的值，因此*map*不可以用下标来访问元素。
  
- *map*的*iterator*是*pair*类型，即*pair*< *const* K, V >。

  ### *pair*类型 

  - 由*first*和*second*两个元素组成的集合。
  - 构造函数*make_pair(A, B)*

- *map*的下标访问与*insert*成员函数在查找目标元素时，如果目标元素不存在则**自动创建**由相应*key*和*value*(默认构造函数或0)的元素。

- *map*的元素*key*值必须定义<运算，因为*key*值需要比较