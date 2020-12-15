#### 1、能够计算二进制和十进制数之间的互转

​	**十进制数据转成二进制数据：**使用除以2获取余数的方式

​	**二进制数据转成十进制数据：**使用8421编码的方式  

小贴士： 

位（bit）：一个数字0或者一个数字1，代表一位。
字节（Byte）：每逢8位是一个字节，这是数据存储的最小单位。

#### 2、能够使用常见的DOS命令 

命令提示符（cmd）

启动：		Win+R，输入cmd回车
切换盘符	盘符名称:
进入文件夹	cd 文件夹名称
进入多级文件夹	cd 文件夹1\文件夹2\文件夹3
返回上一级	cd ..
直接回根路径	cd \
查看当前内容	dir
清屏		cls
退出		exit

#### 3、理解Java语言的跨平台实现原理 

任何软件的运行，都必须要运行在操作系统之上，而我们用Java编写的软件可以运行在任何的操作系 

统上，这个特性称为**Java****语言的跨平台特性**。该特性是由JVM实现的，我们编写的程序运行在JVM上，而JVM 

运行在操作系统上。 

#### 4、理解JDK和JRE的组成和作用 

**JRE** (Java Runtime Environment) ：是Java程序的运行时环境，包含 JVM 和运行时所需要的 核心类库 。 

**JDK** (Java Development Kit)：是Java程序开发工具包，包含 JRE 和开发人员使用的工具。 

我们想要运行一个已有的Java程序，那么只需安装 JRE 即可。 

我们想要开发一个全新的Java程序，那么必须安装 JDK 。

三者关系： JDK > JRE > JVM 

 #### 5、能够配置环境变量JAVA_HOME 

为了开发方便，我们想**在任意的目录下都可以使用****JDK****的开发工具**，则必须要配置环境变量，配置环境变量的意义 

在于告诉操作系统，我们使用的JDK开发工具在哪个目录下。 

 点击 新建 ，创建新的环境变量 

 变量名输入 JAVA_HOME ，变量值输入JDK9的安装目录 c:\Java9\jdk-9.0.1

 选中 Path 环境变量， 双击 或者 点击编辑 

在变量值的最前面，键入 %JAVA_HOME%\bin; 分号必须要写，必须是英文格式。 

环境变量配置完成，重新开启DOS命令行，在任意目录下输入 javac 命令，运行成功。

#### 6、能够编写HelloWorld程序编译并执行 

Java程序开发三步骤：**编写**、**编译**、**运行**。 

在DOS命令行中，**进入****Java源文件的目录**，使用 javac 命令进行编译。

​	javac Java源文件名.后缀名

在DOS命令行中，**进入****Java源文件的目录**，使用 java 命令进行运行。

​	java 类名字  

#### 7、理解关键字的含义 

**关键字**：是指在程序中，Java已经定义好的单词，具有特殊含义。

 public 、 class 、 static 、 void 等，这些单词已经被 Java定义好，全部都是小写字母

#### 8、理解标识符的含义 

**标识符**：是指在程序中，我们自己定义内容。比如类的名字、方法的名字和变量的名字等等，都是标识符。

**命名规则：** **硬性要求** 

标识符可以包含 英文字母26个(区分大小写) 、 0-9数字 、 $（美元符号） 和 _（下划线） 。 

标识符不能以数字开头。 

标识符不能是关键字。 

**命名规范：** **软性建议** 

类名规范：首字母大写，后面每个单词首字母大写（大驼峰式）。 

方法名规范： 首字母小写，后面每个单词首字母大写（小驼峰式）。 

变量名规范：全部小写。  

#### 9、能够定义出所有类型的常量 

```java
public class ConstantDemo { 
  public static void main(String[] args){ //输出整数常量 
  System.out.println(123); //输出小数常量
  System.out.println(0.125); //输出字符常量 
  System.out.println('A'); //输出布尔常量 
  System.out.println(true); //输出字符串常量 
  System.out.println("你好Java"); }
```

#### 10、理解Java中的基本数据类型分类

#### 两大类： 

基本数据类型
	整数型	byte short int long
	浮点型	float double
	字符型	char
	布尔型	boolean

引用数据类型
	字符串、数组、类、接口、Lambda

四类八种基本数据类型： 

![截屏2020-12-15 下午7.15.51](/Users/junion/GitHub/Macapp/截屏2020-12-15 下午7.15.51.png) 

注意事项：
1. 字符串不是基本类型，而是引用类型。
2. 浮点型可能只是一个近似值，并非精确的值。
3. 数据范围与字节数不一定相关，例如float数据范围比long更加广泛，但是float是4字节，long是8字节。
4. 浮点数当中默认类型是double。如果一定要使用float类型，需要加上一个后缀F。
   如果是整数，默认为int类型，如果一定要使用long类型，需要加上一个后缀L。推荐使用大写字母后缀。

#### 11、能够定义8种基本数据集类型的变量 

变量定义的格式包括三个要素： 数据类型 、 变量名 、 数据值 。 

**格式**

数据类型 变量名 = 数据值;

```java
public class Variable { 
  public static void main(String[] args){ 
    //定义字节型变量
    byte b = 100; System.out.println(b); 
    //定义短整型变量
    short s = 1000; System.out.println(s); 
    //定义整型变量 
    int i = 123456; System.out.println(i);
    //定义长整型变量 
    long l = 12345678900L;
    System.out.println(l);
    //定义单精度浮点型变量 
    float f = 5.5F; System.out.println(f); 
    //定义双精度浮点型变量 
    double d = 8.5; System.out.println(d);
    //定义布尔型变量 
    boolean bool = false; System.out.println(bool); 
    //定义字符型变量 
    char c = 'A'; System.out.println(c);
  } }
```

变量名称：在同一个大括号范围内，变量的名字不可以相同。 

变量赋值：定义的变量，不赋值不能使用

