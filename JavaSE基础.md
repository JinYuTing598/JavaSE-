# **01：Java基础引言**

1.程序是为了模拟现实世界解决现实问题，使用计算机语言编写一系列有序的指令集合

2.java属于设计语言

3.分为 javase、javaee、javame

## **java的历史和特点**

##### 一、历史	

1. javase ： 平台标准版

2. javaee ：平台企业版，企业级开发

   c/s :结构的应用程序（客户端应用程序，需要下载安装本地应用软件）

   b/s :(通过网页输入域名+....)

3. javame：平台微缩版

##### 二、特点

1. 面向对象

2. 跨平台性

3. 简单性

   java虚拟机内置的gc垃圾回收，自动完成空间清理

4. 开源

## **计算机的运行机制**

1.  编译执行：在具体的环境中（windows）执行一次翻译（源文件-->机器码语言），执行机器码文件。

   #### **特点：执行效率高，不跨平台**

   ![image-20230131141006523](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230131141006523.png)

2.  解释执行：将源文件代码一行一行的解释并且执行，不同的运行环境有不同的解释器。

   特点：执行效率低，可以跨平台。

   ![image-20230131141031039](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230131141031039.png)

3.  java语言执行机制：先编译，再解释。

   将java源文件先编译成平台中立的字节码（.class）文件，再执行跨平台的逐行解释执行，，将计算机的两种执行机制合二为一。运行在JVM上

   #### **特点：执行效率高，可以跨平台。**

   ![image-20230131141046571](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230131141046571.png)

## **名次解析**

1. JVM：虚拟机
2. JRE：运行环境
3. JDK：java环境

#### 包含关系：JDK>JRE>JVM

![image-20230131104528419](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230131104528419.png)+



## **DOC命令操作**

![image-20230131143155004](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230131143155004.png)



## **编写第一个代码**

![image-20230131135912350](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230131135912350.png)

#### 注意：每行代码要使用“ ; ”进行结尾！！！

1.  class 类
2.   public 公共公开的
3.   static 静态的
4.   void 无返回值
5.   main 主要的
6.   String 字符串
7.   out输出
8.   print 打印



## **DOS命令编码过程**

1. 先使用javac  源文件名（类名）.java  进行编译
2. java 类名 + 回车

注意：当修改密码以后必须在记事本中进行保存，不保存的话，运行的是原来的，我们在运行的时候都是运行的字节码文件



## **类的阐述**

1. 同一个源文件中可以定义多个类
2. 编译后，每个类都会产生独立的class文件
3. 一个类只能有一个主方法（也就是只有一个入口），每个类都可以有自己的主方法
4. public修饰的类，源文件名和类名必须完全相同
5. 一个源文件只能有一个公开类

![image-20230131151129024](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230131151129024.png)



## **包的规范**

1. 为什么用包？当两个源文件名不同的时候，内部的类名相同，就会产生覆盖，最后编译的文件会显示出来，为了避免这种情况，将两个源文件放在不同的包下边就不会出现这种状况

![](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230131152255325.png)



2. 作用：类似于文件夹，用于管理字节码(.class)文件。
   语法：package包名；
   位置：必须写在源文件的第一行。
   带包编译：javac -d . 源文件名称.java(自动生成目录结构)
   带包运行：java 包名.类名（包名+类名又称全限定名）
   采用域名倒置的规则：www.baidu.com.cn->cn.com.baidu.XXx
   例如：cn.com.company.department..group.project.module..XxxClass



## **编写规范1**

1. 层级之间必须缩进使用Teb (制表符)
2. 一句代码写在一行



## **编写规范(注释)**

1. 单行注释：// 哈哈哈
2. 多行注释：/* 嘻嘻嘻  */
3. 文档注释：/**  呵呵呵  */  生成外部文档：javadoc-d.HelloWorld,java

#### 注意：注释不会参任何代码编译





# 2：**Java语言基础**

## 2.1：变量

1. 概念：计算机内的一块存储空间，是存储数据的最大单元(就相当于用水杯来装水)
2. 组成：数据类型  变量名  =  值        例如：int a = 20;   也就是将右边的值赋给左边的变量
3. 等号（=）：把等号左边的东西赋值给右边的东西

## 2.2：变量的定义流程

声明：数据类型 变量名；  例如：int money；

赋值：变量名 = 值；   例如：money = 100；

![image-20230201094807872](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201094807872.png)



### 注意：Java是强类型语言，变量类型必须和数据类型相同。

## 2.3：变量的定义方式

声明变量的三种方式：

1. 先声明再赋值  

   数据类型 变量名；

   变量名 = 值；

2. 声明时候直接赋值：

   数据类型 变量名 = 值；

3. 多个类型的变量同时赋值

   int a = 110,b,c;

   c = 200;

   此时能输出的是a = 110，c = 200，输出b会报错，因为只是声明了但是没有赋值

