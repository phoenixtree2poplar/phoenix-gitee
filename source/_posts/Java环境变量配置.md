---
title: Java环境变量配置
date: 2019-03-07 12:55:58
tags:
	- java环境变量配置
	- jdk环境变量配置
---

## 安装java环境，选择安装目录，安装过程中会出现两次安装提示。
### 第一次是安装jdk，第二次是安装jre 。
### 建议两个都安装在同一个文件夹中的不同文件夹中。（不能都安装在java文件夹的根目录下，jdk和jre安装在同一文件夹会出错
#### 1.安装jdk 根据个人喜好选择安装目录
#### 2.安装jre 根据个人喜好选择安装目录
###### 注：若无安装目录要求，可全默认设置。无需做任何修改，两次均直接点下一步。
## 安装完JDK后配置环境变量  计算机→属性→高级系统设置→高级→环境变量 
#### 1.系统变量→新建JAVA_HOME变量，变量值填写jdk的安装目录（本人是 D:\Java\jdk1.7);
#### 2.系统变量→寻找 Path 变量→编辑，在变量值最后输入 %JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;
#### (注意原来Path的变量值末尾有没有;号，如果没有，先输入；号再输入上面的代码)
#### 3.系统变量→新建 CLASSPATH 变量，变量值填写   .;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar(注意最前面有一点);
#### 4.系统变量配置完毕,检验是否配置成功，运行cmd输入：
```cmd
java -version  //java 和 -version 之间有空格
```