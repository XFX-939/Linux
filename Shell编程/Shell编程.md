## 什么是Shell脚本？

Shell脚本（英语：Shell script）是一种电脑程序与文本文件，内容由一连串的shell命令组成，经由Unix Shell直译其内容后运作。被当成是一种脚本语言来设计，其运作方式与直译语言相当，由Unix shell扮演命令行**解释器**的角色，**在读取shell script之后，依序运行其中的shell命令，之后输出结果**。利用Shell script可以进行系统管理，文件操作等。

例子：

```shell
#!/bin/sh    
cd ~
mkdir shell_tut
cd shell_tut

for ((i=0; i<10; i++)); do
    to
```

### 实例解析：

- 第1行：指定脚本解释器，"#!"是一个约定的标记，它告诉系统这个脚本需要什么解释器来执行，这里是用/bin/sh做解释器的。
- 第2行：切换到当前用户的home目录
- 第3行：创建一个目录shell_tut
- 第4行：切换到shell_tut目录
- 第5行：循环条件，一共循环10次
- 第6行：创建一个test_1…10.txt文件
- 第7行：循环体结束

cd, mkdir, touch都是系统自带的程序，一般在/bin或者/usr/bin目录下。for, do, done是sh脚本语言的关键字。



## 环境

### Linux

Linux默认安装就带了shell解释器。

### Mac OS

Mac OS不仅带了sh、bash这两个最基础的解释器，还内置了ksh、csh、zsh等不常用的解释器。

### Windows上的模拟器

windows出厂时没有内置shell解释器，需要自行安装，为了同时能用grep, awk, curl等工具，最好装一个cygwin或者mingw来模拟linux环境。

- [cygwin](http://www.cygwin.com/)
- [mingw](http://www.mingw.org/)



## 解释器：

###### 是一种电脑程序，能够把高级编程语言**一行一行直接转移运行**。解释器不会一次把整个程序转译出来，只像一位“中间人”，每次运行程序时都要先转成另一种语言再作运行，因此解释器的程序运行速度比较缓慢。它每转译一行程序叙述就立刻运行，然后再转译下一行，再运行，如此不停地进行下去。

Python、Shell、MATLAB都是这种形式



### 脚本解释器

### sh

即Bourne shell，POSIX（Portable Operating System Interface）标准的shell解释器，它的二进制文件路径通常是/bin/sh，由Bell Labs开发。

### bash

Bash是Bourne shell的替代品，属GNU Project，二进制文件路径通常是/bin/bash。业界通常混用bash、sh、和shell，比如你会经常在招聘运维工程师的文案中见到：熟悉Linux Bash编程，精通Shell编程。

### 高级编程语言

理论上讲，只要一门语言提供了解释器（而不仅是编译器），这门语言就可以胜任脚本编程，**常见的解释型语言都是可以用作脚本编程**的，如：Perl、Tcl、Python、PHP、Ruby。Perl是最老牌的脚本编程语言了，Python这些年也成了一些linux发行版的预置解释器。**（MAC就内置了Python）**

**编译型语言，只要有解释器，也可以用作脚本编程**，如C shell是内置的（/bin/csh），Java有第三方解释器Jshell。

```php
#!/usr/bin/php
<?php
for ($i=0; $i < 10; $i++) {
    echo $i . "\n";
}
```

执行：

```shell
/usr/bin/php test.php
```

或者：

```shell
chmod +x test.php
./test.php
```