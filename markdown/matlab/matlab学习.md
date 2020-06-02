# matlab概述

​    matlab系统由开发环境、数学函数库、编程语言、图形处理系统和应用程序接口(*API*)五大部分组成。



## 路径搜索

​    matlab提供了专用的路径搜索器，用来搜索存储计算机的内存或硬盘中的M文件和其他相关文件，默认情况下搜索路径包含所有matlab自带的文件。

添加搜索路径

![image-20200601172050382](C:\Users\12520\AppData\Roaming\Typora\typora-user-images\image-20200601172050382.png)

``` matlab
path %列出搜索路径
pathtool %打开设置路径窗口，和点击上面搜索路径效果一样
%其他方法感觉没窗口方便
```



## *DEMOS*

​	matlab提供了直观的DEMOS演示，可以帮助学习。

![image-20200601173446541](C:\Users\12520\AppData\Roaming\Typora\typora-user-images\image-20200601173446541.png)

```matlab
demo
demos
```







# matlab基础



## matlab数据类型

matlab默认浮点数类型为双精度

matlab中单精度类型不能与整数类型直接运算

双精度类型与其他类型运算结果类型由其他类型来决定

matlab中eps可以视为0

[数据类型](https://www.cnblogs.com/bky-lx/p/10513568.html)



### 取整函数

``` matlab
floor(1.5) %向下取整,1
ceil(1.5) %向上取整,2
round(-1.5) %取向最近的整数，向绝对值较大的方向，-2
fix(1.5) %向0取整
```



### 查看类型的最大最小值

``` matlab
realmax('single')
realmin('double')
```



## 结构

### 创建和访问结构对象

通过字段赋值创建结构对象

~~~ matlab
student.name = 'huangyaosen';%创建一个对象名为student，其中一个字段为name，值为huangyaosen
student.grade = 100;
student.birthday = [1996 12 25];
~~~

使用struct函数创建结构对象

~~~ matlab
student = struct('name','haungyaosen','grade',100,'birthday',[1996 12 25]);
~~~

访问通过**对象名.字段**访问内容

结构对象内可以存储多个对象

~~~ matlab
student(1) = struct('name','haungyaosen','grade',100,'birthday',[1996 12 25]);
student(2) = struct('name','zhangsan','grade',60,'birthday',[1998 10 21]);
~~~



