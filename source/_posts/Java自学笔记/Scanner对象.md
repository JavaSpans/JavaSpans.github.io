---
title: Scanner对象
description: ' '
tags:
  - Java
  - 笔记
categories: Java
copyright: true
abbrlink: e2abe5ec
---

### Scanner对象

####   是实现人机交互的工具类，通过Scanner类来获取用户的输入。

#### 基本的语法：

```java
//创建一个扫描器对象，用于接收键盘数据
Scanner s = new Scanner(System.in)
```

 

#### 通过Scanner类的next()与nextLine()方法获取输入的字符串，在读取前我们一般需要使用 hasNext()与hasNextLine()来判断是否还有输入的数据

```java
//判断用户有没有输入字符
if(Scanner.hasNext()){
//使用next方式接收
String str = Scanner.next();
System.out.println("输出的内容为"+str)
}
//凡是属于IO流的泪如果不关闭会一直占用资源，要养成好习惯用完就关掉
scanner.close();
```

##### next():

##### 1. 一定要读取到有效字符后才可以结束输入。

##### 2. 对输入的有效字符之前遇到的空白，next()方法会自动将其去掉。

##### 3. 只要有输入有小字符后才将其后面输入的空白作为分隔符或者结束符。

#####  4. next()不能得到带有空格的字符串。

#### nextLine();

##### 1. 以回车位结束符，也就是说nextLine()方法返回的是输入回车之前的所有字符。

##### 2. 可以获得空白



