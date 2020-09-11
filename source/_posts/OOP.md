---
title: OOP
date: 2020-09-09 22:25:31
tags: 
- 编程语言
- 总结
categories: With Python
---

# 面向对象

面向对象三个特征：封装、多态、继承。

Python的面向对象：

<!-- more -->

* *Everything is Object.* 不同于Java和C++，Python没有内置类型，即int,float等都是对象。

* 类方法（Class Function）声明：方法的第一个参数为self（类比于Java里的this关键字）（相对于其他function）。

* 构造方法：定义`__init__`方法

  ~~~python
  def __init__(self, xxx):
  	xxxx
  ~~~

* 继承：构造方法子类需调用父类`__init__`方法。父类作为子类的参数（可以这么理解）

  ~~~python
  class Student(SchoolMember):
      '''xxx'''
  ~~~

* 成员变量：在类定义里定义的变量为Class Variable。方法里定义的为Object Variable。