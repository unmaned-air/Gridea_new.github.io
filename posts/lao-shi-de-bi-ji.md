---
title: '老师的笔记'
date: 2022-09-02 00:00:35
tags: [大二课程]
published: true
hideInList: false
feature: /post-images/lao-shi-de-bi-ji.jpg
isTop: false
---
# 1 Java环境搭建

## 1.1 JDK下载

www.oracle.com

安装后的路径：

![1661866604481](Java环境搭建.assets/1661866604481.png)

## 1.2 设置环境变量

当我们执行一个命令的时候，搜索顺序就是当前路径和path环境变量下面的路径（依次去找）

![1661866702563](Java环境搭建.assets/1661866702563.png)

1.2.1 path路径的设置

**创建一个JAVA_HOME的环境变量**：C:\Program Files\Java\jdk-11.0.16.1

![1661866661564](Java环境搭建.assets/1661866661564.png)



**设置环境变量path**

![1661866756770](Java环境搭建.assets/1661866756770.png)

**常见的DOS命令：**

| dir      | 显示当前目录下面的内容       |
| -------- | ---------------------------- |
| C:/D:    | 切换硬盘分区                 |
| cd\      | 进入当前分区的根目录         |
| cd..     | 进入当前目录的上一层目录     |
| cd .     | 当前路径                     |
| cd  dell | 进入当前目录的子目录dell下面 |
|          | 相对路径和绝对路径的区别     |
|          |                              |
|          |                              |
|          |                              |

# 2 第一个Java程序

**第一步：编写java源程序**

```
//第一个Java程序，位置D:\code\javacode\first.java
class A{
}
class B{
}
class C{
}
```

**第二步：编译源程序(Javac)：**

```
javac 源文件的文件名.java（扩展名必须为.java)
```

编译生成字节码文件



![1661863612975](Java环境搭建.assets/1661863612975.png)

**第三步：运行字节码文件(java)**

```
java 字节码文件名（不包含扩展名）

D:\code\javacode>java A
错误: 在类 A 中找不到 main 方法, 请将 main 方法定义为:
   public static void main(String[] args)
否则 JavaFX 应用程序类必须扩展javafx.application.Application
```



当类A加一个修饰符public，此时编译无法通过。

```
D:\code\javacode>javac first.java
first.java:2: 错误: 类 A 是公共的, 应在名为 A.java 的文件中声明
public class A{
       ^
1 个错误
```

**总结一下：**

1.  一个源文件中可以有很多类。
2. 编译源文件，生成字节码文件，有多少类就生成多少字节码文件。
3. 一个源文件中只能有一个public类。
4.  有public类的源文件的文件名必须与public类名一致。
5.  main方法的修饰符 public static void，String

A. public static int main(String[]args)    错

B. public static void Main(String[]args)  错

C. public static void main(string[]args)  错

D. public static void main(String args)  错

E. public static void main(String [] a)   对