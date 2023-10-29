---
title: Arrays集合
description: ' '
tags:
  - Java
  - 笔记
copyright: true
categories: Java
abbrlink: c3c27062
---

### Arrays类

- ##### 数组的工具类包名 java.util.Arrays

- ##### 由于数组对象本身并没有什么方法可以供我们调用，但API中提供了一个工具类Arrays供我们使用，从而可以对数据对象进行一些基本的操作。

- ##### 查看JDK帮助文档

- ##### Arrays类中的方法都是static修饰的静态方法，在使用的时候可以直接使用类名进行调用，而“不用”使用对象来调用（注意是"不用"而不是“不能”）

- #### 具有以下常用供能：

  - ##### 给数组赋值：通过fill方法。	

  - ##### 给数组排序：通过sort方法，按升序。

  - ##### 比较数组：通过equals 方法比较数组中元素值是否相等。

  - ##### 查找数组元素：通过binarySearch方法能对排序号的数组进行二分查找法操作。

 

#### 打印数组元素：

```java
public class ArratRes {
    public static void main(String[] args) {
        int [] array ;//定义一个数组
        array = new int [10];//创建了一个数组，这里面可以存放10个int类型的数字
    //给数组元素赋值
        array[0]=1;
        array[1]=2;
        array[2]=3;
        array[3]=4;
        array[4]=5;
        array[5]=6;
        array[6]=7;
        array[7]=8;
        array[8]=9;
        array[9]=10;
        System.out.println(Arrays.toString(array));
```

#### 集合类数组排序

```java
public class ArratRes {
    public static void main(String[] args) {
        int [] array ;//定义一个数组
        array = new int [5];//创建了一个数组，这里面可以存放10个int类型的数字
    //给数组元素赋值
        array[0]=1;
        array[1]=2;
        array[2]=3;
        array[3]=4;
        array[4]=5;
 Arrays.sort(array);
        System.out.println(Arrays.toString(array));
```

#### 数组填充

```java
import java.util.Arrays;

public class ArratRes {
    public static void main(String[] args) {
        int [] array ;//定义一个数组
        array = new int [10];//创建了一个数组，这里面可以存放10个int类型的数字
    //给数组元素赋值
        array[0]=10;
        array[1]=9;
        array[2]=8;
        array[3]=4;
        array[4]=5;
        array[5]=6;
        array[6]=3;
        array[7]=6;
        array[8]=7;
        array[9]=0;
        Arrays.sort(array);
        //给数组 二到第四个元素填充0
        Arrays.fill(array,2,4,0);
        System.out.println(Arrays.toString(array));

    }
}

```

