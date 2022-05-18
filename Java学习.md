# Java学习

## <center>JAVA入门</center>

<u>asassas</u>

[JAVA韩顺平讲师](https://www.bilibili.com/video/BV1fh411y7R8?from=search&seid=8239657508154822384&spm_id_from=333.337.0.0)

[TOC]



### <center>dos指令</center>



​		cmd,DOS命令，计算机术语，是指DOS操作系统的命令，是一种面向磁盘的操作命令，主要包括目录操作类命令、磁盘操作类命令、文件操作类命令和其它命令。

<img src="https://bkimg.cdn.bcebos.com/pic/d4628535e5dde71194700d64adefce1b9c166185?x-bce-process=image/watermark,image_d2F0ZXIvYmFpa2U5Mg==,g_7,xp_5,yp_5/format,f_auto" alt="img" style="zoom:50%;" />



```
->javac Test.java  \\编译
->java Test.class  \\运行
->dir			\\显示目录
->cd  D:\		\\切换到指定目录
->cd /D C:\		\\其他盘切换到C盘
->tree D:\		\\文件树目录
->cls           \\清屏
->exit			\\退出tos
->md D:\\XXX    \\创建目录
->rd			\\删除
```



![image-20220307153723226](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220307153723226.png)

![image-20220307154140907](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220307154140907.png)

![image-20220307154717255](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220307154717255.png)

### java语言的重要特点

1.java语言是**面向对象的（oop）**

2.java语言是**健壮**的，java的强类型机制、异常处理、垃圾的自动收集等是java程序健壮性的重要保证

3.java语言是**跨平台性**的

​	解释：java文件**编译**成class文件，class文件可以在**windows平台**运行也可以在**Linux平台**上运行

4.java语言是解释型的

解释性语言:javascript,PHP,java 编译型语言：c/c++ 

区别：

解释性语言：编译后的代码，不能直接被机器执行，需要解释器执行（**class文件需要解释执行**）

编译性语言：编译后的代码，可以直接被机器执行，c/c++，（**编译后的代码即为二进制代码**）

##### ```1月25日 初始———小记```

​		我已经浪费了太多时间了，时间流逝的很快。我还有一个月的时间让我进步，一个月以后的开学将见证一些事情的发生，希望到时候的我不会后悔，我后悔的事情已经太多太多，但愿我能成为我想成为的人。今天就先到这里了，明天加油。

| 今日完成事宜 | 完成情况 |
| ------------ | -------- |
| Typora入门   | 完成良好 |

| 明日完成目标 | 完成情况 |
| ------------ | -------- |
| JAVA基础复习 | 待完成   |
| VS code上手  | 待完成   |

***



### Java运行机制及运行过程

#### JVM——JAVA虚拟机

1.**JVM是Java Virtual Machine（[`Java虚拟机`](https://baike.baidu.com/item/Java虚拟机/6810577)）的缩写**，具有指令集并使用不同的存储区域。负责执行指令，管理数据，内存，寄存器，包含在JDK中。

2.对于不同的平台，有不同的虚拟机（即需要安装不同的JVM）

因为有了JVM，同一个JAVA程序在三个平台都可以运行

3.JAVA虚拟机机制屏蔽了底层运行平台的差别，实现了`一次编译，到处运行`

#### JDK——JAVA开发工具包

1.JDK的全称（Java Development Kit   `JAVA开发工具包`）

JDK=JRE+java的开发工具[java,javac,javadoc,javap等]

2.JDK是提供给开发人员使用的，其中包含了java的开发工具，也包括了jre，所以安装了jdk，就不用再单独安装jre了

**JDK包含的基本组件包括**：

javac – 编译器，将源程序转成字节码

jar – 打包工具，将相关的类文件打包成一个文件

javadoc – 文档生成器，从源码注释中提取文档

jdb – debugger，查错工具

java – 运行编译后的java程序（.class后缀的）

appletviewer：小程序浏览器，一种执行[HTML文件](https://baike.baidu.com/item/HTML文件)上的Java小程序的Java浏览器。

Javah：产生可以调用Java过程的C过程，或建立能被Java程序调用的C过程的头文件。

Javap：Java反汇编器，显示编译类文件中的可访问功能和数据，同时显示[字节代码](https://baike.baidu.com/item/字节代码)含义。

Jconsole: Java进行系统调试和监控的工具

[![img](https://bkimg.cdn.bcebos.com/pic/7af40ad162d9f2d36880ccf1a3ec8a136327cc1f?x-bce-process=image/resize,m_lfit,w_440,limit_1/format,f_auto)](https://baike.baidu.com/pic/jdk/1011/0/7af40ad162d9f2d36880ccf1a3ec8a136327cc1f?fr=lemma&ct=single)

jdk结构图

#### JRE——Java运行环境

1.JRE（Java Runtime Environment  Java运行环境）

JRE=JVM+JAVA的核心类库[类]

2.包括JAVA虚拟机和JAVA程序所需的核心类库等，**如果想要运行一个开发好的JAVA程序，计算机中只需要安装JRE即可**

即如果有*非开发人员*想要运行JAVA程序，安装JRE即可，开发人员则需要JRE和JAVA开发工具



#### 环境配置

略

#### 快速入门

```java
//这是java的快速入门，演示
//对代码的相关说明
//public class Hello 表示Hello是一个类，public表示公有的类，stratic静态
//main方法，主方法，程序执行入口
public class Hello{
	//编写一个main方法
	public static void main(String[] args){
		System.out.println("Hello word!");
	}
}
```

`小知识：`.class文件也被称为字节码文件。有了java源文件，通过编译器将其编译成JVM可以识别的字节码文件

`Java文件`（源文件）→`.class文件`（字节码文件）→结果

### JAVA开发的细节问题-chapter01

1.JAVA具有严格的大小写区分，语句结尾必须接分号

2.**一个源文件中最多只能有一个public修饰的类**，其他类的个数不限。（源文件编译后，每一个类，都会对应一个.class文件)

3.**如果源文件包含一个public类，则文件名必须按照该类名命名**

4.**main方法可以写在非public类中，然后指定运行非public类，这样入口方法就是非public的main方法**

##### `1月27日小记`

​		昨天因为意外的熬夜加班所以没能学上，有点失落是真的，最近也被某些东西扰乱了心神，有些烦躁，但是该学的东西还是要学会的，即使这让我并不好受，一步一步，走下去，至少我目前是这么想的，我会坚持下去，一定会。

| 今日完成事宜 | 完成情况       |
| ------------ | -------------- |
| Typora入门   | 完成良好，逐步熟悉   |
| JAVA基础复习 | 复习了部分细节，还有很多要做 |
| VS code上手  |VS code的基础运行无碍，逐步分析    |

| 明日完成目标 | 完成目标                               |
| ------------ | -------------------------------------- |
| JAVA基础复习 | JAVA基础部分快速复习，待进             |
| VS code上手  | VS code逐步熟悉，使用sublime多熟悉代码 |
| 计算机基础   | 基础待进步                             |



#### JAVA常用转义字符

![image-20220307112031761](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220307112031761.png)

dos指令中Tab补全文件名

```java
System.out pringtln("你好啊\r世界");//转义字符\r回车不换行同行输出
//"你好"被"世界"替换,输出结果应为：世界啊 
//热知识：IDLE不支持回车符\r
```

#### JAVA初级易犯错误

1.**找不到文件**：文件名书写错误

2.**类XXX是公共的，应在.....中声明**:主类名和文件名不一致

3.**缺少分号**：略

#### JAVA注释

##### 单行注释

```java
//这是一个单行注释
```

基本格式：//注释文字

##### 多行注释

```java
/*这是一个
多行的
注释*/
/*这是/*一个
错误的
多行*/注释/*

```

基本格式：/*注释文字 */

1.被注释的文字，不会被JVM（java虚拟机）解释执行

2.多行注释里不允许有多行注释嵌套

##### 文档注释（JAVADOC）

```java
/**
 *@author 作者
 *@version 1.0
 *
 */
```

文档注释@有固定的内容

#### JAVA代码规范

1.**类、方法的注释，要以javadoc（即文档注释）的方式来写**

2.非Java Doc的注释，往往是给代码的维护者看的，着重告知读者为什么这样写，如何修改，注意什么问题等

3.**使用tab操作**，Tab实现缩进默认整体向右以动，Shift+Tab整体向左移

4.运算符和 = 两边习惯性各加一个空格，例如：2 + 3 = 5;

5.**源文件要保存为UTF-8;(dos系统演示需要保存为GBK,但工作需要存为UTF-8)**

6.每行不要超过80字符

7.代码编写**次行风格**和**行尾风格**。

#### 相对路径和绝对路径

1.相对路径：`..\`返回上一级，根据当前目录开始定位，形成一个路径

2.绝对路径：从顶级目录开始定位，形成路径

### Java变量的基本原理-chapter03

#### 变量的基本原理：

变量的对应关系：

```java
int a = 1;  //执行时，首先在内存中分配了一个空间，空间里有一个值1，a变量指向了它
int b = 1;
b = 89;		//通过变量b找到对应的空间，将其中的数值换为89

```

#### 变量的概念：

变量相当于内存中一个数据存储空间

#### 变量的注意事项

1.变量表示内存的一个存储区域[**不同的变量，类型不同，占用的空间大小不同**]`比如：int->4个字节  double->8个字节`

2.该区域有自己的名称[**变量名**]和类型[**数据类型**]

3.变量必须**先声明，后使用**，即有顺序

4.该区域的数据可以在同一类型范围内不断变化

5.变量在**同一个作用域内不能重名**

6.变量 = 变量名 + 值 + 数据类型，变量三要素

#### 程序中 + 号的使用

1.当左右两边为数值时，做加法运算

2.当左右两边有一方为字符串，则做拼接运算

```java
//示例
System.out.println(100+98);//198
System.out.println("100"+98);//10098
System.out.println(100+3+"hello");//103hello
System.out.println("hello"+100+3);//hello1003
```

### JAVA数据类型

#### 数据类型分类

每一种数据都定义了明确的数据类型，在内存中分配了不同大小的内存空间（字节）

##### 基本数据类型：

1.数值型：

​	(1).整数类型，存放整数`byte[1] , short[2] , int[4] , long[8]`（[ ] 内容为类型所占字节数）

​	(2).浮点(小数)类型`float[4], double[8]`

2.字符型:

​	字符型`char[2]`，存放单个字符

3.布尔型

​	布尔型`boolean[1]`，存放true，false

##### 引用数据类型:

1.类`class`（注意：**String不属于基本数据类型，属于类**）

2.接口`interface`

3.数组[  ]



#### 整数类型

##### 整形细节：

1.Java中各整数类型有固定的范围和字段长度，不受OS[操作系统]的影响，以保证java的可移植性。

2.Java的**整型常量默认为int型**，声明long型常量须后加'l'或'L'。

```java
int n1 = 1;//4个字节，对
	//int n2 = 1L;  8个字节，从long转换到int可能会有损失，会有编译错误，错
long n3=1; //4个字节，对，int可以给long 
long n4=1L;//对

```

3.Java变量声明常用int型，除非有超出范围的数才会用long型。

4.**`bit`：计算机中最小的存储单位，byte：计算机中基本存储单元。1 byte = 8 bit`**



#### 浮点类型

##### 面试重点：

1.浮点数=符号位+指数位+尾数位。

2.尾数部分可能丢失，造成精度损失（小数都是近似值）

##### 浮点细节：

1.Java中各浮点类型有固定的范围和字段长度，不受OS[操作系统]的影响，以保证java的可移植性。

2.Java的**浮点常量默认为double型**，声明`float`型常量须后加'f'或'F'。

而double型常量后面可加'd'或'D'，也可以不加。

```java
//float n1 = 1.1;错误，不兼容类型，从double转换到float可能会有损失
float n2 = 1.1F; //对
double n3 = 1.1; //对
double n4 = 1.1L;//对，4个字节，对，float可以给double 
 
```

3.浮点型常量有**两种表示形式**：

十进制：如：`5.12  512.0f  .512(小数零可以省略)`

```java
double n5 = .123 //对，等价0.123
```

科学计数法： 如： `5.12e2[5.12*10的2次方]  5.12e-2[5.12除以10的2次方]`

```java
System.out.println(5.12e2);//512.0  double类型整数后面自带.0
System.out.println(5.12e-2);//0.0512
```

4.通常情况下，应使用double，因为它比float型更精确

5.**浮点使用陷阱**： `2.7` 和 `8.1/3` 比较

```java
double n6 = 2.7;
double n7 = 8.1 / 3;
System.out.println(n6);//结果为2.7
System.out.println(n7);//结果为2.6999999999999997，输出为一个近似于2.7的值，而不是2.7
//重要的使用点，当我们对运算结果是小数的时候进行相等判断时要小心，不要对运算后的小数进行比较
//应该是以两个数的差值的绝对值，在某个精度范围判断
System.out.println(Math.abs(n6-n7));
if(Math.abs(n6-n7)<0.000001){
    System.out.println("差值非常小，到我规定的精度，认为相等");
//判断相等，自行确定一个精度
}
```



#### 字符类型

基本介绍

字符类型可以表示单个字符，字符类型为char

演示char的基本使用

```java
char c1 = 'a';
char c2 = '\t';
char c3 = '杨';
char c4 = 97 ;//结果为 a 
```

字符数字对应ASIC码值，当输出c4的时候，会输出97表示的字符。

##### 字符细节：

1.字符常量用单引号（ `' '` )括起来的单个字符，双引号会报错。

2.Java中还允许使用转义字符`' \ '` 

3.在Java中，char的本质是一个整数，在输出时，是Unicode码对应的字符。 

[字符编码转换（ASCII和中文和Unicode）](http://tool.chinaz.com/Tools/Unicode.aspx)

```java
char c1 = 97;
System.out.println(c1); //a
System.out.println((int)c1); //97
char c2='杨';
System.out.println((int)c2);//26472,输出对应数字
```

4.可以直接给char赋一个整数，输出时，是unicode码对应的字符

5.char类型是可以运算的，相当于一个整数，因为它都对应有Unicode码

```java
System.out.println('a' + 10);// 107
System.out.println('a' + 'a');//194
char n1 = 'a';
char n2 = 'b' + 1;
System.out.println(n1 + 'a');//194
System.out.println(n1);//a
System.out.println(n2);//c
System.out.println(n1 + n2);//196
```



##### 字符类型本质讨论：

1.字符型存储到计算机中，需要将字符对应的码值（整数）找出来，比如’a'

​	存储：'a' ==> 码值 97 ==> 二进制==>存储

​	读取： 二进制 => 97 ===>  'a' => 显示

2.字符和码值的对应关系是通过字符编码表决定的（规定好的）

![image-20220308180859968](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220308180859968.png)

**实际上ASCII编码表是用一个字节表示的，而一个字节可以表示256个字符，只是作者只用了128个**

ASCII编码表英文够用，对类似于中国的国家，ASCII编码表不够用，Unicode基于ASCII编码表扩展了。Unicode编码表使用两个字节表示字符，字母和汉字都是占用两个字节，这样浪费空间。

**不同的编码对文件的大小有影响，并且对字符本身也有影响**

UTF-8编码对字符的使用情况较好，因为文档中英文大于汉字，Unicode编码容易浪费过多空间

**GBK可表示的汉字<UTF-8可表示的汉字，这就是为什么UTF-8的文件转GBK会报错**

**Unicode编码**

优点：不会出现乱码的问题，将世界上所有的符号都纳入其中，包括中文，韩文，日文，英文等，Unicode码兼容ASCII码。

缺点：对于存储空间过于浪费。

**UTF-8**

优点：UTF-8是互联网上使用最广的一种Unicode的改进，避免了空间浪费且能表示更多的汉字。



#### 布尔类型

1.布尔类型也叫boolean类型，boolean类型只允许存`ture`或`false。`



```java
boolean isPass = true;
if(isPass == true){
    System.out.println("真");
}else{
    System.out.println("假");
}
```

##### 布尔细节：

1.不可以**用0**或者**非0的整数**替代`false`和`true`，**这点和C语言不同，C语言可以。**



#### 基本数据类型转换

##### 自动类型转换：

当Java程序在进行赋值或运算时，精度小的类型会自动转换为精度大的数据类型，即**自动类型转换**

自动转换路线：

![image-20220308183133779](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220308183133779.png)

 Auto convert（自动 转换）

##### 自动类型转换注意和细节

1.有多种类型的数据混合运算时，系统首先将所有数据转换为容量最大的那种数据类型，然后在进行计算

```java
int n1 = 10;
double d1 = n1 + 1.1;//*float d1 = n1 + 1.1错误*，因为1.1为double类型，整个右边计算出为double类型。
```



2.当把精度达大的数据类型赋给精度小的类型时会报错

```java
//即
int n = 1.1;//错误 double不能转换int
```



3.byte和short不能自动转换为char，char也不能自动转换为byte和short

```java
byte b1 = 10;//对的，当把一个具体的数赋给byte时，先判断是否在范围内，如果是就可以。
int n2 = 1;//n2 是int。
//byte b2 = n2;错误,放不进去，如果是按变量赋值则判断类型。
//char c1 = b1;错误，byte不能自动转成char，同理short，编译层面规定的
```



4.byte , short , char 他们三者可以计算，在计算时**首先转换为int类型**。**即使是同类型计算**也会转换为`int类型`

```java
byte b2 = 1;
byte b3 = 1;

short s1 = 1;
// short s2 = b3 + s1; 错误，b3 + s1 => int类型
//byte b4 = b2 + b3;同样错误，三者只要参与运算，就会转换为int类型，不论是单独还是混合。
```



5.boolean类型不参与自动类型转换

```java
boolean pass = true;
//int num100 = pass;报错，boolean不参与
```



6.自动提升规则：自动转换为最大类型。



##### 强制类型转换：

自动类型转换的逆过程，将容量大的数据类型转换为容量小的数据类型，使用时要加上强制转换符( )，但可能造成精度降低或溢出，需要注意。

force 强迫

```java
int n1 = (int)1.9;
System.out.println("n1="+n1);//结果 n1=1
int n2 = 2000;
byte b1 = (byte)n2;
System.out.println("b1="+b1);//结果 b1=-48
```

强制类型转换细节：

1.从大到小使用强制转换

2.强制类型转换只针对最近的操作数有效，往往会使用小括号提升优先级。

```java
int x = (int)(10*3.5+6*1.5);
```

3.char类型可以保存int的常量值，但不能保存int的变量值，需要强转。

4.byte和short和char类型在进行也能算时，当作int类型处理



##### 基本数据类型和String类型的转换

基本类型转String类型：

语法：将基本类型加上`“ ”`即可

```java
//基本数据类型→String
int n1 = 100;
float f1 = 1.1F;
boolean b1 = true;
String s1 = n1 + "";
String s2 = f1 + "";
String s3 = b1 + "";
System.out.println(s1);
System.out.println(s2);
System.out.println(s3);
```

 String类型转换为基本数据类型：

语法：通过**基本类型的包装类**雕用`parseXX`方法即可

```java
String s5 = "123";
//使用基本类型对应的包装类的相应方法，得到基本数据类型。
int num1 = Integer.parseInt(s5);//会在讲OOP讲对和方法的时候详细说
double num2 = Double.parseDoublt(s5);
long num3 = Long.parseLong(s5);
float num4 = Float.parseFloat(s5);
byte num5 = Byte.parseByte(s5);
boolean num6 = Boolean.parseBoolean(s5);
Short num7 = Short.parseShort(s5);
//字符串转换为字符，通常是指把字符串的第一个字符提到字符里
System.out.println(s5.charAt(0));//得到第一个字符 1 
```

##### 注意事项

1.在将String类型转换为基本数据类型时，要确保String类型能够转成有效的数据，比如可以把`"123"`转成一个整数，但不能把`"hello"`转成一个整数。

2.如果格式不正确，就会抛出异常，程序就会终止，<异常处理机制>

```java
String str = "hello";
int n1 = Integer.parseInt(str);
System.out.println(n1);
```

![image-20220308192746228](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220308192746228.png)

**注意：编译的时候不会报错，运行的时候会报错**，运行程序会终止

 

### 运算符-chapter04



# **`以下内容因时间有限，将只记录重点以及一些难点，在此分割`**

------

#### 算术运算符

![image-20220308201410097](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220308201410097.png)

Arithmetic(算数)Operator(运算符)

##### 除法运算符

两个整数类型相除，会得到一个整数。运算时会转换为高精度。

```java
//除法
System.out.println(10 / 4);//从数学来看2.5，在java中2
double d = 10 / 4;
System.out.println(d);//2.0
```



##### 取模运算符

在 % 的本质，!!!!公式：**a % b = a - (int)a / b * b;**

注意有**强转**，故**小数**也可以！！！而**C语言里取模运算符两边只能为int类型**

```java
//在 % 的本质，!!!!公式：a % b = a - （int)a / b * b;
System.out.println(10 % 3);//1
System.out.println(-10 % 3);//-1
System.out.println(10 % -3);//1
System.out.println(10.5 % 3);//Java里支持小数取模。故答案为1.5
```



##### 自增自减

###### 面试题

```java
int i = 10;
//独立使用时前++后++完全等价于i=i+1
++i;//11
i++;//12
int b;
//表达式使用
//前++：++i先自增，后赋值
//后++：i++先赋值，后自增
b=i++;//b=12 等价 b=i;i=i+1;
b=++i;//b=14 等价 i=i+1;b=i;

//!!!面试题：
int i = 1;
i = i++;//规则使用临时变量：(1)temp = i; (2)i = i+1 (3)i = temp;
System.out.println(i) //最后结果为1
```

#### 关系运算符

![image-20220308204828312](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220308204828312.png)

**两个`==`表判断，一个`=`表赋值**。

`instanceof`会在面向对象中讲解

Relationa(关系)Operator(运算符)

`实际开发中不要使用a,b,a1,b之类的变量名`

##### 关系运算符细节

1.关系运算符的结果都是boolean类型。

2.关系运算符组成的表达式，称为关系表达式。

3.注意等号的使用

#### 逻辑运算符

![image-20220308205424932](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220308205424932.png)

`a^b`：当a和b不同时，则返回结果为true，否则为false。

##### `&&`和`&`的区别

短路与`&&`

逻辑与`&`

```java
int age = 50;
if(age > 20 && age <90){
    System.out.println("真");
}
//结果：真
if (age > 20 & age < 90) {
	System.out.println("真");
}
//结果：真

int a = 5;
int b = 9;
if(a < 1 && ++b >5){
    System.out.println("真"); 
}
System.out.println("a=" + a + "b=" + b);//a=5b=9
//因为a<1为假，故&&后面不再判断，++b不执行
if (a < 1 && ++b > 5) {
    System.out.println("真");
}
System.out.println("a=" + a + "b=" + b);//a=5b=10
//即使a<1为假，&后面也会再判断，++b执行

```



`&&`:如果第一个条件为true，则第二个条件不会判断

`&`:两个条件都会判断，效率较低。

`&`的效率较低，故平时基本上使用的是`&&`

##### `||`和`|`的区别

短路或`||`

逻辑或`|`

与`&&`和&的区别同理

`||`:如果第一个条件为true，则第二个条件不会判断

`|`:两个条件都会判断，效率较低。



#### 赋值运算符

Assign(分配)Operator(运算符)

```java
int n1 = 10;
n1 += 4; //n1 = n1 + 4;
System.out.println(n1);//14
n1 /= 3; //n1 = n1 / 3;
System.out.println(n1);// 3
```

##### 赋值运算符细节

**1.赋值运算符的左边只能是变量，右边可以是变量、表达式、常量值。**

**2.复合运算符会进行类型的转换**

```java
byte b = 3;//复合运算符会进行强制类型转换
b += 2; //等价于b =(byte)(b + 2);
b++;//等价于b = (byte)(b + 1);
```

#### 三元运算符

条件表达式 ? 表达式1 : 表达式2;

1.如果条件表达式为true，运算后的结果是表达式1；

2.如果条件表达式为false，运算后的结果是表达式2；

```java
int a = 10;
int b = 99;
int result = a > b ? a++ : b--; //result = 99;b = 98
```

##### 三元运算符细节

1.表达式1和表达式2要为可以赋给接受变量的类型(可以自动转换)。

```java
int a = 3;
int b = 8;
int c = a > b ? a : b ;//对
//int c = a > b ? 1.1 : 3.4;错误，会报错，同自动转换规律
```

2.三元运算符可以转成if-else语句。



#### 运算符的优先级

![image-20220309150541001](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220309150541001.png)



### 标识符的命名规则和规范

#### 标识符的命名规则[必须遵守]

1.由26个英文字母大小写，`0~9`，`_`或`$`组成

2.**数字不可以开头**，`int 3ab = 1` 错误

3.**不可以**使用**关键字**和**保留字**，但能包含关键字和保留字。

```java
int abcclass = 10; // 对，如果为int class = 10;会严重报错
```

4.**Java中严格区分大小写即a和A为两个不同的变量**，长度无限制。但一般不会太长

5.标识符不能包含空格，`int a b = 300;`错误。



#### 标识符的规范[更加专业]

1.**包名**：多单词组成时所有**字母都小写**：`aaa.bbb.ccc` //比如 `com.yjk.crm`

2.类名、接口名：多单词组成时，所有单词的首字母大写：`XxxYyyZzz`[大驼峰]

3.变量名、方法名米：多单词组成时，第一个单词首字母小写，第二个单词开始每个单词首字母大写：`xxxYyyZzz`

4.常量名：所有字母都大写。多单词时每个单词都用下划线连接：XXX_YYY_ZZZ

5.**具体规范看文档。**

#### 关键字

定义：被Java语言赋予了特殊含义，用做专门用途的字符串。

**特点：关键字所有字母都是小写。**

#### 保留字

现有版本尚未使用，但以后可能会作为关键字使用，命名时要避免。



### 键盘输入语句

#### 扫描器（Scanner类）

步骤：

1.导入该类所在包，java.util.*

2.创建该类的对象

3.调用方法。

```java
//导入包
import java.util.Scanner;
public class Input{
    public static void main(String[] args){
        //Scanner类表示简单文本扫描器，在java.util包
        //1.引入 Scanner类所在包
        //2.创建 Scanner 对象，new 创建一个。
        //3.雕用 Scanner类的方法
        Scanner myScanner = new Scanner(System.in);
        System.out.println("请输入姓名："); 
        String name = myScanner.next();
        System.out.println("请输入年龄：");
        int age = myScanner.nextInt();
       	System.out.println("姓名："+name+"年龄："+age);
    }
}
```



### *进制

1.二进制：0,1，满2进1，以**`0b`**或者`0B`开头。

2.十进制：0~9，满10进1。

3.八进制：0~7，满8进1，以数字**`0`**开头表示。

4.十六进制：0~9及A(10)~F(15)，满16进1，以**`0x`**或**`0X`**开头表示，此处的**A~F不区分大小写**。

```java
//演示四种进制
int n1 = 0b1010;
int n2 = 1010;
int n3 = 01010;
int n4 = 0x10101;
System.out.println("n1="+n1);//10
System.out.println("n2="+n2);//1010
System.out.println("n3="n3);//520
System.out.println("n4="n4);//65793
```



#### 进制的转换（基本功）

##### 其他进制转十进制

1.二进制转十进制

从最低位（右边）开始，将每个位上的数据提取出来，**乘以2的（位次-1）次方**，然后求和.

2.八进制转十进制

从最低位（右边）开始，将每个位上的数据提取出来，**乘以8的（位次-1）次方**，然后求和.

3.十六进制转十进制

从最低位（右边）开始，将每个位上的数据提取出来，**乘以16的（位次-1）次方**，然后求和.



##### 十进制怎么转其进制

1.十进制转二进制

规则：**将这个数不断除以2**，直到**商为0为止**，然后将**每步得到的余数倒过来**，就是对应的二进制

案例：将34转成二进制

34→0B00100010  //转进制之后因为一个字节有8位，故前面应当补两个0

```
34 / 2 = 17 //余0
17 / 2 = 8  //余1
8 / 2 = 4 //余0
4 / 2 = 2 //余0
2 / 2 = 1 //余0
1 / 2 = 0 //余1
0 1 0 0 0 1 依次入栈，先进后出，后进先出
即出栈为 1 0 0 0 1 0 
故34→0B100010
```

2.十进制转八进制

规则：**将这个数不断除以8**，直到**商为0为止**，然后将**每步得到的余数倒过来**，就是对应的二进制

与转二进制同理

3.十进制转十六进制

规则：**将这个数不断除以16**，直到**商为0为止**，然后将**每步得到的余数倒过来**，就是对应的二进制

与转二进制同理



##### 二进制转八进制、十六进制

1.二进制转八进制

规则：从**低位开始**，将二进制的**每三位以组**，**转成对应的八进制数**即可

案例：请将0b11010101 转为八进制

```
0b11|010|101 //0b11010101拆分
101→5
010→2
11→3
即0325
```



2.二进制转十六进制

规则：从低位开始，将**二进制的每四位以组**，**转成对应的十六进制数**即可

案例：请将0b11010101 转为十六进制

```
0b|1101|0101 //0b11010101拆分
0101→5
1101→13(十进制)→D
即0xD5
```



##### 八进制、十六进制转成二进制

1.八进制转二进制

规则：将八进制**每一位数**，转成对应的**一个三位二进制数**即可

案例：0237转成二进制

```
0237
7→111
3→011
2→010
ob10011111 //注意八位
```

2.十六进制转二进制

规则：将十六进制**每一位数**，转成对应的**一个四位二进制数**即可

案例：0x23B转成二进制

```
0x23B
B→1011
3→0011
2→0010
即0b001000111011
```

#### 位运算

1.二进制是逢2进位的进位制，0，1是基本运算符

2.计算机内部处理的信息，都采用二进制来表示

```java
int a = 1>>2;//向右位移两位
int b = -1>>2;//向右位移两位
int c = 1<<2;//向左位移两位
int d = -1<<2;//向左位移两位
System.out.println("a="+a);
System.out.println("b="+b);
System.out.println("c="+c);
System.out.println("d="+d);
```



##### 原码补码反码（重点，难点）

**1.二进制的最高位是符号位：0表示正数，1表示负数（口诀：0->0 1->-)**



**2.正数的原码，反码，补码都一样（三码合一）**
$$
正数的原码=反码=补码
$$
**3.负数的反码 = 它的原码符号位不变，其他位取反（0->1,1->0）**
$$
负数的反码 = 它的原码符号位不变，其他位取反（0->1,1->0）
$$
**4.负数的补码 = 它的反码 + 1，负数的反码 = 负数的补码 - 1**
$$
负数的补码 = 它的反码 + 1，负数的反码 = 负数的补码 - 1
$$
**5.0的反码，补码都是0**
$$
0的反码=0，补码都是0=0
$$
6.java没有无符号数，换言之，**java中的数都是有符号的**

7.计算机在按位运算的时候，都是**以补码的方式**来运算的（注：因为补码可以解决正数和负数的计算问题）

**8.当我们看运算结果的时候，要看它的原码（！！）**



#### 位运算符

java中7个位运算(&、|、^、~、>>、<<和>>>)

##### 按位

按位`&`运算：**两位全为1，结果为1**，否则为0

```
1 0 0 1 0 0 1 1 
1 1 1 0 0 1 0 1 &
————————————————
1 0 0 0 0 0 0 1
```

按位或`|`运算：**两位有一位为1，结果为1**，否则为0

按位异或`^`运算：**两位有一位为1，一个为0，结果为1**，否则为0

按位取反`~`：0→1，1→0

```java

System.out.println(2 & 3);//2
System.out.println(~-2);//1
//1.先得到-2的原码 10000000 00000000 00000000 00000010
//2.-2的反码 11111111 11111111 11111111 11111101
//3.-2的补码 = -2的反码 + 1; 故补码：11111111 11111111 11111111 11111110
//4.-2的补码的取反： 00000000 00000000 00000000 00000001
//5.取反后的原码：00000000 00000000 00000000 00000001
//6.结果1
System.out.println(~2);//-3
//1.因为2是正数所以补码等于原码 00000000 00000000 00000000 00000010
//2.按位取反，运算后的补码： 11111111 11111111 11111111 11111101
//3.运算后的原码，先算运算后的反码 = 运算后的补码 -1即反码：11111111 11111111 11111111 11111100
//4.反码除符号位按位取反：10000000 00000000 00000000 00000011
//5.得到结果-3
```



##### 位移位

1.算数右移`>>`:低位溢出，符号位不变，并用符号位补溢出的高位

2.算数左移`<<`：符号位不变，低位补0。

3.`>>>`逻辑右移也叫无符号右移，运算规则是：低位溢出，高位补0

4.**特别说明：没有`<<<`符号**

``` java
int a = 1 >> 2; //本质上等于 1 / 2 / 2 = 0;
int b = 1 << 2; //本质上等于 1 * 2 * 2 = 4;
```



#### <center>位运算掌握以上即可</center>

------





### 控制结构 

在程序中，程序运行的流程控制决定程序是如何运行的

#### 顺序控制

程序从上到下逐行地执行，中间没有任何判断和跳转

Java中定义成员变量时采用合法的向前引用：

```java
public class Test{
    int num1 = 12;
    int num2 = num1 + 2;
    //先定义后使用
}
```



#### 分支控制（if,else,else if）

##### 1.单分支

```java
if(条件表达式){
    执行代码块;
}
```

如果{}中只有一条语句，{}可以不写。



流程图：

![image-20220309194751090](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220309194751090.png)

##### 2.双分支

```java
if(条件表达式){
    执行代码块1;
}
else {
    执行代码块2;
}
```

 流程图：

 ![image-20220309195110129](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220309195110129.png)

##### 3.多分支

```java
if(条件表达式1){
    执行代码块1;
}
else if(条件表达式2){
    执行代码块2;
}
……
else{
    执行代码块n;
}
```

流程图

![image-20220309200219115](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220309200219115.png)

特别说明：

1.**多分支可以没有else，如果所有条件表达式都不成立，则一个执行入口都没有**

2.如果有else，则如果所有条件表达式都不成立，执行else执行代码块。

##### 4.嵌套分支

规范：**嵌套不要超过三层**

```java
if(){
   if(){
       ;
   }
    else {
        ;
    } 
}

```

**score(成绩) **

**gender(性别)**

##### 接收字符



```java
Scanner scanner = new Scanner(System.in);
char gender = scanner.next().charAt(0);//获取字符串的第一个字符
```

##### switch分支结构

```java
switch(表达式){
    case 常量1:
        语句块1;
        break;
    case 常量2:
        语句块1;
        break;
        ……
    case 常量n:
        语句块n;
        break;
    default: 
        default语句块;
        break;
}
```

1.表达式对应一个值。

2.break：表示退出switch。

3.如果和case常量1匹配，就执行语句块1，如果没有匹配，就继续匹配case常量2

4.如果一个都没匹配上，执行default。

流程图

![image-20220309203018036](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220309203018036.png)

###### switch分支结构细节：

1.表达式类型，应和case 后的常量**类型一致**，或者是可以自动转换可以相互比较的

```java
char c = 'a';
switch(c){
    case 'a':
        System.out.println("1");
    case 'b'://如果写成"hello"会报错
        System.out.println("1");
    case 20: //对，可以比较
        System.out.println("1");
    case 'd':
        System.out.println("1");
        
}
```

2.switch(表达式)中表达式返回值必须是：`（byte , shart , int , char , enum[] , String)`，即**不能为float、double**等，会报错。

3.**case字句中的值只能为常量或常量表达式**不能为变量。即case后值不能为变量。

```java
char c = 'a';
switch(c){
    case 'a':
        System.out.println("1");
    case 'b'+1://对，可以为常量表达式
        System.out.println("1");
    case 20: //对，可以为数字
        System.out.println("1");
}
     
```

4.default字句是可选的，当没有匹配的时候，执行default，如果没有匹配也没有default，则没有输出。

5.break语句用来执行完一个case分支后跳出switch语句。如果没有break语句，直接进行下一条语句（穿透），直到遇到break语句或者直到switch语句结束。

> 表达式：只要有值返回就是表达式



##### switch语句和if语句区别

1.如果判断的具体数值不多，而且符合（byte , shart , int , char , enum[] , String)这几种类型，虽然两个语句都可以使用，但建议switch

2.其他情况：对于区间判断，使用if



#### 循环控制

##### for循环控制

```java
for(循环变量初始化;循环条件;循环变量迭代){
    循环操作(可以多条语句);
}
```

同样，如果循环操作只有一条语句，可以省略{}，但建议不要省略。

for循环流程分析

流程图

![image-20220316192151855](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220316192151855.png)

##### for循环细节

1.循环条件是返回布尔值的表达式。

2.初始化和变量迭代可以写在其他地方，但是不能省略分号。

3.循环初始值可以有多条初始化语句，但要求类型一致，并且中间用逗号隔开，循环变量迭代也可以用多条变量迭代语句，中间用逗号隔开。

##### while循环

流程图

![image-20220329193103727](C:\Users\28262\AppData\Roaming\Typora\typora-user-images\image-20220329193103727.png)

##### do while循环

```java
do{
    //循环体语句
    //循环变量迭代
}while(循环条件);
```

1.do while 是关键字

2.循环四要素位置不一样

3.**先执行，再判断，也就是至少执行一次**

4.结尾有分号



#### 多重循环控制



1.将一个循环放在另一个循环体内，就形成了嵌套循环，其中，for、while、do while 循环都可以做内循环或外循环。**（建议一般使用两层，最多不要超过三层循环）**

2.实质上，嵌套循环就是把内层循环当作外层循环的循环体。当只有内层循环的循环条件为false时，才会完全跳出内层循环，才可结束外层的当次循环，才可以进行下一次的循环

3.设外层循环次数为m次，内层为n次，则内层循环体实际上需要执行m*n次

# 本篇笔记篇幅过长，导致Typora打字会出现卡顿的状态，故此分割，下接Java学习2



#### break

#### continue

#### return

### 如何使用API

#### JAVA API 文档

1.API（应用程序编程接口）是 Java 提供的基本编程接口（ Java提供的类还有相关的方法）。

​	中文在线文档：[Java API 文档](https://www.matools.com)

2.Java 语言提供了大量的基础类，因此 Oracle公司也为这些基础类提供了相应的API文档

```java

```

3.Java类的组织形式（图）

4.举例说明如何使用，例如 ArrayList类有哪些方法：

安：包→类→方法

直接索引



##### 