# Java-5
Java课程作业项目仓库
# 实验五 模拟学生作业处理
## 一.实验目的
1. 掌握字符串String及其方法的使用 
2. 掌握文件的读取/写入方法
3. 掌握异常处理结构
## 二.实验要求
在某课上,学生要提交实验结果，该结果存储在一个文本文件A中。 文件A包括两部分内容： 一是学生的基本信息； 二是学生处理后的作业信息，该作业的业务逻辑内容是：利用已学的字符串处理知识编程完成《长恨歌》古诗的整理对齐工作，写出功能方法，实现如下功能：
1. 每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
2. 允许提供输入参数，统计古诗中某个字或词出现的次数
3. 输入的文本来源于文本文件B读取，把处理好的结果写入到文本文件A
4. 考虑操作中可能出现的异常，在程序中设计异常处理程序 要求：
5. 设计学生类（可利用之前的）；
6. 采用交互式方式实例化某学生；
7. 设计程序完成上述的业务逻辑处理，并且把“古诗处理后的输出”结果存储到学生基本信息所在的文本文件A中。
## 三.实验设计
先创建student类和Test类，重新写了student类，定义txt2String方法读取文件，定义一个BufferedReader对象来读取文件，使用while语句，用readLine语句读取文件，一次读一行，定义字符串变量s，按行读取文件，读到空行，停止读取，再关闭文件，捕捉异常，若出现错误，返回错误的行数，一字符串形式返回对象，定义布尔类型的写入文件方法，设置布尔型变量flag的值为false,定义新的PrintWriter对象，写入内容后关闭文件,改变flag的值为true，捕捉异常后返回flag,写main方法，通过Scanner方法建立对象，并获取用户输入键盘值，来完成交互操作，让用户自主填写个人信息，并打印个人信息，把读取的内容通过.toCharArray()方法转换为数组，定义空字符串，用for语句把数组的每一个元素赋值给s，并利用if语句查找能整除7不能整除2的字符位置，加上逗号，能被2整除也能被7整除的位置加上句号，用while(true)语句写入选择功能，用户通过键盘输入，选择查询字或词的出现次数或退出程序，利用switch语句完成功能的选择，通过indexOf语句查找用户输入的指定字或词，找到后count变量加1，如果选择功能输入错误，输入default语句，如果选择功能每输入int型，输出catch语句。
## 四.核心代码
对文本文件进行标点符号的添加