```java
public class TestVariable2{
public static void main(String [args){
//变量的三种定义方式
//第一种：先声明再赋值
//数据类型变量名；
int
money;
//变量名=值；
money=1003
//使用
System.out.println(money);
//第二种：边声明边赋值
//数据类型
变量名=值；
int age=18;
//使用
/print打印In line println打印后换行
System.out.println(age);
//第三种：多个同类型变量声明并赋值（了解）
//定义3个整数类型abc并为c赋值为5
int a,b,cj
a=53
b=5;
c=5;
System.out.println(a);
System.out.println(b);
System.out.println(c);
```

## 2.4：数据类型

基本数据类型：4类8种

数值类型：

> 整形：byte  short  int  long

> 浮点型：float  double 



非数值类型：

> 布尔型：boolean

> 字符型：char

引用数据类型：

> 字符串  数组  对象  枚举 等等



## 2.5：基本数据类型（整数）

![image-20230201110610753](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201110610753.png)

```java
public class Demo2 {
    /**
     基本数据类型（整数）
     */
        public static void main(String[]args) {
//数据类型变量名=值;
            byte b = 127;//-128 ~ 127(共计256个整数)
            System.out.println(b);
            short s = 32767;//-32768 ~ 32767 (共计65536个整数)
                    System.out.println(s);
            int i  = 2147483647;//-2147483648 ~ 2147483647(共计42亿多个整数)
            System.out.println(i);
//Java中所有的“整数字面值"的默认类型是int,当整数字面值超过int的取值范围时，则提醒"过大的整数"
            long l1 = 2147483648L;//显示告知JVM,此值为1ong类型
            long l2 = 922337283685477587L;//-9223372036854775808L ~ 9223372036854775807L
            System.out.println(l1);
            System.out.println(l2);
        }
}

```



## 2.6：基本数据类型（小数）

![image-20230201115639288](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201115639288.png)



##### 注意：小数的默认值类型是double

##### **注意：**double**为浮点数的默认类型，如需为**float类型赋值时，需要在值的后⾯追加“F”



> **面试题：float f = 1; 能不能编译通过？**
>
> ```java
> //默认是int类型，float取值范围包含int类型，float能把这个数包范围在里边，不能被数迷惑，看数的类型，一个整数的类型默认是int！！！！
> 		float f = 1;
> 		System.out.println(f);
> 
> //编译不能通过，因为1.0默认是double类型，float的取值范围没法覆盖double所以不兼容会报错
> //值后边加上f就可以通过了
>         float f1 = 1.0f;
>         System.out.println(f1);
> 
>         //double不适合精准运算，因为涉及到二进制转十进制，会有精度丢失现象
>         double d6 = (1.4-0.5)/0.9;
>         System.out.println(d6);//输出0.9999999999999999
> ```





## 2.7：基本数据类型（布尔类型）

非真既假！ 只有两个结果true或者flase，多用于判断

绝对不能参与运算

![image-20230201144841542](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201144841542.png)

> ```java
> public class TestType3{
>  public static void main(String[] args){
>  boolean b1 = false; 
>  System.out.println(b1);//false
>  boolean b2 = 5 > 4;
>  System.out.println(b2);//true
>  	}
> }
> ```
>
> 

## 2.8：基本数据类型（字符-1）

ASCII(美国信息交换标准码)：48代表0    65代表A    97代表a

![image-20230201142748827](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201142748827.png)

万国码表：

![image-20230201142819165](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201142819165.png)

##### 三种字符类型赋值的方式

![image-20230201144914989](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201144914989.png)

>```java
>使用三种方式输出字符A
>public class Demo5_Char {
>    public static void main(String[] args) {
>        //字符类型的3种赋值方式,都输出A
>        //第一种：字符赋值
>        char c1 = 'A';
>        System.out.println("c1是："+c1);
>        //第二种：整数赋值
>        char c2 = 65;
>        System.out.println("c2是："+c2);
>        //第三种：进制赋值
>        char c3 = '\u0041';
>        System.out.println("c3是："+c3);
>    }
>
>```

##### 转义符

1.   \  将本身具有特殊含义的字符转为普通字符

2.   \  将普通的字符转为有特殊含义的字符

3.  注意：想写输出2个斜杠那就写4个然后输出2个，以此类推。

   ![image-20230201144326866](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201144326866.png)

> ```java
> public class TestSign{
>  public static void main(String[] args){
>  char c1 = '\'';
>  System.out.println(c1);
>  System.out.println("\"");
>  System.out.println("Hello\tWorld");
>  System.out.println("Hello\nWorld");
>  System.out.println("\\");
>  System.out.println("u0041");
>  System.out.println("\u0041");
>  }
> }
> ```
>
> 



## 2.9：引用数据类型（字符串String）



>```java
>public class TestString{
> public static void main(String[] args){
> String str1 = "HelloWorld";
> System.out.println(str1);
> System.out.println("HelloWorld");
> String str2 = "Hello Everyone";
> System.out.println(str2);
> String str3 = "小金小金";
> System.out.println(str3);
> }
>}
>```
>
>

## 2.10：思考题

