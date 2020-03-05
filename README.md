

# 项目内容

分数的运算，包括支持假分数的输入方式（整数部分实现无限位数的读入，分子分母有限位存储）

## 输入

1.键盘输入

用户可以输入任何数的空格符（‘ ’）、制表符（‘\t’）、换行符（‘\n’）。正分数的输入是要求形如“xxx+xxx/xxx”，负分数的输入要求形如“-(xxx+xxx/xxx)”。（注意负分数的括号一定要求是用英文输入法输入的，否则程序就会报错）。用户输入“=”后，按回车即可。若表达式正确，在计算完成后，可以选择将用户输入的表达式存入文件中（若是已存在的文件，将会把原内容覆盖）。文件名由用户自行输入。若表达式不正确，那么自动清除用户输入内容，当然，也不能将用户输入内容进行存入文件这一操作。  

2.读取文件

文件名由用户自行输入。文件表达式要求与键盘输入的要求相当。若表达式有多个的话，只能读入第一个表达式。若表达式有错误的话，将打印程序读取文件到哪一步，提示用户错误表达的位置。  

## 函数模块

1.整数部分`integer.h`

该部分是用来实现分数里面整数部分的加减计算，数据的整理（进位、退位）等相关操作，作为分数运算的基础，为fraction文件中函数的执行提供计算支持。

2.分数部分`fraction.h `

该部分是用来实现读入用户输入的所有分数，并对分数进行整理约分的优化。除此之外，并对分数进行计算，得到最终的答案，并与用户读入情况经整理后一同打印。

3.文件部分`file.h`

该部分是用来从文件中读入表达式，存入内存，方便后续操作。其内容主体与`fraction.h`中的读入函数作用类似。此外，还可以将内存中链表所存储的表达式存储到文件中。  

4.通分部分`tongfen.h`

该部分是用来展示通分的具化过程，进行信息打印。要求的是并进行整理，并进行打印，相当于是将`fraction.c`中多个函数的整合使用。  

## 效果展示

程序菜单界面

![程序菜单界面](F:\CodeBlocks(workshop)\作业\大作业\U201713511\fraction\fig\程序菜单界面.png)

操作1

![操作1](F:\CodeBlocks(workshop)\作业\大作业\U201713511\fraction\fig\操作1.png)

操作2

![操作2](F:\CodeBlocks(workshop)\作业\大作业\U201713511\fraction\fig\操作2.png)

操作3

![操作3](F:\CodeBlocks(workshop)\作业\大作业\U201713511\fraction\fig\操作3.png)

