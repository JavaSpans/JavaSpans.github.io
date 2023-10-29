---
title: java学校笔记数据类型结构
description: ' '
tags:
  - Java
  - 学校笔记
categories: Java
copyright: true
abbrlink: 37015d6b
---

```java
package 学习内容;

import java.util.Scanner;

public class 数据类型结构 {
	public static void main(String[] args) { 
		//1.数据类型：基本数据类型、引用数据类型
		/*基本数据类型：四种八类
		 * （1）整数类型（byte、short、int、long）
		 * （2）浮点数类型（float、double）
		 * （3）字符类型（char）
		 * （4）布尔类型（boolean）
		 */
		

​	//(1)整数类型
​	/*

  * byte：字节型，一个字节（占8位），范围：-2^7~2^7-1   -128~127,默认值0

    * short:短整型，二个字节（占16位），范围：-2^15~2^15-1,默认值0
     * int：整型，Java中默认的整数类型，四个字节（占32位），范围：-2^31~2^31-1,默认值0
     * long:长整型，八个字节（占64位），范围：
       */

    //（2）浮点型
    /*

     * 单精度浮点型：float，默认值0.0f，四个字节（占32位）
     * 双精度浮点型：double，默认值0.0d，八个字节（占64位）
     * */

    //（3）字符类型
    /*

     * char:0~65535或'\u0000'~'\uffff',默认值0或\u0000
       */
       //(4)布尔类型
       /*
     * boolean:true flase
       */

    //2.变量：内存单元
    Scanner scan = new Scanner(System.in);
    int score = 0;
    score = scan.nextInt();

}
}


```

