---
title: Debug的使用
description: ' '
tags:
  - Java
  - 笔记
categories: Java
copyright: true
abbrlink: 3f0598a9
---

### Debug的使用 ：

#### 在IDEa或者在eclipse中,

#### 1.先点击要检查的代码前面，出现红点或蓝点表示标记成功,

#### 2.然后找到选项栏运行图标旁边的 ”Debug“ 

#### 3.点击之后下方窗口会出现控制栏,就可以调试或者一步一步点击下一步看代码运行状态和代码执行内容



```java
    public static void main(String[] args) {
        //打印五行三角形  5行
        for (int i = 1; i <= 5; i++) {
            for (int j = 5; j >= i; j--) {
                System.out.print(" ");
            }
            for (int j = 1; j <= i;j++){
                System.out.print("*");
            }
            for (int j =1 ; j<i;j++){
                System.out.print("*");
            }
            System.out.println();
        }

    }
}

```

