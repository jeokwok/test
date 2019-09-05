# Java基础学习记录资料分享
一个纯新手的快速入门，言简意赅，来自一个自学者的提要。参考和部分转载[http://www.runoob.com/java/java-tutorial.html]
## Java简介 
图片[]
Java 是由Sun Microsystems公司于1995年5月推出的高级程序设计语言。</br>
Java可运行于多个平台，如Windows, Mac OS，及其他多种UNIX版本的系统。</br>
本教程通过简单的实例将让大家更好的了解JAVA编程语言。Java语言的特点简单、解释性、面向对象、健壮、动态、高性能、多线程、分布式处理、安全性、开源、结构中立、跨平台。 3大特性  1.安全性  2.虚拟机JVM（一次编译到处运行） 3.GC垃圾回收机制
## 开发环境配置、开发工具的安装
环境配置、安装各开发工具网上教程是比较多且详细，具体可以百度或参考 [http://www.runoob.com/java/java-environment-setup.html] 

算法导论资料  https://blog.csdn.net/mao_hui_fei/article/details/83453168
Android设计模式 https://www.cnblogs.com/android-blogs/p/5530239.html
兼职网站：   taskcity： http://www.taskcity.com/
            软件商务网： www.bizsofts.com/
                        https://www.sxsoft.com/
开源数据集网站  1.   aws.amazon.com      2.  www.data.gov   3. data.worldbank.org
学习网站  掘金   慕课网    小猿圈  B站 </br>
论坛 https://stackoverflow.com      codeproject    forums.devshed.com    www.xda-developers.com </br>
练习网站  codeHS    codechef    lintcode   programming praxis  </br>
 
##  基础语法
1. 编写Java程序时，应注意以下几点：</br>
 大小写敏感：Java是大小写敏感的，这就意味着标识符Hello与hello是不同的。严格区分大小写</br>
 类名：对于所有的类来说，类名的首字母应该大写。如果类名由若干单词组成，那么每个单词的首字母应该大写，例如 MyFirstJavaClass 。</br>
 方法名：所有的方法名都应该以小写字母开头。如果方法名含有若干单词，则后面的每个单词首字母大写。</br>
 源文件名：源文件名必须和类名相同。当保存文件的时候，你应该使用类名作为文件名保存（切记Java是大小写敏感的），文件名的后缀为.java。（如果文件名和类     名不相同则会导致编译错误）。
 主方法入口：所有的Java 程序由public static void main(String []args)方法开始执行。</br>

1. 标识符 可参考阿里巴巴Java开发手册（公开版）有需要自行百度</br>
所有的标识符都应该以字母（A-Z或者a-z）,美元符（$）、或者下划线（_）开始</br>
首字符之后可以是字母（A-Z或者a-z）,美元符（$）、下划线（_）或数字的任何字符组合</br>
关键字不能用作标识符</br>
标识符是大小写敏感的</br>
合法标识符举例：age、$salary、_value、__1_value</br>
非法标识符举例：123abc、-salary</br>

1. 枚举
   Java 5.0引入了枚举，枚举限制变量只能是预先设定好的值。使用枚举可以减少代码中的bug。</br>
   例如，我们为果汁店设计一个程序，它将限制果汁为小杯、中杯、大杯。这就意味着它不允许顾客点除了这三种尺寸外的果汁。</br>
   

## 对象和类
1. 一个Java程序可以认为是一系列对象的集合，而这些对象通过调用彼此的方法来协同工作。下面简要介绍下类、对象、方法和实例变量的概念。</br>
1. 对象：对象是类的一个实例，有状态和行为。例如，一条狗是一个对象，它的状态有：颜色、名字、品种；行为有：摇尾巴、叫、吃等。</br>
1. 类：类是一个模板，它描述一类对象的行为和状态。</br>
1. 方法：方法就是行为，一个类可以有很多方法。逻辑运算、数据修改以及所有动作都是在方法中完成的。</br>
1. 实例变量：每个对象都有独特的实例变量，对象的状态由这些实例变量的值决定。</br>

## 基本数据类类型 （存储在栈区）
8大基本类型  byte1个字节  short2个字节  int4个字节   long8个字节  char1个字节   float4个字节  double8个字节  boolean1个字节 
引用类型 引用的为对象
## 变量类型
 ### 局部变量 Java中所有变量使用前必须先声明 type identifier [ = value][, identifier [= value] ...] ;
 局部变量声明在方法、构造方法或者语句块中；
 局部变量在方法、构造方法、或者语句块被执行的时候创建，当它们执行完成后，变量将会被销毁；
 访问修饰符不能用于局部变量；
 局部变量只在声明它的方法、构造方法或者语句块中可见；
 局部变量是在栈上分配的。
 局部变量没有默认值，所以局部变量被声明后，必须经过初始化，才可以使用。
 
 ### 实例变量 （成员变量） 在类的声明中，属性是用变量来表示的。这种变量就称为实例变量，是在类声明的内部但是在类的其他成员方法之外声明的。类的每个对象维护它自己的一份实例变量的副本。
 实例变量声明在一个类中，但在方法、构造方法和语句块之外；</br>
 当一个对象被实例化之后，每个实例变量的值就跟着确定；</br>
 实例变量在对象创建的时候创建，在对象被销毁的时候销毁；</br>
 实例变量的值应该至少被一个方法、构造方法或者语句块引用，使得外部能够通过这些方式获取实例变量信息；</br>
 实例变量可以声明在使用前或者使用后；</br>
 访问修饰符可以修饰实例变量；</br>
 实例变量对于类中的方法、构造方法或者语句块是可见的。一般情况下应该把实例变量设为私有。通过使用访问修饰符可以使实例变量对子类可见；</br>
 实例变量具有默认值。数值型变量的默认值是0，布尔型变量的默认值是false，引用类型变量的默认值是null。变量的值可以在声明时指定，也可以在构造方法中指定；</br>
 实例变量可以直接通过变量名访问。但在静态方法以及其他类中，就应该使用完全限定名：ObejectReference.VariableName。</br>
 
 ### 类变量（静态变量）
 类变量也称为静态变量，在类中以 static 关键字声明，但必须在方法之外。</br>
 无论一个类创建了多少个对象，类只拥有类变量的一份拷贝。</br>
 静态变量除了被声明为常量外很少使用。常量是指声明为public/private，final和static类型的变量。常量初始化后不可改变。</br>
 静态变量储存在静态存储区。经常被声明为常量，很少单独使用static声明变量。</br>
 静态变量在第一次被访问时创建，在程序结束时销毁。</br>
 与实例变量具有相似的可见性。但为了对类的使用者可见，大多数静态变量声明为public类型。</br>
 默认值和实例变量相似。数值型变量默认值是0，布尔型默认值是false，引用类型默认值是null。变量的值可以在声明的时候指定，也可以在构造方法中指定。此外，静   态变量还可以在静态语句块中初始化。</br>
 静态变量可以通过：ClassName.VariableName的方式访问。</br>
 类变量被声明为public static final类型时，类变量名称一般建议使用大写字母。如果静态变量不是public和final类型，其命名方式与实例变量以及局部变量的命名   方式一致。</br>


## 修饰符
访问控制修饰符 : default, public , protected, private</br>
Java中，可以使用访问控制符来保护对类、变量、方法和构造方法的访问。Java 支持 4 种不同的访问权限。</br>
default (即缺省，什么也不写）: 在同一包内可见，不使用任何修饰符。使用对象：类、接口、变量、方法。</br>
private : 在同一类内可见。使用对象：变量、方法。 注意：不能修饰类（外部类）</br>
私有访问修饰符-private</br>
私有访问修饰符是最严格的访问级别，所以被声明为 private 的方法、变量和构造方法只能被所属类访问，并且类和接口不能声明为 private。</br>
声明为私有访问类型的变量只能通过类中公共的 getter 方法被外部类访问。</br>
Private 访问修饰符的使用主要用来隐藏类的实现细节和保护类的数据。</br>

public : 对所有类可见。使用对象：类、接口、变量、方法</br>
被声明为 public 的类、方法、构造方法和接口能够被任何其他类访问。</br> 
如果几个相互访问的 public 类分布在不同的包中，则需要导入相应 public 类所在的包。由于类的继承性，类所有的公有方法和变量都能被其子类继承。 </br>

protected : 对同一包内的类和所有子类可见。使用对象：变量、方法。 注意：不能修饰类（外部类）。</br>
rotected 需要从以下两个点来分析说明：</br>
子类与基类在同一包中：被声明为 protected 的变量、方法和构造器能被同一个包中的任何其他类访问；</br>
子类与基类不在同一包中：那么在子类中，子类实例可以访问其从基类继承而来的 protected 方法，而不能访问基类实例的protected方法。</br>
protected 可以修饰数据成员，构造方法，方法成员，不能修饰类（内部类除外）。</br>

非访问控制修饰符 : static，final, abstract, static, synchronized</br>
为了实现一些其他的功能，Java 也提供了许多非访问修饰符。</br>
static 修饰符，用来修饰类方法和类变量。</br>
final 修饰符，用来修饰类、方法和变量，final 修饰的类不能够被继承，修饰的方法不能被继承类重新定义，修饰的变量为常量，是不可修改的。</br>
abstract 修饰符，用来创建抽象类和抽象方法。</br>
synchronized 和 volatile 修饰符，主要用于线程的编程。</br>

static 修饰符，用来修饰类方法和类变量。</br>
final 修饰符，用来修饰类、方法和变量，final 修饰的类不能够被继承，修饰的方法不能被继承类重新定义，修饰的变量为常量，是不可修改的。</br>
abstract 修饰符，用来创建抽象类和抽象方法。</br>
synchronized 和 volatile 修饰符，主要用于线程的编程。</br>
static 修饰符</br>
静态变量：</br>
static 关键字用来声明独立于对象的静态变量，无论一个类实例化多少对象，它的静态变量只有一份拷贝。 静态变量也被称为类变量。局部变量不能被声明为 static 变量。 </br>
静态方法：</br>
static 关键字用来声明独立于对象的静态方法。静态方法不能使用类的非静态变量。静态方法从参数列表得到数据，然后计算这些数据。 </br>
对类变量和方法的访问可以直接使用 classname.variablename 和 classname.methodname 的方式访问。 </br>
如下例所示，static修饰符用来创建类方法和类变量。</br>
public class InstanceCounter {</br>
   private static int numInstances = 0;</br>
   protected static int getCount() {</br>
      return numInstances;</br>
   }</br>
 
   private static void addInstance() {</br>
      numInstances++;</br>
   }</br>
 
   InstanceCounter() {</br>
      InstanceCounter.addInstance();</br>
   }</br>
 
   public static void main(String[] arguments) {</br>
      System.out.println("Starting with " +</br>
      InstanceCounter.getCount() + " instances");</br>
      for (int i = 0; i < 500; ++i){</br></br>
         new InstanceCounter();</br>
          }</br>
      System.out.println("Created " +</br>
      InstanceCounter.getCount() + " instances");</br>
   }</br>
}</br>
以上实例运行编辑结果如下:</br>
Starting with 0 instances</br>
Created 500 instances</br>
final 修饰符</br>
final 变量：</br>
final 表示"最后的、最终的"含义，变量一旦赋值后，不能被重新赋值。被 final 修饰的实例变量必须显式指定初始值。</br>
final 修饰符通常和 static 修饰符一起使用来创建类常量。</br>
实例</br>
public class Test{</br>
  final int value = 10;</br>
  // 下面是声明常量的实例</br>
  public static final int BOXWIDTH = 6;</br>
  static final String TITLE = "Manager";</br>
 
  public void changeValue(){</br></br>
     value = 12; //将输出一个错误</br>
  }</br>
}</br>
final 方法</br>
类中的 final 方法可以被子类继承，但是不能被子类修改。</br>
声明 final 方法的主要目的是防止该方法的内容被修改。</br>
如下所示，使用 final 修饰符声明方法。</br>
public class Test{</br>
    public final void changeName(){</br>
       // 方法体</br>
    }</br>
}</br>
final 类</br>
final 类不能被继承，没有类能够继承 final 类的任何特性。</br>
实例</br>
public final class Test {</br>
   // 类体</br>
}</br></br>
abstract 修饰符</br>
抽象类：</br>
抽象类不能用来实例化对象，声明抽象类的唯一目的是为了将来对该类进行扩充。 </br>
一个类不能同时被 abstract 和 final 修饰。如果一个类包含抽象方法，那么该类一定要声明为抽象类，否则将出现编译错误。</br> 
抽象类可以包含抽象方法和非抽象方法。 </br>
实例</br>
abstract class Caravan{</br>
   private double price;</br>
   private String model;</br></br>
   private String year;</br>
   public abstract void goFast(); //抽象方法</br></br>
   public abstract void changeColor();</br>
}</br>
抽象方法</br></br>
抽象方法是一种没有任何实现的方法，该方法的的具体实现由子类提供。</br>
抽象方法不能被声明成 final 和 static。 </br>
任何继承抽象类的子类必须实现父类的所有抽象方法，除非该子类也是抽象类。</br> 
如果一个类包含若干个抽象方法，那么该类必须声明为抽象类。抽象类可以不包含抽象方法。 </br></br>
抽象方法的声明以分号结尾，例如：public abstract sample();。 </br>
实例</br>
public abstract class SuperClass{</br>
    abstract void m(); //抽象方法</br>
}</br>
 
class SubClass extends SuperClass{</br>
     //实现抽象方法</br>
      void m(){</br>
          .........</br>
      }</br>
}</br>
synchronized 修饰符</br>
synchronized 关键字声明的方法同一时间只能被一个线程访问。synchronized 修饰符可以应用于四个访问修饰符。 </br>
实例</br>
public synchronized void showDetails(){</br>
.......</br>
}</br>
transient 修饰符</br>
序列化的对象包含被 transient 修饰的实例变量时，java 虚拟机(JVM)跳过该特定的变量。 </br>
该修饰符包含在定义变量的语句中，用来预处理类和变量的数据类型。 </br>
实例
public transient int limit = 55;   // 不会持久化</br>
public int b; // 持久化</br>
volatile 修饰符</br>
volatile 修饰的成员变量在每次被线程访问时，都强制从共享内存中重新读取该成员变量的值。而且，当成员变量发生变化时，会强制线程将变化值回写到共享内存。这样在任何时刻，两个不同的线程总是看到某个成员变量的同一个值。</br>
一个 volatile 对象引用可能是 null。 </br>
实例
public class MyRunnable implements Runnable
{
    private volatile boolean active;
    public void run()
    {
        active = true;
        while (active) // 第一行
        {
            // 代码
        }
    }
    public void stop()
    {
        active = false; // 第二行
    }
}
通常情况下，在一个线程调用 run() 方法（在 Runnable 开启的线程），在另一个线程调用 stop() 方法。 如果 第一行 中缓冲区的 active 值被使用，那么在 第二行 的 active 值为 false 时循环不会停止。 
但是以上代码中我们使用了 volatile 修饰 active，所以该循环会停止。


## 运算符
计算机的最基本用途之一就是执行数学运算，作为一门计算机语言，Java也提供了一套丰富的运算符来操纵变量。我们可以把运算符分成以下几组：
算术运算符
+
加法 - 相加运算符两侧的值
A + B 等于 30
-
减法 - 左操作数减去右操作数
A – B 等于 -10
*
乘法 - 相乘操作符两侧的值
A * B等于200
/
除法 - 左操作数除以右操作数
B / A等于2
％
取余 - 左操作数除以右操作数的余数
B%A等于0
++
自增: 操作数的值增加1
B++ 或 ++B 等于 21（区别详见下文）
--
自减: 操作数的值减少1
B-- 或 --B 等于 19（区别详见下文）
1、自增（++）自减（--）运算符是一种特殊的算术运算符，在算术运算符中需要两个操作数来进行运算，而自增自减运算符是一个操作数。

关系运算符
==
检查如果两个操作数的值是否相等，如果相等则条件为真。
（A == B）为假。
!=
检查如果两个操作数的值是否相等，如果值不相等则条件为真。
(A != B) 为真。
> 
检查左操作数的值是否大于右操作数的值，如果是那么条件为真。
（A> B）为假。
< 
检查左操作数的值是否小于右操作数的值，如果是那么条件为真。
（A <B）为真。
>=
检查左操作数的值是否大于或等于右操作数的值，如果是那么条件为真。
（A> = B）为假。
<=
检查左操作数的值是否小于或等于右操作数的值，如果是那么条件为真。
（A <= B）为真。

位运算符
＆
如果相对应位都是1，则结果为1，否则为0
（A＆B），得到12，即0000 1100 </br>
|
如果相对应位都是0，则结果为0，否则为1
（A | B）得到61，即 0011 1101 </br>
^
如果相对应位值相同，则结果为0，否则为1
（A ^ B）得到49，即 0011 0001 </br>
〜
按位取反运算符翻转操作数的每一位，即0变成1，1变成0。
（〜A）得到-61，即1100 0011 </br>
<< 
按位左移运算符。左操作数按位左移右操作数指定的位数。
A << 2得到240，即 1111 0000 </br>
>> 
按位右移运算符。左操作数按位右移右操作数指定的位数。
A >> 2得到15即 1111 </br>
>>> 
按位右移补零操作符。左操作数的值按右操作数指定的位数右移，移动得到的空位以零填充。
A>>>2得到15即0000 1111 </br>

逻辑运算符
&&称为逻辑与运算符。当且仅当两个操作数都为真，条件才为真。
（A && B）为假。 </br> 
| |称为逻辑或操作符。如果任何两个操作数任何一个为真，条件为真。
（A | | B）为真。</br>
！称为逻辑非运算符。用来反转操作数的逻辑状态。如果条件为true，则逻辑非运算符将得到false。
！（A && B）为真。</br>
    短路逻辑运算符

赋值运算符
=
简单的赋值运算符，将右操作数的值赋给左侧操作数
C = A + B将把A + B得到的值赋给C
+ =
加和赋值操作符，它把左操作数和右操作数相加赋值给左操作数
C + = A等价于C = C + A
- =
减和赋值操作符，它把左操作数和右操作数相减赋值给左操作数
C - = A等价于C = C -
 A
* =
乘和赋值操作符，它把左操作数和右操作数相乘赋值给左操作数
C * = A等价于C = C * A
/ =
除和赋值操作符，它把左操作数和右操作数相除赋值给左操作数
C / = A等价于C = C / A
（％）=
取模和赋值操作符，它把左操作数和右操作数取模后赋值给左操作数
C％= A等价于C = C％A
<< =
左移位赋值运算符
C << = 2等价于C = C << 2
>> =
右移位赋值运算符
C >> = 2等价于C = C >> 2
＆=
按位与赋值运算符
C＆= 2等价于C = C＆2
^ =
按位异或赋值操作符
C ^ = 2等价于C = C ^ 2
| =
按位或赋值操作符
C | = 2等价于C = C | 2

其他运算符
条件运算符也被称为三元运算符。该运算符有3个操作数，并且需要判断布尔表达式的值。该运算符的主要是决定哪个值应该赋值给变量。
variable x = (expression) ? value if true : value if false

instanceof 运算符
该运算符用于操作对象实例，检查该对象是否是一个特定类型（类类型或接口类型）。
instanceof运算符使用格式如下：
( Object reference variable ) instanceof  (class/interface type）

## 循环结构
顺序结构的程序语句只能被执行一次。如果您想要同样的操作执行多次,，就需要使用循环结构。 
Java中有三种主要的循环结构：
while 循环
do…while 循环
for 循环
Java 增强 for 循环
Java5 引入了一种主要用于数组的增强型 for 循环。
Java 增强 for 循环语法格式如下:
for(声明语句 : 表达式)
{
   //代码句子
}
声明语句：声明新的局部变量，该变量的类型必须和数组元素的类型匹配。其作用域限定在循环语句块，其值与此时数组元素的值相等。 
表达式：表达式是要访问的数组名，或者是返回值为数组的方法。

break 关键字
break 主要用在循环语句或者 switch 语句中，用来跳出整个语句块。 
break 跳出最里层的循环，并且继续执行该循环下面的语句。

continue 关键字
continue 适用于任何循环控制结构中。作用是让程序立刻跳转到下一次循环的迭代。 
在 for 循环中，continue 语句使程序立即跳转到更新语句。 
在 while 或者 do…while 循环中，程序立即跳转到布尔表达式的判断语句。

## 条件语句
一个 if 语句包含一个布尔表达式和一条或多条语句。
if 语句后面可以跟 else if…else 语句，这种语句可以检测到多种可能的情况。

使用 if，else if，else 语句的时候，需要注意下面几点：

if 语句至多有 1 个 else 语句，else 语句在所有的 else if 语句之后。
if 语句可以有若干个 else if 语句，它们必须在 else 语句之前。
一旦其中一个 else if 语句检测为 true，其他的 else if 以及 else 语句都将跳过执行。

switch case 语句有如下规则：
switch 语句中的变量类型可以是： byte、short、int 或者 char。从 Java SE 7 开始，switch 支持字符串 String 类型了，同时 case 标签必须为字符串常量或字面量。
switch 语句可以拥有多个 case 语句。每个 case 后面跟一个要比较的值和冒号。
case 语句中的值的数据类型必须与变量的数据类型相同，而且只能是常量或者字面常量。
当变量的值与 case 语句的值相等时，那么 case 语句之后的语句开始执行，直到 break 语句出现才会跳出 switch 语句。
当遇到 break 语句时，switch 语句终止。程序跳转到 switch 语句后面的语句执行。case 语句不必须要包含 break 语句。如果没有 break 语句出现，程序会继续执行下一条 case 语句，直到出现 break 语句。
switch 语句可以包含一个 default 分支，该分支一般是 switch 语句的最后一个分支（可以在任何位置，但建议在最后一个）。default 在没有 case 语句的值和变量值相等的时候执行。default 分支不需要 break 语句。
switch case 执行时，一定会先进行匹配，匹配成功返回当前 case 的值，再根据是否有 break，判断是否继续输出，或是跳出判断。


## 数组 
概念   定义  byte[] b 
数组初始化（实例化） 2种方法 指定数值初始化 int[] i = {1,2,3,4,5}; int[] i = new int[];
Java 语言中提供的数组是用来存储固定大小的同类型元素。
数组索引是在栈上，根据索引指向堆区的内存（）
数组是储存在堆上的对象，可以保存多个同类型变量。
数组2大异常 1.空指针异常  2.数组索引越界
二维数组
## 日期和时间
Java.util包提供了Date类来封装日期和时间java.util 包提供了 Date 类来封装当前的日期和时间。 Date 类提供两个构造函数来实例化 Date 对象。

第一个构造函数使用当前日期和时间来初始化对象。

Date( )
第二个构造函数接收一个参数，该参数是从1970年1月1日起的毫秒数。

Date(long millisec)

##  正则表达式
Java 正则表达式
正则表达式定义了字符串的模式。
正则表达式可以用来搜索、编辑或处理文本。
正则表达式并不仅限于某一种语言，但是在每种语言中有细微的差别。

## Java 流(Stream)、文件(File)和IO
Java.io 包几乎包含了所有操作输入、输出需要的类。所有这些流类代表了输入源和输出目标。

Java.io 包中的流支持很多种格式，比如：基本类型、对象、本地化字符集等等。

一个流可以理解为一个数据的序列。输入流表示从一个源读取数据，输出流表示向一个目标写数据。

Java 为 I/O 提供了强大的而灵活的支持，使其更广泛地应用到文件传输和网络编程中。
Java 的控制台输入由 System.in 完成。

为了获得一个绑定到控制台的字符流，你可以把 System.in 包装在一个 BufferedReader 对象中来创建一个字符流。
下面是创建 BufferedReader 的基本语法：
BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
                      
## 异常处理
Java 异常处理
异常是程序中的一些错误，但并不是所有的错误都是异常，并且错误有时候是可以避免的。 
比如说，你的代码少了一个分号，那么运行出来结果是提示是错误 java.lang.Error；如果你用System.out.println(11/0)，那么你是因为你用0做了除数，会抛出 java.lang.ArithmeticException 的异常。 
异常发生的原因有很多，通常包含以下几大类：
用户输入了非法数据。
要打开的文件不存在。
网络通信时连接中断，或者JVM内存溢出。
这些异常有的是因为用户错误引起，有的是程序错误引起的，还有其它一些是因为物理错误引起的。-
要理解Java异常处理是如何工作的，你需要掌握以下三种类型的异常： 
检查性异常：最具代表的检查性异常是用户错误或问题引起的异常，这是程序员无法预见的。例如要打开一个不存在文件时，一个异常就发生了，这些异常在编译时不能被简单地忽略。
运行时异常： 运行时异常是可能被程序员避免的异常。与检查性异常相反，运行时异常可以在编译时被忽略。
错误： 错误不是异常，而是脱离程序员控制的问题。错误在代码中通常被忽略。例如，当栈溢出时，一个错误就发生了，它们在编译也检查不到的。

Exception 类的层次
所有的异常类是从 java.lang.Exception 类继承的子类。 
Exception 类是 Throwable 类的子类。除了Exception类外，Throwable还有一个子类Error 。 
Java 程序通常不捕获错误。错误一般发生在严重故障时，它们在Java程序处理的范畴之外。 
Error 用来指示运行时环境发生的错误。 
![](https://github.com/jeokwok/studytoshare/blob/master/12-130Q1234I6223.jpg)      
例如，JVM 内存溢出。一般地，程序不会从错误中恢复。 
异常类有两个主要的子类：IOException 类和 RuntimeException 类。

使用 try 和 catch 关键字可以捕获异常。try/catch 代码块放在异常可能发生的地方。 
try catch  finally 
try/catch代码块中的代码称为保护代码，使用 try/catch 的语法如下： 
try
{
   // 程序代码
}catch(ExceptionName e1)
{
   //Catch 块
}
注意下面事项：</br>
catch 不能独立于 try 存在。</br>
在 try/catch 后面添加 finally 块并非强制性要求的。</br>
try 代码后不能既没 catch 块也没 finally 块。</br>
try, catch, finally 块之间不能添加任何代码。</br>

声明自定义异常
在 Java 中你可以自定义异常。编写自己的异常类时需要记住下面的几点。
所有异常都必须是 Throwable 的子类。
如果希望写一个检查性异常类，则需要继承 Exception 类。
如果你想写一个运行时异常类，那么需要继承 RuntimeException 类。
可以像下面这样定义自己的异常类：
class MyException extends Exception{
}
只继承Exception 类来创建的异常类是检查性异常类。 
下面的 InsufficientFundsException 类是用户定义的异常类，它继承自 Exception。 
一个异常类和其它任何类一样，包含有变量和方法。 

通用异常
在Java中定义了两种类型的异常和错误。</br>
JVM(Java虚拟机) 异常：由 JVM 抛出的异常或错误。例如：NullPointerException 类，ArrayIndexOutOfBoundsException 类，ClassCastException 类。
程序级异常：由程序或者API程序抛出的异常。例如 IllegalArgumentException 类，IllegalStateException 类。</br>

## 小技巧
1. 注释
   2种注释方式   //   单行注释  ;  /* string body */ 多行注释  /** string body*/  说明注释允许你在程序中嵌入关于程序的信息。你可以使用 javadoc 工具软件来生成信息，并输出到HTML文件中。具体参考[https://jingyan.baidu.com/article/eb9f7b6d4b1f6a869364e83d.html]
说明注释，使你更加方便的记录你的程序信息。
   空行 Java是无视空行 为了代码的优雅清爽 建议是适当使用
   /** 方法的头上 回车
   ##函数注释参数信息 
   1.Android Studio ->File -> Setting -> Keymap ->发现框输入comment -> 选择Other的Fix doc comment 
   选择 Add keyboard shortcut 添加你自己喜欢的快捷方式（快捷键） 将鼠标光标放置到你想要添加方法注释的
   方法前,按下你自己设置的快捷方式. 就自动生成了方法注释了. 

简而言之：框架是大智慧，用来对软件设计进行分工；设计模式是小技巧，对具体问题提出解决方案，以提高代码复用率，降低耦合度。
   
# 面向对象

## 继承
继承的概念（Java为单根继承）</br>
继承是java面向对象编程技术的一块基石，因为它允许创建分等级层次的类。</br>
继承就是子类继承父类的特征和行为，使得子类对象（实例）具有父类的实例域和方法，或子类从父类继承方法，使得子类具有父类相同的行为。 </br>
所以继承需要符合的关系是：is-a，父类更通用，子类更具体。</br>
子类是不继承父类的构造器（构造方法或者构造函数）的，它只是调用（隐式或显式）。如果父类的构造器带有参数，则必须在子类的构造器中显式地通过 super 关键字调用父类的构造器并配以适当的参数列表。</br>
如果父类构造器没有参数，则在子类的构造器中不需要使用 super 关键字调用父类构造器，系统会自动调用父类的无参构造器。</br> 
super关键字：我们可以通过super关键字来实现对父类成员的访问，用来引用当前对象的父类。</br>
this关键字：指向自己的引用。</br>

继承的特性
子类拥有父类非 private 的属性、方法。</br>

子类可以拥有自己的属性和方法，即子类可以对父类进行扩展。</br>

子类可以用自己的方式实现父类的方法。</br>

Java 的继承是单继承，但是可以多重继承，单继承就是一个子类只能继承一个父类，多重继承就是，例如 A 类继承 B 类，B 类继承 C 类，所以按照关系就是 C 类是 B 类的父类，B 类是 A 类的父类，这是 Java 继承区别于 C++ 继承的一个特性。</br>

提高了类之间的耦合性（继承的缺点，耦合度高就会造成代码之间的联系越紧密，代码独立性越差）。</br>


继承关键字
继承可以使用 extends 和 implements 这两个关键字来实现继承，而且所有的类都是继承于 java.lang.Object，当一个类没有继承的两个关键字，则默认继承object（这个类在 java.lang 包中，所以不需要 import）祖先类。

extends关键字
在 Java 中，类的继承是单一继承，也就是说，一个子类只能拥有一个父类，所以 extends 只能继承一个类

implements关键字
使用 implements 关键字可以变相的使java具有多继承的特性，使用范围为类继承接口的情况，可以同时继承多个接口（接口跟接口之间采用逗号分隔）。

super 与 this 关键字
super关键字：我们可以通过super关键字来实现对父类成员的访问，用来引用当前对象的父类。
this关键字：指向自己的引用。

final关键字
final关键字
final 关键字声明类可以把类定义为不能继承，即终类 ，也可以用于修饰方法，这个方法是不能被子类重写；
final 关键字声明类可以把类定义为不能继承的，即最终类；或者用于修饰方法，该方法不能被子类重写：

声明类：
final class 类名 {//类体}
声明方法：
修饰符(public/private/default/protected) final 返回值类型 方法名(){//方法体}
注:实例变量也可以被定义为 final，被定义为 final 的变量不能被修改。被声明为 final 类的方法自动地声明为 final，但是实例变量并不是 final
实例变量也是可以被定义为final，被定义为final的变量是不能被修改。被声明为final类的方法自动声明为final，但是实例变量并不是final

构造器
子类是不继承父类的构造器（构造方法或者构造函数）的，它只是调用（隐式或显式）。如果父类的构造器带有参数，则必须在子类的构造器中显式地通过 super 关键字
子类是不继承父类的构造器（构造方法或构造函数），只是调用。如果父类的构造您好带有蚕食，则必须在子类的构造器中显式的通过super关键字调用父类的构造器并配以适当的参数列表。
调用父类的构造器并配以适当的参数列表。
如果父类构造器没有参数，则在子类的构造器中不需要使用 super 关键字调用父类构造器，系统会自动调用父类的无参构造器。
如果父类构造器没有蚕食，则在子类的构造器中不需要使用 super 关键字调用父类构造器，系统会自动调用父类的无参构造器。

## 重载和重写

重写(Override)  重写 是指子类在继承父类的时候，父类的方法是不能够满足需要，子类重写父类的同名方法，用于拓展功能 
重写是子类对父类的允许访问的方法的实现过程进行重新编写, 返回值和形参都不能改变。即外壳不变，核心重写！ 
重写的好处在于子类可以根据需要，定义特定于自己的行为。 也就是说子类能够根据需要实现父类的方法。
重写方法不能抛出新的检查异常或者比被重写方法申明更加宽泛的异常。例如： 父类的一个方法申明了一个检查异常 IOException，但是在重写这个方法的时候不能抛出 Exception 异常，因为 Exception 是 IOException 的父类，只能抛出 IOException 的子类异常。 
方法的重写规则</br>
参数列表必须完全与被重写方法的相同；</br>
返回类型与被重写方法的返回类型可以不相同，但是必须是父类返回值的派生类（java5 及更早版本返回类型要一样，java7 及更高版本可以不同）；</br>
访问权限不能比父类中被重写的方法的访问权限更低。例如：如果父类的一个方法被声明为public，那么在子类中重写该方法就不能声明为protected。</br>
父类的成员方法只能被它的子类重写。</br>
声明为final的方法不能被重写。</br>
声明为static的方法不能被重写，但是能够被再次声明。</br>
子类和父类在同一个包中，那么子类可以重写父类所有方法，除了声明为private和final的方法。</br>
子类和父类不在同一个包中，那么子类只能够重写父类的声明为public和protected的非final方法。</br>
重写的方法能够抛出任何非强制异常，无论被重写的方法是否抛出异常。但是，重写的方法不能抛出新的强制性异常，或者比被重写方法声明的更广泛的强制性异常，反之则可以。</br>
构造方法不能被重写。</br>
如果不能继承一个方法，则不能重写这个方法。</br>
需要在子类中使用被重写的方法时，使用关键字super关键字。</br>
当需要在子类中调用父类的被重写方法时，要使用super关键字。</br> 

重载 是指方法在类里，可以写多个同名的方法，以参数来区分方法。</br>
       在调用方法的时候是根据所传的参数来判断重载的方法</br>
 重载(overloading) 是在一个类里面，方法名字相同，而参数不同。返回类型可以相同也可以不同。</br>
每个重载的方法（或者构造函数）都必须有一个独一无二的参数类型列表。</br>
最常用的地方就是构造器的重载。</br>
重载规则:</br>
被重载的方法必须改变参数列表(参数个数或类型不一样)；</br>
被重载的方法可以改变返回类型；</br>
被重载的方法可以改变访问修饰符；</br>
被重载的方法可以声明新的或更广的检查异常；</br>
方法能够在同一个类中或者在一个子类中被重载。</br></br>
无法以返回值类型作为重载函数的区分标准。 </br>
 
 方法的重写(Overriding)和重载(Overloading)是java多态性的不同表现，重写是父类与子类之间多态性的一种表现，重载可以理解成多态的具体表现形式。</br>
(1)方法重载是一个类中定义了多个方法名相同,而他们的参数的数量不同或数量相同而类型和次序不同,则称为方法的重载(Overloading)。</br>
(2)方法重写是在子类存在方法与父类的方法的名字相同,而且参数的个数与类型一样,返回值也一样的方法,就称为重写(Overriding)。</br>
(3)方法重载是一个类的多态性表现,而方法重写是子类与父类的一种多态性表现。</br>
## 多态
多态是同一个行为具有多个不同表现形式或形态的能力。</br>
多态的优点 </br>
1. 消除类型之间的耦合关系</br>
2. 可替换性</br>
3. 可扩充性</br>
4. 接口性</br>
5. 灵活性</br>
6. 简化性</br>
多态存在的三个必要条件</br>
继承</br>
重写</br>
父类引用指向子类对象</br>
当使用多态方式调用方法时，首先检查父类中是否有该方法，如果没有，则编译错误；如果有，再去调用子类的同名方法。</br>
多态的好处：可以使程序有良好的扩展，并可以对所有类的对象进行通用处理。</br>
虚函数</br>
虚函数的存在是为了多态。</br>

Java 中其实没有虚函数的概念，它的普通函数就相当于 C++ 的虚函数，动态绑定是Java的默认行为。如果 Java 中不希望某个函数具有虚函数特性，可以加上 final 关键字变成非虚函数。</br>
多态的实现方式</br>
方式一：重写： </br>
这个内容已经在上一章节详细讲过，就不再阐述，详细可访问：Java 重写(Override)与重载(Overload)。</br>

方式二：接口 </br>
1. 生活中的接口最具代表性的就是插座，例如一个三接头的插头都能接在三孔插座中，因为这个是每个国家都有各自规定的接口规则，有可能到国外就不行，那是因为国外自己定义的接口类型。</br>
2. java中的接口类似于生活中的接口，就是一些方法特征的集合，但没有方法的实现。具体可以看 java接口 这一章节的内容。</br>
方式三：抽象类和抽象方法 </br>

## 抽象
   抽象类 里面是没有具体的实现方法，用abstract 修饰  ，继承抽象类是必须要实现抽象类的方法 一般是override </br> 
   主要是用来抽取物体比较单一的功能，并不提供具体的实现方式  实现程序的分类</br>
  
   
   抽象方法 一个类里面包含抽象方法，这个类一定是抽象类</br>
   在面向对象的概念中，所有的对象都是通过类来描绘的，但是反过来，并不是所有的类都是用来描绘对象的，如果一个类中没有包含足够的信息来描绘一个具体的对   象，这样的类就是抽象类。 </br>
抽象类除了不能实例化对象之外，类的其它功能依然存在，成员变量、成员方法和构造方法的访问方式和普通类一样。</br>
由于抽象类不能实例化对象，所以抽象类必须被继承，才能被使用。也是因为这个原因，通常在设计阶段决定要不要设计抽象类。</br>
父类包含了子类集合的常见的方法，但是由于父类本身是抽象的，所以不能使用这些方法。</br>
在Java中抽象类表示的是一种继承关系，一个类只能继承一个抽象类，而一个类却可以实现多个接口。</br>

抽象方法</br>
如果你想设计这样一个类，该类包含一个特别的成员方法，该方法的具体实现由它的子类确定，那么你可以在父类中声明该方法为抽象方法。</br>

Abstract 关键字同样可以用来声明抽象方法，抽象方法只包含一个方法名，而没有方法体。</br>

抽象方法没有定义，方法名后面直接跟一个分号，而不是花括号。</br>

抽象类总结规定
1. 抽象类不能被实例化(初学者很容易犯的错)，如果被实例化，就会报错，编译无法通过。只有抽象类的非抽象子类可以创建对象。
2. 抽象类中不一定包含抽象方法，但是有抽象方法的类必定是抽象类。
3. 抽象类中的抽象方法只是声明，不包含方法体，就是不给出方法的具体实现也就是方法的具体功能。
4. 构造方法，类方法（用 static 修饰的方法）不能声明为抽象方法。
5. 抽象类的子类必须给出抽象类中的抽象方法的具体实现，除非该子类也是抽象类。

## 封装
在面向对象程式设计方法中，封装（英语：Encapsulation）是指一种将抽象性函式接口的实现细节部份包装、隐藏起来的方法。 
封装可以被认为是一个保护屏障，防止该类的代码和数据被外部类定义的代码随机访问。
要访问该类的代码和数据，必须通过严格的接口控制。
封装最主要的功能在于我们能修改自己的实现代码，而不用修改那些调用我们代码的程序片段。
适当的封装可以让程式码更容易理解与维护，也加强了程式码的安全性。
封装的优点
1. 良好的封装能够减少耦合。
2. 类内部的结构可以自由修改。
3. 可以对成员变量进行更精确的控制。
4. 隐藏信息，实现细节。

实现Java封装的步骤
1. 修改属性的可见性来限制对属性的访问（一般限制为private）
采用 this 关键字是为了解决实例变量（private String name）和局部变量（setName(String name)中的name变量）之间发生的同名的冲突。

通常情况下，这些方法被称为getter和setter方法。构建实体类，谁封装，谁提供set和get方法。
因此，任何要访问类中私有成员变量的类都要通过这些getter和setter方法。

   1. 类的属性private 私有属性是无法在外部类是没办法调用，作用域是当前类，在本类中调用本类属性。提供下get（返回获取属性的返回值）、set方法。
   1. 类的属性private 私有属性是无法在外部类是没办法调用，作用域是当前类。在本类中调用本类属性。提供下get（返回获取属性的返回值）、set方法用于设置对       象的属性值；
    
  设计模式之单例模式   （饿汉和懒汉2中模式）
  饿汉模式 私有化构造器，  提供一个获取对象的（静态）方法  直接设置静态的属性对象  调用是直接通过类名直接调用方法  比较常用，缺点是空占内存 
  懒汉模式 私有化构造器，  提供一个获取对象的（静态）方法   设置本类属性，在获取对象的方法中判断属性对象是否为null 当属相对象为null 则通过获取对象方法创建对象，属性对象不为空的情况下是不在创建属性对象  有线程安全上的问题</br>
## 接口
接口（英文：Interface），在JAVA编程语言中是一个抽象类型，是抽象方法的集合，接口通常以interface来声明。一个类通过继承接口的方式，从而来继承接口的抽象方法。

接口并不是类，编写接口的方式和类很相似，但是它们属于不同的概念。类描述对象的属性和方法。接口则包含类要实现的方法。</br>
除非实现接口的类是抽象类，否则该类要定义接口中的所有方法。</br>
接口无法被实例化，但是可以被实现。一个实现接口的类，必须实现接口内所描述的所有方法，否则就必须声明为抽象类。另外，在 Java 中，接口类型可用来声明一个变量，他们可以成为一个空指针，或是被绑定在一个以此接口实现的对象。</br>
接口与类相似点：</br>
一个接口可以有多个方法。</br>
接口文件保存在 .java 结尾的文件中，文件名使用接口名。</br></br>
接口的字节码文件保存在 .class 结尾的文件中。</br>
接口相应的字节码文件必须在与包名称相匹配的目录结构中。</br>
接口与类的区别：</br>
接口不能用于实例化对象。</br>
接口没有构造方法。</br>
接口中所有的方法必须是抽象方法。</br>
接口不能包含成员变量，除了 static 和 final 变量。</br>
接口不是被类继承了，而是要被类实现。</br>
接口支持多继承。</br>
接口特性</br>
接口中每一个方法也是隐式抽象的,接口中的方法会被隐式的指定为 public abstract（只能是 public abstract，其他修饰符都会报错）。</br>
接口中可以含有变量，但是接口中的变量会被隐式的指定为 public static final 变量（并且只能是 public，用 private 修饰会报编译错误）。</br>
接口中的方法是不能在接口中实现的，只能由实现接口的类来实现接口中的方法。</br>





  
## 包
Java 包(package)
package 用于封装分类的类 ，为了更好地组织类，Java 提供了包机制，用于区别类名的命名空间。
包的作用
1、把功能相似或相关的类或接口组织在同一个包中，方便类的查找和使用。
2、如同文件夹一样，包也采用了树形目录的存储方式。同一个包中的类名字是不同的，不同的包中的类的名字是可以相同的，当同时调用两个不同包中相同类名的类时，应该加上包名加以区别。因此，包可以避免名字冲突。 
3、包也限定了访问权限，拥有包访问权限的类才能访问某个包中的类。
Java 使用包（package）这种机制是为了防止命名冲突，访问控制，提供搜索和定位类（class）、接口、枚举（enumerations）和注释（annotation）等。 


# Java高级
## 数据结构
## 集合框架
## 泛型
## 序列化
## 网络编程
## 多线程
## 数据库
## 常用库(github)
EventBus   线程组件间通信
1.控件按钮到fram之前的通信
2.线程之间通信 通过子线程发布者  通过线程订阅者的注解设置，实现设置订阅者在的线程设定
官方API资料和简单实例参考

九宫格解锁实现
获取9个点的点击和未点击的bitmap 使用循环画出界面，先确定中间点的坐标信息 在根据这个点的左上角坐标绘出其他点 画出和联动的要点
通过循环画出点  计算点位是否在点上，用于刷新显示被点击的点  创建一个点位的list集合，用来存储选中的点位
获取ontouch事件的屏幕坐标  根据计算a^2 + b^2 = c^2 算出点击的屏幕坐标点，依次循环和9个坐标点的比较，跟据算出这个C的长度判断是否小于等于9个坐标点的
半径，获取点位 然后判断在哪个点位范围  触发在这个点位的绘制，在点击下个点 判断不在范围内刷新绘制
画点  点击事件  画线  画简单线  连接的线

自定义底部导航栏设计  引用库 实现修改（自定义）底部导航栏图片和title
自定义底部导航栏图标 自定义通过一个视图集合来修改  采用MVP 程序设计模式 2个变量值交换   4种方法  

open CV2.20 实现动态监测，实时录影功能，主要用于停车

聊天软件开发 library 基础语言学习  面向对象的引用

自动回复软件的开发 

软件自动化
## 代码结构

   MVC </br>    
               View：对应于布局文件</br> 
               Model：业务逻辑和实体模型</br> 
               Controllor：对应于Activity</br> 
    
    
    MVP结构 </br>
    MVP结构中的 model        数据实体bean 依然是业务逻辑和实体模型  </br> 
               view         对应于Activity，负责View的绘制以及与用户交互</br>
               presenter    负责完成View于Model间的交互</br>
               
               
![](https://github.com/jeokwok/test/blob/master/QQ%E5%9B%BE%E7%89%8720190709181243.png)       
![](https://github.com/jeokwok/test/blob/master/QQ%E5%9B%BE%E7%89%8720190709181302.png) 
## 支持
1.项目还会持续更新。

2.项目仅用于学习和交流，严禁用于任何商业用途。

3.水平有限，如果有什么问题可以留言或是qq联系，370156664

4.感觉有帮助，支持下作者，欢迎点赞和star
