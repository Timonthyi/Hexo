---
title: C++：智能指针
date: 2021-03-08 11:13:00
tags: 
- 编程语言
categories: C++
---

智能指针的定义、如何实现以及C++STL库中智能指针的使用。<!--more-->

## 什么是智能指针？

智能指针与普通类行为相似，由用户创建的对象，最后由智能指针负责删除。

智能指针解决了指针之间复制控制问题，提高了程序的安全性。

![](https://i.loli.net/2021/03/08/xZTbnQOok8aEW56.png)

## 如何实现智能指针？

常用的实现智能指针的方法（<<C++ Primer 4th Edition>>中）是==使用计数==，使用一个计数器来记录指向一个对象的指针个数。具体实现如下：

```C++
#include <iostream>

class SmartPtr
{
private:
    int val;
    U_ptr *u_ptr;
public:
    SmartPtr(int* p, int i): val(i), u_ptr(new U_ptr(p)){ };
    SmartPtr(const SmartPtr& orig):u_ptr(orig.u_ptr), val(orig.val){
        ++u_ptr->use;
    };
    SmartPtr& operator=(const SmartPtr&);
    ~SmartPtr(){
        if (--u_ptr->use == 0)
        {
            delete u_ptr;
        } 
    };
};

SmartPtr& SmartPtr::operator=(const SmartPtr& rhs)
{
    rhs.u_ptr->use++;
    if (--u_ptr->use == 0)
    {
        delete u_ptr;
    }
    u_ptr = rhs.u_ptr;
    val = rhs.val;
    return *this;
}
class U_ptr
{
    int* ip;
    size_t use;
    U_ptr(int* p): ip(p), use(1){ };
    ~U_ptr();
    friend class SmartPtr;
};

U_ptr::~U_ptr()
{
    delete ip;
}
```

通过一个U_ptr的类实现计数器功能，每新增一个指针，使用use变量记录。SmartPtr类的构造函数、复制构造函数和赋值操作符都得自定义。

## STL中的智能指针

定义在memory头文件中。

- ~~auto_ptr（deprecated）~~
- unique_ptr
- shared_ptr

auto_ptr与unique_ptr原理相同，保证最终只有一个指针指向对象。它们的不同之处在于unique_ptr能够在编译阶段报错，以及编译器允许unique_ptr短暂存在（可存在于右值）。

shared_ptr采用使用计数的原理实现。

使用示例程序：

```c++
#include <iostream>
#include <memory>

std::unique_ptr<std::string> demo(std::string s)
{
    std::unique_ptr<std::string> temp(new std::string(s));
    return temp;
}
int main()
{
    // std::auto_ptr<std::string> a(new std::string("hi"));		//1
    // std::auto_ptr<std::string> b = a;						//2
    // std::unique_ptr<std::string> a(new std::string("hi"));	//3
    // std::unique_ptr<std::string> b(demo("Hello"));			//4
    std::shared_ptr<std::string> a(new std::string("hi"));		//5
    std::shared_ptr<std::string> b = a;							//6
    std::cout << *b << std::endl;								//a
    std::cout << *a << std::endl;								//b
    return 0;
}
```

运行1+2+a+b时，编译通过，运行报错（Segmentation fault）。

运行3+4+a+b时，编译通过，运行结果符合要求。

运行5+6+a+b时，编译通过，运行结果符合要求。

## 参考博文

https://www.cnblogs.com/lanxuezaipiao/p/4132096.html

