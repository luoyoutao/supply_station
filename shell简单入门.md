shell是一种脚本语言（写好可以直接运行，不用编译），下面的简单教程参考链接：https://space.bilibili.com/254507574  

1、新建shell脚本  
在linux中，创建一个shell脚本。touch run.sh。  

2、编写第一行  
\#!/bin/bash  
第一行，井号感叹号，表示用什么来执行  

3、打印输出（变量）  
打印简单的输出语句：echo "hello world!"  
打印变量（**注意变量赋值不能有空格。且引用变量用${}**）：  
name="supply_station"  
echo ${name}  
**还得注意，单引号不能引用变量的值，双引号才可以。例如下面两条语句的输出不同：**  
echo 'my name is \$ \{name\}'的打印结果为 my name is \$\{name\}     
echo "my name is ${name}"的打印结果为 my name is supply_station  
**如果不希望变量被更改，可以用readonly在变量前面修饰**  
删除变量：unset 变量名  

4、赋予权限并运行脚本  
退出后，给其赋权限，命令：chmod +x run.sh  
然后运行命令：./run.sh  

5、输入  
read -p "请输入内容" n。-p是给一个提示，输入到n中。  

6、注释  
用#井号注释一行，用:<<EOF    EOF注释一段  

7、取字符串的一些属性  
name="hello world"  
打印长度：echo ${#name}  
截取字符串：echo ${name:2:3}，打印name\[2:3]  