![image-20230201152047921](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201152047921.png)

## 2.11：类型转换

- ⾃动类型转换
  - 两种类型相互兼容
  - ⽬标类型⼤于原类型

```java
        //整数 - 整数
        short s = 123;
        int i = s;//将源类型值存⼊到⽬标类型变量中（⾃动类型转换）
        System.out.println(i);
        byte b = 100;
        short s2 = b;//⾃动类型转换
        System.out.println(s2);
        //⼩数 - ⼩数
        float f = 100.0F;
        double d = f;//⾃动类型转换
        System.out.println(d);
        //⼩数 - 整数
        int i2 = 100;
        double d2 = i2;//⾃动类型转换
        System.out.println(d2);
```

- 强制类型转换

  - 目标类型小于原类型
  - 比如int要转成byte，那就   int i = 66;       byte b = (byte) i

  ```java
      /*
  		   类型转换（基本数据类型）
  		   强制转换
  		   1两种类型不兼容
  		   2目标类型小于源类型
  		   byte<--short<--int<--long<--float<--double
  		   char<--int
  
  		*/
          short s9=123;
          byte b9=(byte)s9;
          System.out.println(b);
  
          int i9=65;
          char c9=(char)i9;
          System.out.println(c9);
  
          short g = 65;
          char h = (char) g; //因为short 和 char 范围不全为交集，因此不可以直接赋值
          System.out.println(h);
  
          System.out.println("=======================================");
          //面试题
          //转int 损失精度了 小数点没有了
          double dd = 3.14;
          i = (int) dd;
          System.out.println(i);
  
  
          System.out.println("==============扩展内容============");
          //扩展内容 不强制掌握
          short s8=257;
          byte b8=(byte)s8;
          System.out.println(b8);//1
  		/*
  		   进制：二、八、十、十六
  		   二进制：0 1
  		   八进制：0 1 2 3 4 5 6 7
  		   十进制：0 1 2 3 4 5 6 7 8 9
  		   十六进制：0 1 2 3 4 5 6 7 8 9 a b c d e f
  
  		   十进制转二进制
  		   十进制：0 1 2 3 4 5 6 7 8 9
  		   二进制：0 1
  		   十进制转二进制
  		   1024 512 256 128 64 32 16 8 4 2 1  666-512=154-128=26-16=10-8=2
  		         1   0   1   0  0  1 1 0 1 0
  		    二进制转十进制
  			512+128+16+8+2=666
  
  			short 2字节 每字节8位
  			0000 0000 0000 0000
  		257	1024 512 256 128 64 32 16 8 4 2 1
  		              1   0  0  0  0  0 0 0 1
  	        byte  1字节
  			0000 0000
  			0000 0001
  			第一位是符号位 0代表正数  1代表负数
  			    如果第一位是0 直接二转十进制  1
  		*/
  
          short ss=128;
          byte bb=(byte)ss;
          System.out.println(bb);
  
  		/*
  		  short 2字节
  		  0000 0000 0000 0000
  	128  1024 512 256 128 64 32 16 8 4 2 1
  		               1   0  0  0 0 0 0 0
  	       byte 1字节
  		   0000 0000
  		   1000 0000
  		   第一位是符号位 0代表正数  1代表负数
  		       如果第一位是1 证明是负数 二转十 不要符号位 十进制的0
  			   0-128=-128，为什么用0减，是因为除了第一位的128以外后边的数相加，然后减去128
  		*/
          short s4=723;
          byte b4=(byte)s4;
          System.out.println(b4);
  
          short j = 127;
          byte v = (byte) j;
          System.out.println(v);
  ```

  

## 2.12：算数运算符

![image-20230201191713960](C:\Users\金宇廷的星空\AppData\Roaming\Typora\typora-user-images\image-20230201191713960.png)

##### 注意：当一个取余数小于被取余数的时候，结果是取余数本身。比如3%9 结果是3！！！

```java
public class Demo8_SuanShuYunSuanFu {
    public static void main(String[] args) {
        //算术运算符 + - * / %
        int i=5;
        int j=10;
        System.out.println(i+j);//15
        System.out.println(j-i);//5
        
     
        int a = 10;
        int b = 3;
        System.out.println( a / b );//求商 = 3
        System.out.println( a % b );//求余 = 1
        
        
        double d = 10.0;
        int c = 3;
        System.out.println(d / c);//求商 3.33.......
        
        
        int num1 = 10;
        num1++;//⾃增1
        System.out.println(num1);//11
        
        
        int num2 = 10;
        num2--;//⾃减1
        System.out.println(num2);//9
        
        
        int num3 = 5;
        //前++ ：先++，再打印⾃增后的值
        //后++ ： 先打印当前值，再++
        System.out.println( ++num3 );//6
        System.out.println( num3 );//6
        
        
        int num4 = 100;
        //前++ ：先++，再赋值
        //后++ ： 先赋值，再++
        int num5 = num4++;
        System.out.println(num5);//100
        System.out.println(num4);//101
    }
}
```

