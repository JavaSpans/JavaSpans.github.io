---
title: java学校笔记Static关键字和代码块
description: ' '
tags:
  - Java
  - 学校笔记
categories: Java
copyright: true
abbrlink: 8c6f2d57
---

```java
package 学习内容;
// static 修饰的变量属于对象共享的数据，属于静态变量不在再是成员变量。
/*
 * static 修饰的变量是属于类的 ，而不是属于对象的。
 * static 修饰的方法属于静态方法。
 * 所以访问静态方法以及静态变量有两种方法：
 * 1.通过对象访问
 * 2.通过类目访问--推荐使用
 * 没有创建对象时，静态方法以及静态变量依然存在。
 * 3.静态无法访问成员变量以及成员方法
 * 静态方法只能访问静态方法以及静态变量。
 * 成员方法可以访问静态方法以及静态变量。
 * 
 * 
 * 静态代码块 
 * 1.静态代码块的执行优先于构造方法,在创建对象时优先执行。
 * 2.静态代码块只在创建第一次对象的时候执行一次。
 * 
 * 格式：
 * static{
 * 
 * 	}
 * */
public class Static关键字和代码块 {
	public Static关键字和代码块() {
		
	}

public Static关键字和代码块(int sTuNo, String name, int age) {
	super();
	this.sTuNo = sTuNo;
	this.name = name;
	this.age = age;
}
int sTuNo;
String name;
int age ;
static int room;
@Override
public String toString() {
	return "Stydent [sTuNo=" + sTuNo + ", name=" + name + ", age=" + age + "]";
}

}

```

