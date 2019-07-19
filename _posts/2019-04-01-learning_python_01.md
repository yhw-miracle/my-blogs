---
layout: post
title: learning_python_01
date: 2019-04-01 19:28:14 +0800
tags: [python,]
categories: 知识总结
author: yhw-miracle
---

> 本文为`yhw-miracle`原创文章，可以随意转载，但需注明出处。

### `python`介绍
* 解释型编程语言
* `python`单行注释`#`
* `python`多行注释`"""`与`"""`
* `# TODO`说明文字

### 变量、关键字
* 变量用于描述计算机中的数据存储空间，作用是在计算机内存中保存数据。
* 变量名的命名规则是由数字、字母和下划线组成，不能以数字开头，不能是关键字，区分大小写。
* 下划线连接，驼峰命名法
* 关键字

```python
import keyword
print(keyword.kwlist)
```

![](/images/2019/Apr/01.png)

### 标准输入输出
* 输入：input()

* 输出
> * print()
> * %s，字符串占位符
> * %d，整数占位符
> * %f，浮点数占位符
> * %%，输入\`%\`

### python运算
* 字符串运算
> * `+`：拼接
> * `*`：连续拼接

* 算术运算符
> * `+`，加
> * `-`，减
> * `*`，乘
> * `/`，除
> * `//`，整除
> * `%`，取余
> * `**`，乘方
> * 优先级，乘方 > [乘，除，整除，取余] > [加，减]

* 赋值运算符
> * =，赋值
> * +=，加后赋值
> * -=，减后赋值
> * *=，乘后赋值
> * /=，除后赋值
> * //=，整除后赋值
> * %=，取余后赋值
> * **=，次方后赋值

* 比较运算符
> * \>，大于
> * \>=，大于等于
> * <，小于
> * <=，小于等于
> * !=，不低于
> * ==，等于
> * 查看字母和数字的`ASCII`值
> * 查看`ASCII`值：ord()
> * 已知`ASCII`值查看对应的字符：chr()

* 关系运算符（逻辑运算符）
> * and：短路与，左操作数为`False`，表达式结果为`False`，与`左`操作数`bool`值相同。 
> * or：短路或，左操作数为`True`，表达式结果为`True`，与`左`操作数`bool`值相同。
> * not

	* 一些例子
	> * 1 and True => True
	> * 0 and True => 0
	> * 1 or True => 1
	> * 0 or True => True
	> * 1 and False => False
	> * 0 and False => 0
	> * 1 or False => 1
	> * 0 or False => False
	> ___
	> * True and 1 => 1
	> * True and 0 => 0
	> * True or 1 => True
	> * True or 0 => True
	> * False and 1 => False
	> * False and 0 => False
	> * False or 1 => 1
	> * False or 0 => 0

### 三大语句
* 顺序语句：自上而下执行语句

* 分支语句
> * if...
> * if...else...
> * if...elif...else...
> * 分支嵌套

* 循环结构
> * while
> * for...in...
> * for...in...else...，循环正常结束后执行`else`部分。
> * while...else...
> * break，终止循环的执行
> * continue，终止本轮循环的执行
> * range(m, n, s): 生成 m（默认为0） 到 n-1 的整数，整数间隔为 s（默认为1）。
> * 推导式的使用
> ```python
> list1 = [data for data in range(5)]
> list1 = [data**2 for data in range(5)]
> list1 = [data for data in range(5) if data > 2]
> ```
