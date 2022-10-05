[TOC]



---

# 一、软件架构

## 1.1. C/S架构

Client和Server：客户端和服务器端，如QQ、LOL等

- 优点：用户体验好
- 缺点：开发、安装、部署、维护麻烦

## 1.2. B/S架构

Browser和Server：浏览器和服务器端，如京东、淘宝等

- 优点：开发、安装、部署、维护简单
- 缺点：用户体验不一定好、对硬件要求高

---

# 二、Java基础

## 2.1.基础语法

### 2.1.1. .JRE(Java Runtime Environment)

- java程序运行时环境，包含JVM和运行时所需要的核心类库

### 2.1.2. JDK(Java Development Kit)

- java程序开发工具包，包含JRE和开发人员使用的工具。其中开发工具：编译工具(javac.exe)和运行工具(java.exe)

- 命令行

- |        操作        |                说明                 |
  | :----------------: | :---------------------------------: |
  |      盘符名称      | 盘符切换。eg：E:回车，表示切换到E盘 |
  |        dir         |        查看当前路径下的内容         |
  |       cd目录       |      进入单级目录。eg：cd xxx       |
  |        cd..        |           回退上一级目录            |
  | cd 目录1\目录2\... |    进入多级目录。eg：cd xxx\xxxx    |
  |        cd\         |           回退到盘符目录            |
  |        cks         |                清屏                 |
  |        exit        |         退出命令提示符窗口          |

### 2.1.3. 命令行中运行java程序

- 进入文件所在地址，编译：javac 文件名.java，执行：java 类名

### 2.1.4. Notepad++下载地址

https://notepad-plus-plus.org/

### 2.1.5.注释分类

- 单行注释，格式：//注释信息
- 多行注释，格式：/*注释信息*/
- 文档注释，格式：/**注释信息*/

### 2.1.6.关键字特点

- 关键字的字母全部小写

### 2.1.7.常量

- 在程序运行过程中，其值不可以发生改变的量，除了空常量其余的都可以在控制台直接输出

- |  常量类型  |         说明         |
  | :--------: | :------------------: |
  | 字符串常量 | 用双引号括起来的内容 |
  |  整数常量  |    不带小数的数字    |
  |  小数常量  |     带小数的数字     |
  |  字符常量  | 用单引号括起来的内容 |
  |  布尔常量  |   布尔值，表示真假   |
  |   空常量   |         空值         |

### 2.1.8.数据类型

- 计算机存储设备的最小单位叫“位(bit)”，也叫作“比特位”，用“b”表示。计算机中最小的存储单元叫“字节(byte)”，用“B”表示。1B=8bit

![image](https://user-images.githubusercontent.com/91715224/193967533-88907d53-8833-439e-b85f-7c71edd566c3.png)


数据类型内存占用和取值范围

<table>
    <tr>
        <td>整数类型</td>
        <td>关键字</td>
        <td>内存占用</td>
        <td>取值范围</td>
    </tr>
    <tr>
        <td rowspan="4">整数</td>
        <td>byte</td>
        <td>1</td>
        <td>-128~127</td>
    </tr>
    <tr>
        <td>short</td>
        <td>2</td>
        <td>-32768~32767</td>
    </tr>
    <tr>
        <td>int(默认)</td>
        <td>4</td>
        <td>-2的31次方~2的31次方-1</td>
    </tr>
    <tr>
        <td>long</td>
        <td>8</td>
        <td>-2的63次方~2的63次方-1</td>
    </tr>
    <tr>
        <td rowspan="2">浮点数</td>
        <td>float</td>
        <td>4</td>
        <td>负数：-3.402823E+38~-1.401298E-45
            正数：4.9000000E-324~1.797693E+308
        </td>
    </tr>
    <tr>
        <td>double</td>
        <td>8</td>
        <td>负数：-1.797693E+308~4.9000000E-324
            正数：4.9000000E-324~1.797693E+308
    </tr>
    <tr>
        <td>字符</td>
        <td>char</td>
        <td>2</td>
        <td>0~65535</td>
    </tr>
    <tr>
        <td>布尔</td>
        <td>boolean</td>
        <td>1</td>
        <td>true、false</td>
    </tr>
</table>

### 2.1.9.变量使用注意事项

- 名字不能重复
- 变量未赋值，不能使用
- Long类型的变量定义的时候，为了防止整数过大，后面要加L
- Float类型的变量定义的时候，为了防止类型不兼容，后面要加F

### 2.1.10.标识符

- 给类、方法、变量等起名字的符号
- 规则：由数字、字母、下划线和美元符组成；不能以数字开头；不能是关键字；区分大小写

常见命名的约定

- 小驼峰命名法（针对方法、变量命名）：标识符是一个单词的时候，首字母小写；标识符由多个单词组成的时候，第一个单词首字母小写，其他单词首字母大写
- 大驼峰命名法（针对类命名）：标识符是一个单词的时候，首字母大写；标识符由多个单词组成的时候，每一个单词首字母大写

类型转换

- 自动类型转换：把一个表示数据范围小的数值或者变量赋值给另一个数据范围大的变量
- 强制类型转换：把一个表示数据范围大的数值或者变量赋值给另一个表示数据范围小的变量。格式：目标数据类型 变量名 = (目标数据类型)值或者变量;

  ![image](https://user-images.githubusercontent.com/91715224/193968289-1c781207-b3d2-41a2-9eac-b3e21e65719c.png)


## 2.2.运算符

- 对常量或者变量进行操作的符号

### 2.2.1.算术运算符

\+ - * / %

#### 字符的“+”操作

- ‘A’ 对应65 A-Z是连续的
- ‘a’ 对应97 a-z是连续的
- ‘0’ 对应45 0-9是连续的

- 算术表达式中包含多个基本类型数据的时候，整个算术表达式的类型会自动提升，规则：byte、short、char类型会被提升到int类型；整个表达式的类型自动提升到表达式中最高等级操作数同样的类型，等级顺序（低到高）：byte→short→char→int→long→float→double。

#### 字符串的“+”操作

- 当“+”操作中出现字符串时，这个“+”是字符串连接符，而不是算术运算符。当“+”操作中，如果出现了字符串，就是连接运算符，否则就是算术运算。当连续进行“+”操作时，从左到右依次执行。

### 2.2.2.赋值运算符

=   +=  -=  *=  /=  %= …

### 2.2.3.自增自减运算符

++ -- …

i++：先赋值再自增

++i：先自增再赋值

### 2.2.4.关系运算符

== != > < >= <=

运算结果为True或者False

### 2.2.5.逻辑运算符

- 用来连接关系表达式的运算符，也可以直接连接布尔类型或者变量。

#### 基本逻辑运算符

- &逻辑与：有False则False
- |逻辑或：有True则True
- ^逻辑异或：相同为False，不同为True
- !逻辑非：False变True，True变False，可以叠加

#### 短路逻辑运算符

- &&短路与：有False则False，有短路效果
- ||短路或：有True则True，有短路效果

#### 注意事项：

- 逻辑与&，无论左边真假，右边都要执行
- 短路与&&，如果左边为真，右边执行，如果左边为假，则右边不执行。
- 逻辑或|，无论左边真假，右边都要执行
- 短路或||，如果左边为假，右边执行，如果左边为真，则右边不执行。

### 2.2.6.三元运算符

- 格式：关系表达式?表达式1:表达式2;
- 规则：首先计算关系表达式的值，如果为True，表达式1的值就是运算结果，如果为False，表达式2的值就是运算结果

## 2.3.数据输入

- Scanner使用步骤：

- ```java
  import java.util.Scanner;//导包
  Scanner sc = new Scanner(System.in);//创建对象
  int i = sc.nextInt(); //接收数据
  /*
  输入一个或多个数据时，只需要写一个Scanner sc = new Scanner(System.in);
  */
  int i1 = sc.nextInt();
  int i2 = sc.nextInt();
  int i3 = sc.nextInt();
  ```

## 2.4.分支语句

- 分类：顺序结构、分支结构(if,switch)、循环结构(for,while,do…while)

### 2.4.1.Switch语句

- ```java
  switch(表达式){
   	case值1:		//后面跟的是要和表达式进行比较的值
  		 语句体1;
   		break;
  	 …
  	 default:	//表示所有情况都不匹配的时候，执行该处内容
   		语句体n+1;
  		 [break;]
  }
  ```

- 注意：在switch语句中，如果case控制的语句体后面不写break，将出现穿透现象，在不判断下一个case值的情况下，向下运行，直到遇到break或者整体switch语句结束

### 2.4.2.for循环语句

- 水仙花数：水仙花数是一个三位数，个位、十位、百位的数字立方和等于原数

- 任意数字的指定位上的数值求法：先使用整除操作将要求的数字移动到个位上，再用取余方法取出最后一位上的值。eg：求X位，用数字整除X，然后将得到的数字用10取余，即可得到指定位上的数值

### 2.4.3.跳转控制语句

- 跳过某次循环体内容的执行，继续下一次的执行：continue 
- 注意：使用是基于条件控制的

- 终止循环体内容的执行，结束当前的整个循环：break  
- 注意：使用是基于条件控制的

### 2.4.4.Random

- ```java
  import java.util.Random;	//导包 
  Random r = new Random();	 //创建对象
  int object = r.nextInt(x);	//获取随机数 
  /*
  	获取数据的范围：[0,x) 包括0，不包括x
  	获取1-x之间的随机数：int number = r.nextInt(x) + 1; 注意有+
  */
  ```

## 2.5.IDEA

### 2.5.1.创见类步骤：

1. 创见一个空项目X
2. 创建一个新模块XX
3.  在XX模块下的src下创建一个包XXX
4. 在XXX包下新建一个类XXXX
5. 在XXXX类中编写代码

### 2.5.2.IDEA项目结构

项目project-->模块1、模块2...-->包1、包2...-->类...

### 2.5.3.IDEA内容辅助键、快捷键

- 快速生成main()方法：psvm + Tab
- 快速生成输出语句：sout + tab
- 注释快捷键：单行：选中代码，Ctrl+/
- ​                    多行：选中代码，Ctrl+Shift+/
- 大小写转化：Ctr + shift + U
- 格式化代码：Alt + 0
- 向前缩进选中代码：Shift+Tab

## 2.6.数组

### 2.6.1.定义格式

-  数据类型[] 变量名
-  数据类型 变量名[]

### 2.6.2.数组初始化方式

#### 动态初始化

- 在创建数组时候 直接指定数组当中的数据元素个数 
- 格式：数据类型[ ] 变量名 = new 数据类型[数组长度];

#### 静态初始化

- 在创建数组的时候，不直接指定数据个数多少，而是直接将具体数据内容进行指定
- 格式：静态类型[ ] 变量名 = new 数据类型 [ ] {元素1，元素2…};
- 简化格式：数据类型[ ] 变量名 = {元素1，元素2…};

### 2.6.3.内存分配

- 栈内存：存储局部变量（定义在方法中的变量），使用完毕，立即消失
- 堆内存：存储new出来的内容（实体，对象），每一个new出来的东西都有一个地址值，使用完毕，会在垃圾回收器空闲时回收

### 2.6.4.多个数组指向一个数组

- 先定义数组1，然后将数组1的地址赋值给定义的数组2，然后修改数组2中的元素，则数组1和数组2中的元素都同时被修改。

### 2.6.5.获取数组元素个数

- 数组名.length

## 2.7.方法

### 2.7.1.成员方法与构造方法

- 构造方法 : 构建对象的方法叫构造方法；成员方法: 封装了特定功能的代码块。构造方法是为了创建一个类的对象，成员方法是封装了特定功能的代码块

- ```java
  //构造方法的格式
    public 类名(形式参数列表){
  	方法体;
    }  注意没有void或者返回类型
    
  //成员方法格式
    public 返回值类型 方法名(形式参数列表){
  	//方法体;(特定功能的代码)
  	return 返回值;
    }
  ```

### 2.7.2.无参数方法的定义与调用

- ```java
  public static viod 方法名(){
   方法体
  }
  
  //调用
  
  方法名();
  
  //在main()中调用
  ```

### 2.7.3.带参数方法的定义与调用

- ```java
  public static viod 方法名(数据类型 变量名){
  		 方法体
  	}
  
  //调用
  
  方法名(变量名/常量值);
  
  //在main()中调用
  ```

### 2.7.4.形参和实参

- 形参：方法定义中的参数
- 实参：方法调用中的参数

### 2.7.5.带返回值方法的定义和调用

- ```java
  public static 数据类型 方法名(数据类型 变量名){
   		return 数据;
  	}
  
  //数据类型必须与return中的数据类型匹配
  
  //调用：
  
  数据类型 变量名 = 方法名(变量名/常量值);
  
  //在main()中调用
  ```

### 2.7.6.注意事项

- 方法不能嵌套定义
- void表示无返回值，可以省略return，也可以单独写return，后面不加数据

### 2.7.7.方法重载

- 概述：方法重载指在同一个类中定义的多个方法之间的关系，满足下列条件的多个方法互相构成重载

1. 多个方法在同一个类中
2. 多个方法具有相同的方法名
3. 多个方法的参数不同，类型不同或者数量不同

- 注意：重载仅针对同一个类方法的名称与参数进行识别，与返回值的类型无关，即不能通过返回值类型不同判定两个方法是否相互构成重载。在同一个类中可以存在多个方法的重载和main()方法，在main()中可以调用重载

### 2.7.8.方法重写

- 子类中出现了与父类中一模一样的方法声明，当子类需要父类的功能，而功能主体子类有自己特有内容时，可以重写父类中的方法，这样即沿袭了父类的功能，有定义了子类特有的内容

- 格式

1. 在子类方法中写上自己特有的功能，然后加super.XXX()，XXX是子类与父类相同名称的方法
2. 在定义子类方法的前一行加上@override，可以帮助检查重写方法的方法声明的准确性

- 注意事项

1. 父类中private修饰的方法子类不能重写，只有public修饰的方法子类才可以重写。
2. 子类访问权限不能比父类低(public>默认>私有)

### 2.7.9.参数传递

- 基本类型
- 对于基本数据类型的参数，形式参数的改变，不影响实际参数的值
- 引用类型
- 对于引用类型的参数，形式参数的改变，影响实际参数的改变

### 2.7.10.输出

- ```java
  System.out.println("内容"); //输出内容并换行
  
  System.out.print("内容");// 输出内容不换行
  ```

## 2.8.Debug

### 2.8.1.Debug操作流程

1. Debug调试，又称断点调试，断点其实是一个标记，即从哪里开始查看
2. 加断点：选择要设置断点的代码行，在行号的区域后面点击鼠标左键即可
3. 运行加断点的程序：在代码区域右键Debug运行
4. 看窗口：Debugger窗口，看代码执行到哪里了。Variables窗口，看代码执行过程中变量的变化。看Console窗口，看程序执行过程中结果展示
5. 一步一步执行：按F7或点Step Into(F7)箭头
6. 结束：点stop结束

## 2.9.标准类的创建

1. 成员变量：使用private修饰
2. 构造方法：提供一个无参构造方法，提供多个不同的带参构造方法
3. 成员方法：a.提供每个成员变量对应的setXxx()/getXxx()；重写toString()方法；重写equals()方法；重写HashCode()方法
4. 测试类中创建对象并为其成员变量赋值的两种方法：a.无参构造方法创建对象后使用setXxx()赋值。b.使用带参构造方法直接创建带有属性的对象

## 2.10.面向对象基础

### 2.10.1.类与对象

- 对象是能够看得到摸得着的真实存在的实体
- 对象的属性：对象具有的各种特征，每个对象的每个属性都拥有特定的值
- 对象的行为：对象能执行的操作

#### 类

- 类是对现实生活中一类具有共同属性和行为的事务的抽象
- 类的特点：类是对象的数据类型，类是具有相同属性和行为的一组对象的集合
- 类由属性和行为组成
- 属性：在类中通过成员变量来体现（类中方法外的变量）
- 行为：在类中通过成员方法来体现（和之前的方法相比去掉static关键字即可）

#### 对象

- 创建对象：格式：类名 对象名 = new 类名()

- 使用对象

1. 使用成员变量：格式：对象名.变量名
2. 使用成员方法：格式：对象名.方法名()

#### 成员变量和局部变量

- 成员变量：类中方法外的变量，在内存中处于堆内存，有默认的初始化值
- 局部变量：方法中的变量，在内存中处于栈内存，没有默认的初始化值，必须先定义，赋值，才能使用

### 2.10.2.封装

#### 概述

- 是面向对象三大特征之一（封装、继承、多态），是面向对象编程语言对客观世界的模拟，客观世界里成员变量都是影响在对象内部的，外界无法操作

#### 原则

- 将类的某些信息隐藏在类内部，不允许外部直接访问，而是通过该类提供的方法来实现对隐藏信息的操作和访问成员变量private，提供对象的getXxx()/setXxx()方法

#### private关键字

- 是一个权限修饰符，可以修饰成员（成员变量和成员方法），作用是保护成员不被别的类使用，被private修饰的成员只在本类中才能访问
- 如果A类中被private修饰的成员变量在A类中public的方法中被使用，则在B类中不可以访问A类中被private修饰的成员变量，但可以访问A类中public的方法
- 如果想要访问A类中被private修饰的成员变量，则可以在A类中建立public修饰的set…/get…方法来设置和获取成员变量。这样的作用是，可以在A类中public修饰的set…/get…方法中对成员变量进行限定，例如年龄不能小于零等等
- 一个标准类的编写：把成员变量用private修饰，提供对应的set…/get…方法。

#### this关键字

1. this修饰的变量用于指代成员变量
   1. 注意方法的形参如果和成员变量同名，不带this修饰的变量指的是形参，而不是成员变量，方法的形参没有和成员变量同名，不带this修饰的变量指的是成员变量
2. 当成员变量和局部变量同名时，用this修饰的变量代表成员变量
3. this代表所在类的对象引用

#### 构造方法

作用是创建对象

- ```java
  public class 类名{
   修饰符 类名(参数){
  }
  }
  ```

- 功能：完成对象数据的初始化
- 无参数的构造方法就相当于在B类中重新定义A类中的成员变量的值
- 有参数的构造方法就相当于在B类中使用此方法时顺带将想要给A类参数赋的值赋值

#### 封装的注意事项

1. 构造方法的创建：如果没有定义构造方法，系统将给出一个默认的无参数构造方法，如果定义了构造方法，系统将不再提供默认的无参数构造方法
2. 构造方法的重载：如果定义了带参构造方法，还要使用无参数构造方法，就必须再写一个无参数构造方法
3. 无论是否使用无参数构造方法，都建议手工写一个无参数构造方法

### 2.10.3.继承

#### 概述

- 继承是面向对象三大特征之一，可以使得子类具有父类的属性和方法，还可以在子类中重新定义，追加属性和方法，共性的抽取，实现代码复用

#### 格式

- ```java
  public class 子类名 extends 父类名{
      
  }
  ```

- 父类也称基类、超类
- 子类也称派生类

#### 好处与弊端

- 好处

1. 提高了代码的复用性，多个类相同成员可以放到一个类中
2. 提高了代码的维护性，如果方法的代码需要修改，修改一处即可

- 弊端

1. 继承让类与类之间产生了关系，类的耦合性增强了，当父类发生了变化子类也必须跟着变，削弱了子类的独立性

#### 继承变量访问特点

- 通过子类访问一个变量

1. 在子类局部范围找
2. 在子类成员范围找
3. 在父类成员范围找
4. 如果都没找到则报错

#### 继承中构造方法访问特点

- 通过子类访问一个构造方法

1. 首先默认访问父类中的无参构造方法，然后再访问子类中的构造方法
2. 如果父类中没有无参构造方法，只有带参构造方法，
   1. 可以在子类的构造方法中加一个super()方法，来显示的去调用父类中的带参构造方法。
   2. 在父类中提供一个空内容的无参构造方法

#### 继承中成员方法的访问特点

- 通过子类访问一个成员方法

1. 先在子类成员方法中寻找
2. 然后在父类成员方法中寻找
3. 如果子类和父类有相同名称的成员方法，则访问的是子类中的成员方法，若想要访问父类中的成员方法，则可以在子类相同名称的成员方法中加上super()

#### super关键字

- 在子类方法中访问子类的成员变量、构造方法、成员方法，使用this.object，访问父类的成员变量、构造方法、成员方法，使用super.object

#### 继承的注意事项

1. java中类只支持单继承，不支持多继承
2. java中类支持多层继承
3. 继承中无论父类还是子类建议写无参和带参构造方法

### 2.10.4.多态

#### 概述

- 去完成某个行为，当不同对象去完成时会产生出不同的状态
- 多态的形式：具体类多态、抽象类多态、接口多态

- eg：猫
- ​         可以说猫是猫：猫 cat = new 猫()
- ​         可以说猫是动物：动物 animal = new 猫()
- ​         这里猫在不同的时刻表现出了不同的形态，这就是多态

#### 多态的前提与体现

1. 有继承/实现关系
2. 有方法重写
3. 有父(类/接口)引用指向子(类/接口)对象

#### 多态中成员访问特点

- 成员变量：编译看左边，执行看左边
- 成员方法：编译看左边，执行看右边

- eg
- Animal cat = new Cat()
- cat.object    若object在Animal中有并且在Cat中也有，则输出的是Animal中的值；若Animal中没有但在Cat中有，则无法输出
- cat.object()  若object在Animal中有并且在Cat中也有，则输出的是Animal中的方法，但如果在Cat中重写了此方法，则输出Cat中重写的此方法；若Animal中没有但在Cat中有，则无法输出

#### 多态的好处和弊端

- 好处：提高了程序的扩展性，在定义方法的时候，使用父类型作为参数，将来使用的时候，使用具体的子类型参与操作
- 弊端：不能使用子类的特有功能

#### 多态中的转型

- 向上转型：从子到父，父类引用指向子类对象
- 向下转型：从父到子，父类引用转为子类对象

- 格式

1. 先创建向上转型：父类 object = new 子类()，此时父类中没有的方法，虽然子类中有，但也无法使用
2. 在创建向下转型：子类 object1 = (子类)object，此时可以使用子类中有而父类中没有的方法了

### 2.10.5.抽象类 

#### 概述

- 一个没有方法体的方法应该定义为抽象方法，而类中如果有抽象方法，该类必须定义为抽象类

- ```java
  public abstract class 类名{
  	public abstract void 方法名();
  }
  ```

- 注意：抽象方法必须在抽象类里面定义，且抽象方法没有具体的方法体，即不需要写{…}

#### 抽象类特点

1. 抽象类不一定有抽象方法，但有抽象方法的类一定是抽象类
2. 抽象类不能直接创建对象，而是重写一个类继承抽象类，并且重写抽象类的抽象方法，然后和多态一样，利用新定义的类创建对象
3. 抽象类的子类在继承抽象类时，a.重写抽象类的所有抽象方法；b.将子类也定义为抽象类，此时则可以不重写抽象类的所有抽象方法

#### 抽象类成员特点

1. 抽象类可以有构造方法，但不能实例化，可以用于子类访问父类数据是初始化。
2. 成员变量可以是变量，也可以是final修饰的常量
3. 可以有抽象方法(限定子类必须完成某些动作 )，也可以有非抽象方法(提高代码的复用性)

### 2.10.6.接口

#### 概述

- 一种公共的规范标准，只要符合规范标准，就都可以使用，Java中的接口体现在对行为的抽象

#### 特点

1. 接口用关键字interface修饰，格式：public interface 接口名{}
2. 类实现接口用implements表示，格式：public class 类名 implements 接口名{}
3. 接口不能实例化，需参照多态的方法，通过实现类对象实例化，叫做接口多态
4. 接口的实现类，要么重写接口中的所有抽象方法；要么写成抽象类

#### 接口的成员特点

1. 成员变量：只能是常量，默认修饰符：public static final，可以直接写数据类型 object…
2. 构造方法：接口没有抽象方法；一个类若没有父类，默认继承Object类
3. 成员方法：只能是抽象方法，默认修饰符：public abstract；不能有具有具体方法体的方法，可以直接写void 方法名();

#### 类和接口的关系

1. 类和类的关系：继承关系，只能单继承，但可以多层继承
2. 类和接口的关系：实现关系，可以但实现，也可以多实现，还可以在继承一个类的同时实现多个接口
3. 接口和接口之间的关系：继承关系，可以单继承，也可以多继承

#### 抽象类和接口的关系

- 成员区别
- ​    抽象类：变量、常量、构造方法、抽象方法、非抽象方法
- ​    接口：常量、抽象方法

- 关系区别
- ​    类与类：继承、单继承
- ​    类与接口：实现、单实现、多实现
- ​    接口与接口：继承、单继承、多继承

- 设计理念区别
- ​    抽象类：对类抽象，包括属性、行为
- ​    接口：对行为抽象

#### 注意事项

1. 当一个类即继承了抽象类，又实现了接口类，则在实例化这个类时，只需要通过这个类实例化，即可实现使用抽象类方法和接口类抽象方法
2. 抽象类是对事物的抽象，接口是对行为的抽象，一般设计的时候，将事物固有的属性放到抽象类中，将事物有可能具有的行为放大接口中

## 2.11.字符串

### 2.11.1. String

- String类代表字符串，在java程序中所有双引号字符串，都是String类的对象。
- 特点：字符串不可改变，在创建后不能被修改，但可以被共享，字符串效果相当于字节数组(byte[])

#### 字符串的比较

- 使用 = = 比较：对于基本类型，比较的是数据值；对于引用类型，比较的是地址值。
- 字符串的比较使用的是equals()方法，object1.equals(object2),比较的是两个字符串是否相同
- 获取字符串指定索引处的char值：object.charAt(i)

### 2.11.2. StringBuilder

- StringBuilder是一个可变的字符串类，可以看做是一个容器，容器里面的内容可变。
- 与String的区别：String的内容不可变，StringBuilder的内容可以变

- ```java
  //构造方法
  
  StringBuilder Object = new StringBuilder() //无参构造
  
  StringBuilder Object = new StringBuilder(“字符串内容”) //带参构造
  
  //添加方法
  
  Object.append(“添加的内容”)   //可以连续链式添加，返回的是对象本身
  
  //反转内容
  
  Object.reverse()      //返回的是对象本身
  ```

### 2.11.3. String与StringBuilder的相互转换

- ```java
  String object = Object.toString()方法//StringBuilder转换为String
  
  StringBuilder Object = new StringBuilder(object)//String转换为StringBuilder
  ```

## 2.12.集合

- 结构
- 集合={Collection(单列)[List(可重复)---ArrayList、LinkedList；set(不可重复)---HashSet、TreeSet]；Map(双列)HashMap}
- 接口有Collection、Map、List、Set
- 实现类有：ArrayList、LinkedList、HashSet、TreeSet、HashMap

### 2.12.1.Collection

- 是单列集合的顶层接口，表示一组对象，这些对象也称为Collection的元素，由具体的子接口Set/List实现
- 创建Collection集合的对象：采用多态的方式；具体的实现类参照ArrayList

#### Collection常用方法

- ```java
  object.add(E e)//添加元素
  
  object.remove(Object o)//删除元素o
  
  object.clear()//清空集合中的元素
  
  object.contains(Object o)//判断集合中是否有指定元素
  
  object.isEmpty()//判断集合是否为空
  
  object.size()//集合长度
  ```

#### Collection集合的遍历

- ```java
  //Iterator 迭代器。集合专用遍历方式
  
  Collection<E> object = new ArrayList<E>();
  
  Iterator<E> it = object.iterator();//返回此集合中元素的迭代器，通过集合的iterator()方法得到，这里的E与集合设置中的E是一个类型
  
  //Iterator中常用的方法
  
  Object.next()//返回迭代中的下一个元素
  
  Object.hasNext()//如果迭代具有更多元素，则返回True
  ```

#### 集合使用步骤

```java
//创建集合对象  
Collection<E> object = new ArrayList/LinkedList/HashSet/TreeSet <E>();
//添加元素  
object.add(“元素”)
//遍历集合
//通过集合对象获取迭代器对象   
Iterator<E> it = object.iterator();
//判断是否还有元素
it.hasNext()
//若还有元素，获取下一个元素
it.next()
```

#### List

- 有序集合，可以精确的空值列别中的每个元素的插入位置，可以通过整数索引来访问元素，列表元素允许重复元素存在。
- 特点：存储和读取的元素顺序一致；存储的元素可重复

- ```java
  List<E> list = new ArrayList<E>();
  //遍历：方法1：
      Iterator it = list.iterator();it.hasNext();it.next()；方法2：for循环
  //添加：
          it.add(int index, Object)   //指定位置插入元素
  //删除：
          it.remove(int index)  //删除指定位置元素，并返回指定位置元素
  //修改元素：
          it.set(int index, Object)
  //获取元素：
          it.get(int index)
  ```

- 注意：当在遍历过程中遇到某个元素时需要添加某个元素时，只能用for循环，不可以用Iterator迭代器遍历。

##### ListIterator

- 列表迭代器
- 与Iterator的区别：ListIterator可以在列表中任意位置任意方向遍历，Iterator只能从头到尾遍历；利用Iterator迭代器遍历不可以添加元素，但ListIterator迭代器遍历可以添加元素。

常用方法

- ```java
  List<E> list = new List<E>()
  list.hasNext(); //判断下一个位置知否存在元素
  list.hasPrevious();  //判断上一个位置知否存在元素
  list. next();       //得到下一个位置的元素
  list. previous();    //得到上个位置的元素
  list.add(object);   //在遍历时可以插入指定元素
  ```

##### 增强for循环

简化数组和Collection集合的遍历

- ```java
  for(元素数据类型 变量名:数组或者Collection集合){
  	 //在此处使用变量即可，该变量就是元素
  }
  ```

##### List集合子类特点

- List集合常用的子类：ArrayList、LinkedList
- ArrayList：底层数据结构是数组，特点查询快，增删慢
- LinkedList：底层数据结构是链表，特点增删快，查询慢.

##### 建立List时子类的选择

- 如果需要查询快，则使用ArrayList，如果需要增删快，则使用LinkedList

##### ArrayList

- ```java
  //ArrayList构造方法：
  ArrayList<引用类型> object = new ArrayList<>()
  
  //ArrayList添加方法：
  //添加到目标对象末尾:
      object.add(添加的内容)//返回本身，在输出中返回true or false
  //添加到目标对象任意位置:
      object.add(index, 添加的内容)//返回本身，在输出中返回true or false
  
  //ArrayList删除元素：
  //删除目标对象指定元素:
      object.remove(x)//返回本身，在输出中返回true or false
  //删除指定索引处的元素:
      object.remove(index)//返回本身，在输出中返回被删除的元素
  
  //ArrayList修改元素：
  //修改指定索引处的元素:
      object.set(index,修改的内容)//返回本身，在输出中返回被修改的元素
      
  //ArrayList返回元素：
  //返回指定索引处的元素:
      object.get(index)//在输出中返回指定索引处的元素
  //返回集合中元素的个数:
      object.size()//在输出中返回集合元素个数
  ```

##### LinkedList

- ```java
  //LinkedList构造方法：
  LinkedList<引用类型> object = new LinkedList<>()
  
  //LinkedList添加方法：
  //添加到目标对象开头:
      object.addFirst(添加的内容) //在输出中返回true or false
  //添加到目标对象末尾:
      object.addLast(index, 添加的内容) //在输出中返回true or false
  
  //LinkedList获取元素：
  //获取目标对象第一个元素:
      object.getFirst()//返回本身，在输出中返回列表中第一个元素
  //获取目标对象最后一个元素:
      object.getLast()//返回本身，在输出中返回列表中最后一个元素
  
  //LinkedList删除元素：
  //删除目标对象第一个元素:
      object.removeFirst()//返回本身，在输出中返回第一个元素
  //删除目标对象最后一个元素:
      object.removeLast ()//返回本身，在输出中返回最后一个元素
  ```

#### Set

- 有序集合
- 特点：不包含重复元素；没有带索引的方法，所有不能使用普通的for循环遍历

##### HashSet

- 集合里的元素顺序不一定与输入元素顺序保持一致

- ```java
  Set<E> set = new HashSet<E>();
  ```

- 注意：利用HashSet存储对象时，要在类中重写hashCode()和equals()，自动生成即可

##### 哈希值

- 是JDK根据对象的地址或者字符串或者数字算出来的int类型的数值

- ```java
  public int hashCode()：返回对象的哈希值；object.hashCode()//Object类中获取对象哈希值的方法：
  ```

- 注意：object可以是类对象，也可以是具体数据对象。同一个对象多次调用哈希值返回的值是一样的；默认情况下不同对象返回的哈希值是不一样的，当重写hashCode方法时，返回的哈希值是可以相同的。

##### 哈希表

- jdk8之前，底层用数组+链表实现，可以说是一个元素为链表的数组

- 哈希表默认大小为16的数组，即0-15的数组，然后对存储数据获取哈希值，用此哈希值对16取余，获得的值即为存储在哈希表数组的地址，哈希值不同，取余相同的采取链表存储，哈希值相同，取余相同的咋不采取任何操作

##### LinkedHashSet

- 特点：由哈希表和链表组成的Set接口，其中哈希表保证集合元素唯一，链表保证元素存储和去除顺序一致

##### TreeSet

1. 元素有序，但取出顺序和存储顺序不一定相同，具体集合的排序方法：
   1. TreeSet()方法，根据元素的自然排序进行排序
   2. TreeSet(Comparator comparator)方法，根据指定的标胶器进行排序
2. 没有带索引的方法，不能使用for循环遍历，可以使用Iterator迭代器和增强for循环遍历
3. 集合元素不能重复

##### 自然排序Comparable的使用

- 使用的是TreeSet的无参构造方法，格式

- ```java
  TreeSet<E> ts = new TreeSet<E>();
  ```

- 在TreeSet集合中插入元素，想要按元素的某一个属性排序，则需要在类中实现Comparable<E>接口，然后重写comparableT o(E o)方法，其中o.属性表示现有的TreeSet集合中的所有元素，this.属性表示插入的元素，返回两者相减的值，若值大于0则按自然排序插入，若值等于0，则不插入，若值小于0，则按自然排序相反的顺序插入。注意：也可以同时比较多个属性。

##### 比较器Comparator的使用

- ```java
  //使用的是TreeSet的带参构造方法，格式   
  TreeSet<Student> ts = new TreeSet<>(new Comparator<Student>() {
  	@Override
  	public int compare(E o1, E o2) {
  	return 0;
  	}
  });
  ```

- 修改方法体中返回值的内容即可，注意o1表示想要插入的元素，o2表示当前TreeSet中所有的元素，想要插入的元素属性比TreeSet集合中的元素属性大，则按从小到大插入，相反…

### 2.12.2.泛型

- 本质是参数化类型，将类型由原来的具体的类型参数化，然后在使用/调用时传入具体的类型，可以用于类、方法和接口中，称为泛型类、泛型方法、泛型接口

#### 格式

- ```java
  <类型>//指定一种类型的格式，这里的类型可以看成是形参
  
  <类型1,类型2…>//指定多种类型的格式，多种类型之间用逗号隔开，这里的类型可以看成形参
  
  //将来具体调用时候给定的类型可以看成是实参，并且实参的类型只能是引用类型
  ```

#### 优势

- 把运行时期的问题提前到了编译期间
- 避免了强制类型转换

#### 泛型类

##### 定义格式

- ```java
  修饰符 class 类名<类型>{ 
  	
  	}   //常见的类型(T、E、K、V)等形式的参数常用与表示泛型，在创建对象的时候，再给一个具体的类型即可
  ```

#### 泛型方法

##### 格式

- ```java
  修饰符 <类型> 返回值类型 方法名(类型 变量名){
  
  	}
  ```

#### 泛型接口

##### 格式

- ```java
  修饰符 interface 接口名 <类型>{
  	}
  ```

#### 类型通配符

为了表示各种泛型List的父类，可以使用类型通配符

1. 类型通配符：<?>
   1. List<?>表示元素类型未知的List，它的元素可以匹配任何类型
   2. 这中带通配符的list仅表示他是各种泛型List的父类，并不能将元素添加到其中
2. 类型通配符上限：<? extend 类型>
   1. List<? extend Number>：表示的类型是Number或者其子类型
3. 类型通配符下限：<? super 类型>
   1. List<? superNumber>：表示了类型是Number或者其父类型

#### 可变参数

- 可变参数即参数个数可变，用作方法的形参出现

##### 格式

- ```java
  修饰符 返回值类型 方法名(数据类型 变量名a,数据类型… 变量名b){
  	
  }
  ```

- 注意一般在调用时，在可变参数前的参数是不可变参数，可以有多个，而可变参数b是存储在一个数组中

##### 可变参数的使用

- Arrays中的一个静态方法：

- ```java
  public static <T> List <T> asList(T..a)//返回由指定数组支持的固定大小的列表
  ```

- 注意：返回的集合不能做增删操作，但可以做修改操作

- List接口中有一个静态方法：

- ```java
  public static <T> List <T> of(E..elements)//返回包含任意数量元素的不可变列表
  ```

- 注意：返回的集合不能做增删改操作

- Set接口中有一个静态方法：

- ```java
  public static <T> Set<T> of(E..elements)//返回一个包含任意数量元素的不可变集合
  ```

- 注意：给的元素不能重复，返回的集合不能做增删操作，没有修改操作

### 2.12.3. Map

#### 概述

- Interface Map<K, V>   K：键的类型；V：值的类型
- 将键映射到值的对象，不能包含重复元素，每个键都可以映射到最多一个值
- 创建Map对象：使用多态的形式，具体的实现类HashMap

#### 操作

- ```java
  Map<数据类型，数据类型> Obejct = newHashMap<数据类型，数据类型> ()//一般这里的MAP有HashMap(对键没有排序功能)、TreeMap(对键有自然排序的功能)
  
  //添加：
      Object.put(键;值)//注意当一个键被重复使用是，即为修改的意思，结果为最后修改的值
  
  //根据键获取值：
      Object.get(键)
  //获取所有键的集合：
      Set<数据类型> object = Obejct.keySet()
  //获取所有值的集合：
      Collection<数据类型> object = map.values();
  //获取所有键值对对象的集合：
       Set<Map.Entry<数据类型, 数据类型>> object = Obejct.entrySet();
  
  //删除：
  Object.remove(键)
  //清除所有键值对元素：
      Object.clear
      
  //判断集合是否包含指定的键：
      Object.containsKey(Object key)
  //判断集合是否包含指定的值：
      Object.containsValue(Object Value)
  //判断集合是否为空：
       Object.isEmpty()
      
  //集合的长度：
        Object.size()
  ```

#### 遍历

##### 方式一

1. 获取所有键的集合，用keySet()方法
2. 遍历键的集合，获取每一个键，用增强for循环
3. 根据键得到值，使用gei(object key)方法

##### 方式二

1. 获取所有键值对的集合，用Set<Map.Entry<K,V>> entrySet()
2. 遍历键值对对象的集合，得到每一个键值对对象，用增强for实现，得到每一个Map.entry，for里面的数据类型即为<>中的数据类型
3. 根据键值对对象获取键和值：getKey()、getValue()

### 2.12.4. Collections

#### 概述

- 针对集合操作的工具类

#### 常用方法

```java
public static <T extends Comparable<? super T>> void sort(List<T> list)//将指定的列表按升序排序；Collections.sort(object)，返回对象本身

public static void reverse(List<?> list)//反转指定列表中元素的顺序；Collections. reverse (object) ，返回对象本身

public static void shuffle(List<?> list)//使用默认的随机源随机排序指定的列表；Collections. shuffle (object) ，返回对象本身
```

## 2.13.修饰符

### 2.13.1.权限修饰符

- private、默认、protected、public

- |  修饰符   | 同一个类中 | 同一个包中子类无关类 | 不同包的子类 | 不同包的无关类 |
  | :-------: | :--------: | :------------------: | :----------: | :------------: |
  |  private  |    true    |        false         |    false     |     false      |
  |   默认    |    true    |         true         |    false     |     false      |
  | protected |    true    |         true         |     true     |     false      |
  |  public   |    true    |         true         |     true     |      true      |

### 2.13.2.状态修饰符

- final(最终态)、static(静态)

#### final

- 可以修饰成员方法、成员变量、类

- 特点

1. 修饰方法：表明该方法是最终方法，不能被重写
2. 修饰变量：表明该变量是常量，不能再次被赋值
3. 修饰类：表明该类是最终类，不能被继承
4. 修饰局部变量是基本类型：数据值不能发生改变
5. \修饰局部变量是引用类型：地址值不能发生改变，但地址里面的内容是可以发生改变的

#### static

- 可以修饰成员方法、成员变量

- 特点

1. 被类的所有对象共享
2. 可以通过类名调用，一般对static修饰的变量赋值时，直接使用类名.object赋值，而不是创建对象，然后对象.object赋值。
3. 非静态成员方法能访问静态的成员变量、静态的成员方法、非静态的成员变量、非静态的成员方法
4. 静态成员方法能访问静态成员变量、静态成员方法

## 2.14.形参和返回值

### 2.14.1.类名作为形参和返回值

- 方法的形参是类型，则需要该类的对象
- 方法的返回值的类名，则需要返回该类的对象

### 2.14.2.抽象类名作为形参和返回值

- 方法的形参是抽象类名，则需要该抽象类的子类对象
- 方法的返回值是抽象类名，则需要返回的是抽象类的子类对象

### 2.14.3.接口名作为形参和返回值

- 方法的形参是接口名，则需要该接口的实现类对象
- 方法的返回值是接口名，则需要返回的是该接口的实现类对象

## 2.15.内部类

### 2.15.1.概述

- 在一个类中定义一个类，即在A类中定义一个B类，则B类为内部类

- ```java
  public class 类名A{
  	修饰符 class 类名B{
  	}
  }
  ```

- 分类
- 在类的成员位置：成员内部类
- 在类的局部位置(在类的方法里面定义)：局部内部类

### 2.15.2.内部类的访问特点

- 内部类可以直接方法外部类的成员，包括私有
- 外部类想要访问内部类的成员，必须创建对象

### 2.15.3.成员内部类

- 外界创建成员内部类的对象格式

1. 当内部类的修饰符为public：外部类名.内部类名 对象名 = new 外部类名.new 内部类名
2. 内部类的修饰符为private：可以在外部类里面定义一个method方法，在method方法里面创建private类的对象，然后调用private类里面的方法，最后在外界直接创建外部类的object，利用object.method即可。

### 2.15.4.局部内部类

- 局部内部类实在方法中定义的类，外界无法直接使用，需要在方法内部创建对象并使用，该类可以直接访问外部类的成员，也可以访问方法内部的局部变量

### 2.15.5.匿名内部类

- 前提：存在一个类或者接口，类可以使具体类也可以是抽象类
- 本质是一个继承了该类或者实现了该接口的子类匿名对象

- ```java
  new 类名或者接口名{
  	重写方法
  }.重写的方法名;
  //或者
  类名或者接口名 object = new new 类名或者接口名{
  	 重写方法
  };
  object.重写的方法名;
  ```

## 2.16.常用API

### 2.16.1. Math

- Math的常用方法，直接调用

|                    方法名                    |                      说明                      |
| :------------------------------------------: | :--------------------------------------------: |
|         public static int abs(int a)         |                返回参数的绝对值                |
|     public static double ceil(double a)      | 返回大于或等于参数的最小double值，等于一个整数 |
|     public static doublefloor(double a)      | 返回小于或等于参数的最小double值，等于一个整数 |
|       public static int round(float a)       |        返回四舍五入后最接近参数的int值         |
|     public static int max(int a, int b)      |            返回两个int值中的较大值             |
|     public static int min(int a, int b)      |            返回两个int值中的较小值             |
| public static double pow(double a, double b) |                返回a的b次幂的值                |
|        public static double random()         |            返回值为double类型的正值            |

- eg：-88的绝对值：Math.abs(-88)

### 2.16.2. System

- System的常用方法，不能被实例化，只能使用类名进行访问

- ```java
  System.exit(0)//在此代码后的所有代码都不运行
  
  System.currentTimeMillis()//输出表示当前时间与1970年1月1日之间的时间差异，以毫秒为单位
  
  //注意：
  
  //    计算一段代码的运行时间
  long start_time = System.currentTimeMillis();
  for (int i = 0; i < 10000; i++) {
  	System.out.println(i);
  }
  long end_time = System.currentTimeMillis();
  System.out.println("共耗时：" + (end_time - start_time) + "毫秒");
  ```

|                 方法名                 |                    说明                    |
| :------------------------------------: | :----------------------------------------: |
|  public static void exit(int status)   | 终止当前运行的java虚拟机，非零表示异常终止 |
| public static long currentTimeMillis() |         返回当前时间(以毫秒为单位)         |

### 2.16.3. Object

-  每个类都将Object作为超类

- ```java
  object. toString()//返回对象的字符串表示形式，一般在类中重写一下tostring方法，和get/set方法一样
  equals()方法//object1.equals(object2) 比较两个对象内容是否相同，一般在类中重写一下equals方法，和get/set方法一样
  ```

|              方法名               |                           说明                           |
| :-------------------------------: | :------------------------------------------------------: |
|     public String toString()      | 返回对象的字符串表示形式，建议所有子类自动生成重写该方法 |
| public boolean equals(Object obj) | 比较对象是否相等，默认比较地址，自动生成重写可以比较内容 |

### 2.16.4. Arrays

- 用于操作数组的各种方法

- ```java
  Arrays.sort(Object)//默认从小到大排序，返回对象本身
  ```

|                说明                |                 方法名                 |
| :--------------------------------: | :------------------------------------: |
| 返回指定数组的内容的字符串表示形式 | public static String toString(int[] a) |
|     按照数字顺序排序指定的指数     |    public static void sort(int[] a)    |

### 2.16.5.基本类型包装类

-  将基本数据类型封装成对象的好处在于可以在对象中定义更多的功能操作该数据
- 常用的操作之一：用于基本数据类型与字符串之间的转换

| 基本数据类型 |  包装类   |
| :----------: | :-------: |
|     byte     |   Byte    |
|    short     |   Short   |
|     int      |  Integer  |
|     long     |   Long    |
|    float     |   Float   |
|    double    |  Double   |
|     char     | Character |
|   boolean    |  Boolean  |

- ```java
  public static final int MIN_VALUE//持有最小值的常数为 `int`可以为-2 31 。
  
  public static final int MAX_VALUE//持有最大值的常数为 `int`可以为2 31 -1。
  ```

#### Integer类

- 包装一个对象中的原始类型int的值

|                 方法名                  |                 说明                  |
| :-------------------------------------: | :-----------------------------------: |
|        public Integer(int value)        |       根据int值创建Integer对象        |
|        public Integer(String s)         |      根据String值创建integer对象      |
|  public static Integer valueOf(int i)   |   返回表示指定的int值的Integer实例    |
| public static Integer valueOf(String s) | 返回一个保存指定值的Integer对象String |

#### int和String的相互转换

- ```java
  //int 转换为 String ：
  public static String ValueOf(int i )//返回int参数的字符串表示形式，该方法是String类中的方法，直接String.valueOf(object)调用
  
  //String 转换为int ：
  public static String parseInt(String s )//将字符串解析为int类型，该方法是Integer类中的方法直接Integer.valueOf(object)调用
  ```

#### 自动装箱和拆箱

- 装箱：把基本数据类型转换为对象的包装类类型
- 拆箱：把包装类类型转换为对应的基本数据类型

- ```java
  //eg：
  Integer i = 100;   //自动装箱
  i += 100;    //i = i + 100 : i + 100是自动拆箱；i = i +100是自动装箱 
  ```

- 注意：在使用包装类型的时候，如果做操作，最好先判断是否为null，只要是对象，在使用前就必须进行不为null的判断。

### 2.16.6.日期类

#### Date类

- 代表了一个特定的时间，精确到毫秒

|         方法名         |                             说明                             |
| :--------------------: | :----------------------------------------------------------: |
|     public Date()      |  分配一个Date对象，并初始化，代表它被分配的时间，精确到毫秒  |
| public Date(long date) | 分配一个Date对象，并将其初始化为表示从标准基准时间起指定的毫秒数 |

#### Dtae常用方法

|             方法名             |                         说明                         |
| :----------------------------: | :--------------------------------------------------: |
|     public long getTime()      | 获取的是日期对象从1970年1月1日00:00:00到现在的毫秒值 |
| public void setTime(long time) |                设置时间，给的是毫秒值                |

#### SimpleDateFormat类

- 一个具体的类，用于以区域设置敏感的方式格式化和解析日期

- 常用的模式字母及对应关系如下：
- y：年、M：月、d：日、H：时、m：分、s：秒
- 注意大写的M表示月，小写的m表示分

- ```java
  //格式化(从Date到String)：
  public final String format(Date date)//将日期格式化成日期/时间字符串
  
  //格式：
  SimpleDateFormat sdf1 = new SimpleDateFormat();
  
  //无参构造方法输出的结果2022/6/7 下午1:44
  SimpleDateFormat sdf2 = new SimpleDateFormat("yyyy年MM月dd日 hh:mm:ss");
  
  //带参构造方法给出的是自己设定的格式，输出的结果2022年06月07日 01:51:42
  String object = sdfx. format(Date date);
  
  //解析(从String到Date)：
  public Date parse(String cource)//从给定字符串的开始解析文本以生产日期
  
  //格式：
  String d6s = "1998-9-11 00:00:00";
  
  //字符串的格式要和impleDateFormat对象设置的格式一样
  SimpleDateFormat sdf3 = new SimpleDateFormat("yyyy-MM-dd hh:mm:ss");
  Date d6 = sdf3.parse(d6s);
  System.out.println(d6);
  ```



#### Calendar类

- 为某一时刻和一组日历字段之间的转换提供了一些方法，并为操作日历字段提供了一些方法。

- ```java
  //常用方法1：get方法获取当前日历字段中的YEAR…
  Calendar c= Calendar.getInstance();
  
  //用于获取Calendar对象，其日历字段已使用当前日期和时间初始化
  int Year = c.get(Calendar.YEAR);
  int Month = c.get(Calendar.MONTH) + 1;//月份从0开始 所以要+1
  int Day = c.get(Calendar.DATE);
  System.out.println(Year + "年" + Month + "月" + Day + "日");
  ```

- ```java
  //常用方法2：add方法对当前时间的YEAR…进行增加或减少修改
  
  c.add(Calendar.YEAR, -3);//当前时间的3年前
  
  System.out.println(c.get(Calendar.YEAR));
  ```

- ```java
  //常用方法3：set方法：直接设置具体日期
  
  c.set(2022,3,11);
  ```

- 注意：
- 获取某年某月有多少天：

1. 键盘得到年份月份
2. c.set方法设置年份，月份，day=1
3. c.add方法date-1即可获得输出

## 2.17.异常

### 2.17.1.体系

- ```java
  Throwable{Error，Execption[RuntimeException，非RuntimeException]}
  
  //Error：严重问题，不需要处理
  
  //Exception：称为异常，表示程序本身可以处理的问题
  
  //RuntimeException：在编译时不检查，出现问题后需要修改问题
  
  //非RuntimeException：编译期间就必须处理，否则程序不能通过编译，即不能运行
  ```

### 2.17.2. JVM的默认处理方案

- 当程序出现问题，JVM默认处理方案为：输出出现问题的原因、行号并且终止程序继续向下运行

### 2.17.3.异常处理

- 两种方案

1. try…catch…
2. throws

#### try…catch…

- ```java
  try{
  	出现异常的代码
  }catch (异常类名 e){       //异常类名 即 程序报错是的类名
  	出现异常的处理代码
  }
  
  //执行流程：程序在try里面的代码开始执行，出现异常，会自动生成一个异常类对象，该异常对象将被提交给java运行时系统，当java运行时系统接收到异常时，会到catch中找匹配的异常类，找到后进行异常的处理，执行完毕之后，程序还可以继续往下执行
  
  e. printStackTrace()//输出异常具体信息
  System.out.println(e.getMessage());//输出异常的原因
  System.out.println(e.toString());//输出异常的简洁信息
  ```



#### throws

- ```java
   throws 异常类名;
  ```

- 注意：这个格式是跟在方法的括号后面的

#### 编译时异常和运行时异常的区别

- 运行时异常：在运行前不显示异常，但运行时会出错，可以先运行，然后再异常处理
- 编译时异常：在运行前就显示异常，必须进行异常处理

#### 自定义异常

- ```java
  public class 异常类名 extends Exception{
  	无参构造
  	带参构造
  }
  ```

#### throw和throws的区别

- throws：用在方法声明后面，跟的是异常类名；表示抛出异常，有该方法的调用者来处理，表示出异常的一种可能性，并不一定会发生这些异常
- throw：用在方法体内，跟的是异常对象名，表示抛出异常，有方法体内的语句处理，执行throw一定抛出了某种异常

## 2.18. IO流

### IO流概述

- 流：是一种抽象概念，是对数据传输的总称，也就是说数据在设备间的传输称为流，流的本质是数据传输
- IO流就是用来处理设备间数据传输问题的
- 常见的应用：文件复制、文件上传、文件下载

### 分类

1. 按照数据的流向：
   1. 输入流：读数据
   2. 输出流：写数据
2. 按照数据类型分：
   1. 字节流：字节输入流、字节输出流
   2. 字符流：字符输入流、字符输出流

- 一般来说，IO流的分类是按照数据类型来分的

- 注意：如果数据通过windows自带的记事本打开，并且可以读懂里面的内容，则使用字符流；若读不懂里面的内容，则使用字节流

### 2.18.1. File

#### 概述

- File是文件和目录路径名的抽象表示，文件和目录通过File封装成对象，对于File而言，封装的不是一个真正存在的文件，仅仅是一个路径名，他可以存在，也可以不存在，将来是要通过具体的操作把这个路径的内容转换为具体存在的

#### 构造方法

- ```java
  File(String pathname)//通过将给定的路径名字符串转换成抽象路径名来创建新的File实例
  File(String parent, String child)//通过父路径名字符串和子路径名字符串创建新的File实例
  File(File parent, String child)//通过父抽象路径名和子路径名字符串创建新的File实例
  ```

#### 创建功能

- ```java
  File object = new File(“路径名”)
  public boolean createNewFile(object)//当具有该名称的文件不存在时，创建一个由该抽象路径命名的新空文件
  public boolean mkdir(object)//创建由次抽象路径名命名的目录
  public boolean mkdirs(object)//创建由此抽象路径名命名的目录，包括创建必需但不存在的父目录
  ```

- 注意：创建路径文件就是文件，目录就是目录，不能混淆

#### File类判断和获取功能

- ```java
  public boolean isDirectory()//测试此抽象路径名表示的File是否为目录
  public boolean isFile()//测试此抽象路径名表示的File是否为文件
  public boolean exists()//测试此抽象路径名表示的File是否存在
  ```

注意：以上三个是要在绝对路径下boolean

- ```java
  public String getAbsolutePath()//返回此抽象路径名的绝对路径名字符串，即绝对路径
  public String getPath()//将此抽象路径名转换为路径名字符串，即相对路径
  public String getName()//返回由此抽象路径名表示的文件或目录的名称
  public String[] list()//返回由此抽象路径名表示的目录中的文件和目录的名称字符串数组
  public File[] listFiles()//返回由此抽象路径名表示的文件或目录的File对象数组
  ```

#### File类删除功能

- ```java
  public boolean delete()//删除由次抽象路径名表示的文件或目录
  ```

- 注意：如果目录中有内容(目录、文件)，则应该删除目录中的内容后才能再删除该目录

#### 递归

- 方法定义中调用方法本身，需要有递归出口

### 2.18.2.字节流

#### 写数据

- ```java
  //字节流抽象基类：
  InputStream//这个抽象类表示字节输入流的所有类的超类
  OutputStream//这个抽象类表示字节输出流的所有类的超类
  ```



- ```java
  //子类名特点：子类名称都是以父类名作为子类名的后缀
  FileOutputStream//文件输出流用于将数据写入文件
  FileOutputStream object = new FileOutputStream(“绝对路径”);//创建文件输出流以指定的名称写入文件
  ```

写入字节数据：

- ```java
  object.write(int b)
  object.write(byte[] b)：写入字节数组
  object.write(byte[] b, int off, int len)//将len字节从指定的字节数组开始，从偏移量off开始写入词文件输出流，一次写一个字节数组的部分数据
      
  //注意‘A’ 对应65 A-Z是连续的，‘a’ 对应97 a-z是连续的，‘0’ 对应45 0-9是连续的
  //也可以用
  byte[] b = "内容".getBytes(); 
  object.write(b,off,len);//注意：off是内容中的索引，len是添加的内容的长度
  object.close()//释放资源，写完内容后，必须需要填上
  ```

#### 字节流写数据的两个小问题

1. 写数据实现换行

   - ```java
     //在每次写完一次数据后，添加上
         object.write("x".getBytes());
     //这里的x在windows系统下用\r\n；linux系统用\n；mac系统下用\r
     ```

2. 写数据实现追加写入

   - ```java
     FileOutputStream fos = new FileOutputStream("绝对路径",true);//即可实现追加写数据
     ```

#### 字节流写数据加异常处理

- 使用try catch自行抛出异常
- finally：在异常处理时提供finally块来执行所有清除操作，比如IO流中的释放资源。特点：被finally控制的语句一定被执行，除非jvm退出

- ```java
  try{
  	可能出现异常的代码
  }catch(异常类名 变量名){
  	异常处理代码
  }finally{
  	执行所有清除操作
  }
  ```

- eg

- ```java
  FileOutputStream fos = null;
      try {
        fos = new FileOutputStream("绝对路径名",true);
        fos.write("内容".getBytes());
      }catch (IOException io){
        io.printStackTrace();
      }finally {
        if (fos != null) {
          try {
            fos.close();
          } catch (IOException e) {
            throw new RuntimeException(e);
          }
       }
      }
  ```

#### 字节流读数据（一次读一个字节数据）

- ```java
  FileInputStream(String name)//通过打开与实际文件的连接来创建一个FileInputStream，该文件由文件系统中的路径名name命名
  ```

- 步骤：

1. 创建字节输入流对象
2. 调用字节输入流对象的读数据方法
3. 释放资源

- 注意：使用强制转换，得到想要的输出

#### 字节流读数据（一次读一个字节数组数据）

-  步骤

1. 创建字节输入流对象
2. 创建字节数组，大小一般可以写为1024
3. 调用字节输入流对象的读数据方法
4. 释放资源

- 注意：使用强制转换，得到想要的输出

#### 字节缓冲流

- ```java
  BufferOutputStream//该类实现缓冲输出流，通过设置这样的输出流，应用程序可以向底层输出流写入字节，而不必为写入的每个字节导致底层系统的调用
  BufferInputStream//创建BufferInputStream将创建一个内部缓冲区数组，当从流中读取或跳过字节时，内部缓冲区将根据需要从所包含的输入流中重新填充，一次很多字节
  ```

构造方法：

- ```java
  BufferOutputStream(OutputStream out)
  BufferInputStream(InputStream in)
  ```

- 注意：构造方法需要的是字节流，而不是具体文件或路径，因为字节缓冲流仅仅提供缓冲区，真正的读写数据还得依靠基本的字节流对象进行操作

### 2.18.3.字符流

- 一个汉字的存储：如果是UTF-8编码存储，则占用3个字节；如果用GBK编码存储，则占用2个字节。
- 字符流= 字节流+编码表
- 用字节流复制文本时，文本文件中也会中文，但没有问题，是因为最终底层操作会自动进行字节拼接成中文，在汉字存储时，无论选择哪个编码存储，第一个字节都是负数

#### 字符串中的编码解码问题

- 编码

- ```java
  byte[] getBytes()//使用平台的默认字符集将改String编码为一系列字节，将结果存储到新的字节数组中
  byte[] getBytes(String charsetName)//使用指定的字符集将改String编码为一系列字节，将结果存储到新的字节数组中
  ```

- 解码

- ```java
  String(byte[] bytes)//通过使用平台的默认字符集解码指定的字节数组来构造新的String
  String(byte[] bytes,String charsetName)//通过指定的字符集解码指定的字节数组来构造新的String
  ```

- eg:

- ```java
  String s = "中国";
  
  //    编码
  byte[] bytes1 = s.getBytes();//这里设置的默认编码为GBK
  System.out.println(Arrays.toString(bytes1));//[-42, -48, -71, -6]
  byte[] bytes2 = s.getBytes("Utf-8");//设置UTF-8编码
  System.out.println(Arrays.toString(bytes2));//[-28, -72, -83, -27, -101, -67]
  
  //    解码
  String ss = new String(bytes1);//使用平台默认GBK解码GBK
  System.out.println(ss);
  String sss = new String(bytes1, "UTF-8");//使用UTF-8解码GBK
  System.out.println(sss);
  String ssss = new String(bytes2);//使用平台默认GBK解码UTF-8
  System.out.println(ssss);
  String sssss = new String(bytes2, "UTF-8");//使用UTF-8解码UTF-8
  System.out.println(sssss);
  ```

#### 字符流中的编码解码问题

- 字符流抽象基类

- ```java
  Reader//字符输入流的抽象类
  Writer//字符输出留的抽象类
  ```

字符流中编码解码相关的两个类

- ```java
  InputStreamReader(InputStream in)//创建一个使用默认字符集的InputStreamReader
  InputStreamReader(InputStream in, String charsetName)//创建一个使用命名字符集的InputStreamReader
  OutputStreamWriter(OutputStream out)//创建一个使用默认字符编码的OutputStreamWriter
  OutputStreamWriter(OutputStream out, String charsetName)//创建一个使用命名字符集的OutputStreamWriter
  ```

#### 字符流写数据的5种方式

- ```java
  void write(int c)//写一个字符
  
  void write(char[] cbuf)//写一个字符数组
  
  void write(char[] cbuuf, int off, int len)//写字符数组的一部分
  
  void write(String str)//写一个字符串
  
  void write(String str, int off, int len)//写一个字符串的一部分
  ```

#### 字符流读数据的2种方式

- ```java
  int read()：一次读一个字符数据
  
  int read(char[] cbuf)：一次读一个字符数组
  ```

#### 注意

- FileReader 相当于 InputStreamReader
- FileWrite 相当于 OutputStreamWriter

#### 字符缓冲流

- BufferedWriter：将文本写入字符输出流，缓冲字符，以提供单个字符、数组和字符串的高效写入，可以指定缓冲区大小，或者可以接收默认大小。
- BufferedReader：从字符输入流读取文本，缓冲字符，以提供字符、数组和字符串的高效写入，可以指定缓冲区大小，或者可以接收默认大小。

构造方法：

- ```java
  BufferedWriter(Writer out)
  BufferedReader(Reader in)
  ```

#### 字符缓冲流特有功能

- ```java
  //BufferedWriter：
  
  void newline()//写一行行分隔符，行分隔符字符串由系统属性定义
  
  //BufferedReader：
  
  public String readLine()//读一行文字，结果包含行的内容的字符串，不包括任何行终止字符，如果流的结尾已经到达，则为null
  ```

### 2.18.4.特殊操作流

#### 标准输入输出流

- ```java
  public static final InputStrem in//标准输入流，通常该流对应于键盘输入或由主机环境或用户指定的另一个输入源
  public static final OutputStrem out//标准输出流，通常该流对应于键盘输出或由主机环境或用户指定的另一个输出源
  ```

##### 标准输入流

- ```java
  //自己实现键盘录入数据：
  BufferedReader Object = new BufferedReader(new InputStreamReader(System.in));
  
  //java提供的一个类实现键盘录入数据：
  Scanner sc = new Scanner(System.in)
  
  //注意一般汉字的输入输出，使用的是字符流，因此需要把字节流转换为字符流
  BufferedReader Object = new BufferedReader(new InputStreamReader(System.in));
  //因为输入得到的是一个字符串，则如果需要得到别的类型的输出，则需要进行包装类
  ```

##### 标准输出流

- ```java
  PrintStream ps = System.out
  ```

#### 打印流

- 字节打印流：PrintStream
- 字符打印流：PrintWiter
- 特点：只负责输出数据，不负责读取数据；有自己特有的方法

##### 字节打印流

- ```java
  PrintStream(String fileName)//使用指定的文件名创建新的打印流
  //自己特有的方法：
  PrintStream ps =new PrintStream("文件地址");
  ps.print(内容);
  //使用自己特有的方法写数据，在查看数据时原样输出
  ```

##### 字符打印流

- ```java
  PrintWriter(String fileName) //使用指定的文件名创建一个新的PrintWriter，而不需要自动执行行刷新。
  public PrintWriter(OutputStream out, boolean autoFlush)//从现有的OutputStream创建一个新的PrintWriter
      //out：输出流，autoFlush：一个布尔值，如果为真，则println，printf或format方法将刷新输出缓冲区
  ```

#### 对象序列化流与对象反序列化流

- 将对象保存到磁盘中，或者在网络中传输对象
- 机制就是使用一个字节序列表示一个对象，该字节序列包含：对象的类型，对象的数据和对象中存储的属性等信息，字节序列写到文件后，相当于文件中持久保存了一个对象的信息，反之，改序列还可以从文件中读取回来，重构对象，对他进行反序列化
- 对象序列化流：ObjectOutputStream
- 对象反序列化流：ObjectInputStream

##### 对象序列化流

- ObjectOutputStream将Java对象的原始数据类型和图形写入OutputStream。 可以使用ObjectInputStream读取（重构）对象。 可以通过使用流的文件来实现对象的持久存储。 如果流是网络套接字流，则可以在另一个主机上或另一个进程中重构对象。

- 构造方法

- ```java
  ObjectOutputStream(OutputStream out)//创建一个写入指定的OutputStream的ObjectOutputStream
  ```

- 序列化对象方法

- ```java
  void writeObject(Object obj)//将指定的对象写入ObjectOutputStream
  ```

- 注意：一个对象想要被序列化，该对象所属的类必须实现Serializable接口，Serializable接口是一个标记接口，实现该接口，不需要重写任何方法

##### 对象反序列化流

- ObjectInputStream反序列化先前使用ObjectOutputStream编写的原始数据和对象

- 构造方法

- ```java
  ObjectInputStream(InputStream in)//创建从指定的InputStream读取的ObjectInputStream
  ```

- 反序列化对象方法

- ```java
  void readObject(Object obj)//从ObjectInputStream读取一个对象。
  ```

##### 注意

1. 在对象所属的类文件中写上private static final long serialVersionUID = 42L;可以防止在对象序列化流序列化一个对象后，修改了对象所属的类文件的内容时出现问题。
2. 在对象所属的类文件中被transient关键字修饰的成员变量不会在对象序列化中被序列化

#### Properties

##### 概述

- 是一个Map体系的集合类，Properties可以保存到流中或者从流中加载

##### 特有方法

- ```java
  Object setProperty(String key, String value)//设置集合的键和值，注意都是String类型 
  
  String getProperty(String key)//根据此属性列表中指定的键得到属性属性
  
  Set<String> stringPropertyNames()//从该属性列表中返回所有键的集合，其中键及其对应的值是字符串
  ```

eg：

- ```java
  Properties prop = new Properties(); 
  prop.setProperty("键","值");
  System.out.println(prop.getProperty("键"));//根据键得到值
  System.out.println(prop);
  Set<String> names = prop.stringPropertyNames();//得到所以键的集合
  for (String key:names){
  	System.out.println(key);
  }
  ```

##### Property与IO流结合的方法

```java
void load(InputStream inStream)//从输入字节流读取属性列表(键和元素对)

void load(Reader reader)//从输入字符流读取属性列表(键和元素对)

void store(OutputStream out, String comments)//将此属性列表(键和元素对)写入此property表中，以适合于使用load(InputStream inStream)方法的格式写入输出字节流

void store(Writer writer, String comments)//将此属性列表(键和元素对)写入此property表中，以适合于使用load(Reader reader)方法的格式写入输出字符P流
```

## 2.19.多线程

### 2.19.1.实现多线程

#### 进程

- 正在运行的程序，是系统进行资源分配和调用的独立单位，每个进程都有自己的内存空间和系统资源

#### 线程

- 进程中的单个顺序控制流，是一条执行路径

##### 单线程

- 一个进程只有一条执行路径

##### 多线程

- 一个进程有多条执行路径，即同时执行多个命令

##### 多线程的实现方式

1. 继承Thread类：

   定义一个类MyThread继承Thread类

   在MyThread类中重写run()方法

   创建MyThread类的对象object

   使用object.start()方法，自动启动线程，执行重写的run()方法

   注意：run()方法是用来封装被线程执行的代码；start()方法是启动线程，然后由JVM调用此线程的run()方法的

2. 实现Runnable类接口：

   定义一个类MyRunnable实现Runnable接口

   在MyRunnable类中重写run()方法

   创建MyRunnable类的对象

   创建Thread类的对象，把MyRunnable对象作为构造方法的参数，Thread(Runnabel)或Thread(Runnabel,””)

   启动线程

   相较于Thread类，实现Runnable接口的好处：避免了java单继承的局限性；适合多个相同程序代码去处理同一个资源的情况，把线程和程序的代码、数据有效分离，较好的体现了面向对象的设计思想

##### 设置和获取线程名称

- ```java
  void setName(String name)//将此线程的名称更改为name
  String getName()//返回此线程的名称
  static Thread currentThread() //返回对当前正在执行的线程对象的引用Thread.currentThread().getName()，此方法可以获取main()方法所在线程名称
  ```

- 初始线程名称：Thread-X X=0、1、2…
- 注意：一般是在run()方法中获取名称，在实现类中更改名称；也可以是在继承Thread类的类中添加一个无参构造方法，和一个带参构造方法:public 类名(String name){super(name);},此时即可在创建对象的时候选择无参的使用原本的线程名，或者选择带参的使用自己设置的线程名

##### 线程调度

- 线程调度的两种方式：分时调度模型、抢占式调度模型(优先级)
- JAVA使用的是抢占式调度模型，具有随机性

- ```java
  //Thread类中设置和获取线程优先级的方法：
  public final int getPority()//返回此线程的优先级
  public final void setPority(int newPriority)//更改此线程的优先级
  ```

- 注意：一般线程优先级默认为5，但执行时是随机抢占cpu的，设置优先级在[1-10]之间

##### 线程控制

```java
static void sleep(long millis)//使当前正在执行的线程停留(暂停执行)指定的毫秒数，一般在run方法内设置

void join()//等待这个线程结束，其余线程才可以继续

void setDaemon(boolean on)//将此线程标记为守护线程，当运行的线程都是守护线程时，java虚拟机将退出
```

##### 线程生命周期

- **NEW**: 线程新建状态
- **RUNNABLE**: 就绪状态
- **RUNNING**: 运行状态
- **BLOCKED**:堵塞状态
- **TERMINTED**:终止状态
  
![image](https://user-images.githubusercontent.com/91715224/193968768-69c38821-93ba-489c-8dff-53f562a834e4.png)


### 2.19.2.线程同步

#### 同步代码块

- 锁多条语句操作共享数据

- ```java
  synchronized(new Object()){
  	多条语句操作共享数据的代码
  }
  ```

- 注意：如果只需要一把锁，则需要在之前定义Object obj = new Object()，然后用obj替代new Object()

- 好处：解决了多线程的数据安全问题
- 缺点：当线程很多时，因为每个线程都会去判断同步上的锁，因此会很耗费资源，降低运行效率

#### 同步方法

- 就是把synchronized关键字加到方法上

- ```java
  修饰符 synchronized 返回值类型 方法名(方法参数){ 
  
  	}
  ```

- 注意：同步方法的锁对象是this

#### 同步静态方法

- ```java
  修饰符 static synchronized 返回值类型 方法名(方法参数){   }
  ```

- 注意：同步方法的锁对象是类名.class

#### 线程安全类

- StringBuffer：线程安全，可变的字符序列，从JDK5开始，被StringBulider替代，通常使用StringBulider类，因为它支持所有相同的操作，但速度更快，因为它不执行同步
- Vector：与新的集合实现不同，Vector被同步，如果不需要线程安全的实现，建议使用ArrayList代替Vector
- Hashtable：该类实现了一个哈希表，他将键映射到值，任何非null对象都可以用作键或者值，java2平台v1.2开始，该类进行了改进，实现了Map接口，使其成为Java Collections Framework的成员，与新的集合实现不同，Hashtable被同步，如果不需要线程安全的实现，建议使用HashMap代替Hashtable

#### Lock锁

1. ```java
   //ck实现提供比使用synchronized方法和语句可以获得的更广泛的锁定操作。
   void lock() //获得锁
   void unlock()//释放锁
   //Lock是接口不能直接实例化，采用他的实现类ReentrantLock来实例化
   
   //ReentrantLock的构造方法：
   ReentrantLock()//创建一个ReentrantLock的实例
   ```

### 2.19.3.生产者消费者

#### 概述

- 生产者消费者模式是一个经典的多线程协作的模式，实际上包含了两类线程
- 一类是生产者线程用于生产数据
- 一类是消费者线程用于消费数据
- 为了解耦生产者消费者之间的关系，通常会采用共享的数据区域，就像一个仓库
- 生产者生产数据之后直接放置在共享数据区中，并不需要关心消费者的行为
- 消费者只需要从共享数据区中获取数据，并不需要关心生产者的行为

#### 生产和消费过程中的等待与唤醒

- ```java
  //Object列中的等待和唤醒方法：
  
  void wait()//导致当前线程等待，直到另一个线程调用该对象的notify()方法或者notifyAll()方法
  
  void notify()//唤醒正在等待对象监视器的单个线程
  
  void notifyAll()//唤醒正在等待对象监视器的所有线程
  ```

## 2.20.网络编程

### 2.20.1.网络编程入门

#### 网络编程概述

- 在网络通信协议下，实现网络互连的不同计算机上运行的程序间可以进行数据交换

#### 网络编程三要素

- IP地址：即为每台计算机指定的一个标识号，通过这个标识号来指定要接受数据的计算机和识别发送的计算机，也是设备的标识
- 端口：网络的通信本质上是两个应用程序的通信，可以通过端口号区分应用程序，唯一标识设备中的应用程序，即是应用程序的标识
- 协议：通过计算机网络可以使多台计算机实现连接，位于同一个网络中的计算机在进行连接和通信时需要遵守一定的规则，在计算机网络中，这些连接和通信的规则被称为网络通信协议，对数据的传输格式、传输速率、传输步骤等做了统一的规定，通信双方必须同时遵守才能完成数据交换。常见的协议有UDP协议和TCP协议

#### IP地址

- IPv4：给每个连接在网络上的主机分配一个32bit地址，IP用2进制表示，每个IP地址长32bit，也就是4个字节，通常用十进制表示，中间用”,”分隔不同的字节
- IPv6：扩大了地址空间，采用128bit地址长度，每16个字节为一组，分成8组十六进制数

- 常用命令
- ipconfig：查看本机IP地址
- ping IP地址(即查询到的本机的IPv4地址)：检查网络是否连通 
- 特殊地址：170.0.0.1：是回送地址，可以代表本机地址，一般用来测试使用

#### InetAddress

- java提供的对IP地址的获取和操作的一个类

##### InetAddress方法

1. static InetAddress getByName(String host):确定主机名称的IP地址，主机名称可以是机器，可以是IP地址
2. String getHostName():获取此IP地址的主机名
3. String getHostAddress():返回文本显示中的IP地址字符串

#### 端口

- 端口号：用两个字节表示的整数，取值范围是0~65535，其中，0~1023之间的端口号用于一些知名的网络服务和应用，普通的应用程序需要使用1024以上而定端口号。如果端口号被另外一个服务或应用所占用，会导致当前程序启动失败

####  协议

- 计算机网络中，连接和通信的规则或称为网络通信协议

##### UDP协议

- 用户数据报协议(User Datagram Protocol)
- UDP是无连接通信协议，即在数据传输时，数据的发送端和接收端不建立逻辑连接。即当一台计算机向另一个计算机发送数据时，发送端不会确认接收端是否存在，就会发送数据，同样接收端在收到数据时，也不会向发送端反馈是否收到数据
- 由于使用UDP协议消耗资源小，通信效率高，所用通常都会用于音频、视频和普通数据的传输，但注意因为UDP的面向无连接性，因此在传输重要数据时不使用UDP协议

##### TCP协议

- 传输控制协议(Transmission Control Protocol)
- TCP协议是面向连接的通信协议，即在传输数据之前，在发送端和接收端建立逻辑连接，然后在传输数据，他提供了两台计算机之间可靠无差错的数据传输，在TCP连接中必须明确客户端和服务器端，由客户端向服务器端发出连接请求，每次连接的创建都需要经过“三次握手”
- 三次握手：TCP协议中，在发送数据的准备阶段，客户端和服务器之间的三次交互，以保证连接的可靠
- 第一次握手：客户端向服务器端发出连接请求，等待服务器确认
- 第二次握手：服务器端向客户端回送一个响应，通知客户端收到了连接请求
- 第三次握手：客户端再次向服务器端发送确认信息，确认连接
- 完成三次握手，连接建立后，客户端和服务器就可以开始进行数据传输了，由于TCP是面向连接的协议，所以可以保证传输数据的安全，所以可以用于上传文件、下载文件、浏览网页等

### 2.20.2. UDP通信程序

#### UDP通信原理

- UDP协议是一种不可靠的协议，他在通信的两端各建立一个socket对象，但是这两个socket只是发送、接收数据的对象，因此在UDP中没有客户端和服务器的概念
- Java提供了DatagramSocket类作为基于UDP协议的Socket

#### UDP发送数据

- 步骤

- ```java
  //1.    创建发送端的Socket对象
  DatagramSocket ds = new DatagramSocket();
  
  //2.    创建数据，并把数据打包
  DatagramPacket dp =new DatagramPacket(bys,length,address,port);
  
  //3.    调用DatagramSocket对象的方法发送数据
  ds.send(dp);
  
  //4.    关闭发送端
  ds.close();
  ```

#### UDP接收数据

- 步骤

- ```java
  //1.    创建接收端的Socket对象
  DatagramSocket ds = new DatagramSocket(prot);
  
  //2.    创建一个数据包
  DatagramPacket(byte[] buf, int length)
  
  //3.    调用DatagramSocket对象的方法接收数据
  ds.receive(dp)
  
  //4.    解析数据包，并把数据在控制台显示
  byte[] datas = dp.getData();
  int len = dp.getLength();//getLength()返回想要发送的数据的长度或者接收到的数据的长度
  String dataString = new String(datas,0,len);
  System.out.println("数据是"+dataString);
  
  //5.    关闭接收端
  ds.close();
  ```

### 2.20.3. TCP通信程序

#### TCP通信原理

- TCP是一种可靠的网络协议，他在通信的两端各建立一个Socket对象，从而在通信的两端形成网络虚拟链路，然后两端的程序可以通过虚拟链路进行通信
- java对基于TVP协议的网络提供了良好的封装，使用Socket对象来代表两端的通信端口，并通过Socket产生IO流来进行网络通信
- Java为客户端提供了Socket类，为服务器端提供了ServerSocket类

#### TCP发送数据

- 步骤：

- ```java
  //1.    创建客户端的Socket对象
  Socket(String host, int port)
  
  //2.    获取输出流，写数据
  OutputStream getOutputStream()
  
  //3.    释放资源
  void close()
  ```



#### TCP接收数据

- 步骤：

- ```java
  //1.    创建服务器端的Socket对象
  ServerSocket(int port)
  
  //2.    监听客户端连接，返回一个Socket对象
  Socket accept()
  
  //3.    获取输入流，读数据，并把数据显示在控制台
  InputStream getInputStream()
  
  //4.    释放资源
  void close()
  ```

## 2.21. Lambda表达式

### 2.21.1.函数式编程思想概述

- 函数式思想强调做什么，而不是以什么形式做

### 2.21.2. Lambda表达式的标准格式

- 组成Lambda表达式的三要素：形式参数、箭头、代码块

- 格式：

- ```java
  (形式参数)->{代码块}
  
  //()：里面没有内容，可以看成是方法形式参数为空
  
  //->：用箭头指向后面要做的事
  
  //{}：包含一段代码，可以看做是方法体中的内容，称为代码块
  
  //形式参数：如果有多个参数，参数之间用逗号隔开，如果没有参数，留空即可
  ```

- 使用前提：有一个接口，接口中有且仅有一个抽象方法

### 2.21.2. Lambda表达式的省略模式

1. 参数的类型可以省略，但有多个参数时，必须全部省略
2. 如果参数有且仅有一个，小括号也可以省略
3. 如果代码块的语句只有一条，则可以省略大括号和分号，如果有return，则return也要省略

### 2.21.3. Lambda表达式和匿名内部类的区别

1. 所需类型不同

   匿名内部类：可以是接口、抽象类，具体类

   Lambda表达式：只能是接口

2. 使用限制不同

   如果接口中有且仅有一个抽象方法，可以使用Lambda表达式，也可以使用匿名内部类

   如果接口中多于一个抽象方法，则只能使用匿名内部类

3. 实现原理不同

   匿名内部类：编译之后，会产生一个单独的.class字节码文件

   Lambda表达式：编译之后，没有一个单独的.class字节码文件，对应的字节码文件会在运行的时候动态生成

## 2.22.接口PLUS

### 2.22.1.概述

- 组成

1. 常量：public static final
2. 抽象方法：public abstract
3. 默认方法(java8)
4. 静态方法(java8)
5. 私有方法(java9)

### 2.22.2.接口中默认方法

- 格式：public default 返回值类型 方法名(参数列表){       }
- 注意：默认方法不是抽象方法，所以不强制被重写，但是可以被重写，重写的时候需要去掉default关键字，其中public可以省略，但default不能省略

### 2.22.3.接口中静态方法

- 格式：public static 返回值类型 方法名(参数列表){    }
- 注意：静态方法只能通过接口名调用，不能通过实现类名或者对象名调用，public可以省略，但static不能省略

### 2.22.4.接口中的私有方法

- ```java
  //格式1
      private 返回值类型 方法名(参数列表){       }
  
  //格式2
      private static 返回值类型 方法名(参数列表){  }
  
  //注意：默认方法可以调用私有的静态方法和非静态方法，静态方法只能调用私有的静态方法
  ```

## 2.23.方法引用

### 2.23.1.方法引用符

- ：：该符号为引用运算符，而他所在的表达式被称为方法引用

- eg:

- ```java
  //Lambda表达式
      userPrintable(s -> System.out.println(s));
  //分析：拿到参数s后通过Lambda表达式，传递给System.out.println方法处理
  ```

- ```java
  //方法引用
      userPrintable(System.out::println);
  //分析：直接使用System.out中的println方法来取代Lambda
  ```

- 推导与省略：
- 如果使用Lambda，那么根据可推导就可省略原则，无需指定参数类型，也无需指定重载形式，他们都将被自动推导
- 如果使用方法引用，也是同样可以根据上下文进行推导

### 2.23.2.Lambda表达式支持的方法引用

#### 引用类方法

- 即引用类的静态方法

- ```java
  //格式
  	//类名：：静态方法
  //eg：
      Integer：：parseInt     Integer类的方法：public static int parseInt(String s）
      //将String类型转换为int类型
  //Lambda表达式被类方法替代的时候，他的形式参数全部传递给静态方法作为参数
  ```

#### 引用对象

- 即引用类中的成员方法

- ```java
  //格式
      	//对象：：成员方法
  //eg
      ”Hello world”::toUpperCase     String类中的方法：public String toUpperCase()
         // 将此String所有字符转换为大写
  //Lambda表达式被对象的实例方法替代的时候，他的形式参数全部传递给该方法作为参数
  ```

#### 引用类的实例方法

- 即引用类中的成员方法

- ```java
  //格式
  	//类名：：成员方法
  //eg
  String::substring   String类中的方法：public String substring(int beginIndex int endIndex)     
      //从beginIndex开始到endIndex结束，截取字符串，返回一个子串，子串的长度为beginIndex-endIndex
  //Lambda表达式被类的实例方法替代的时候，第一个参数作为调用者，后面的参数全部传递给该方法作为参数
  ```

#### 引用构造器

- 即引用构造方法

- ```java
  //格式
  	//类名::new
  //eg
  Student：：new
  //Lambda表达式被构造器替代的时候，他的形式参数全部传递给构造器作为参数
  ```

## 2.24.函数式接口

### 2.24.1.函数式接口概述

- 有且仅有一个抽象方法的接口
- 通过注解来检测是否是函数式接口，@FunctionalInterface

### 2.24.2.函数式接口作为方法的参数

### 2.24.3.函数式接口作为方法的返回值

### 2.24.4.常用的函数式接口

#### Supplier接口

- ```java
  Supplier<T>//包含一个无参的方法
  T get()//获得结果
   //该方法不需要参数，他会按照某种实现逻辑(由Lambda表达式实现)返回一个数据
  Supplier<T>//接口也被称为生产型接口，如果我们指定了接口的泛型是什么类型，那么接口中的get方法就会生产什么类型的数据
  ```

#### Consumer接口

- ```java
  void accept(T t) //对给定的参数执行此操作
  default Consumer<T> andThen(Consumer<? super T> after) //返回一个组成的 Consumer ，依次执行此操作，然后执行 after操作
  Consumer<T>//接口也被称为消费型接口，他消费的数据的数据类型由泛型指定
  ```

#### Predicate接口

- ```java
  boolean test(T t) 在给定的参数上评估这个谓词 
  
  default Predicate<T> and(Predicate<? super T> other) ：返回一个组合的谓词，表示该谓词与另一个谓词的短路逻辑AND
  
  default Predicate<T> or(Predicate<? super T> other) ：返回一个组合的谓词，表示该谓词与另一个谓词的短路逻辑或
  
  default <T> negate() ：返回表示此谓词的逻辑否定的谓词
  
  Predicate<T>接口通常用于判断参数是否满足指定的条件
  ```

#### Function接口

- ```java
  default <V> Function<T,V> andThen(Function<? super R,? extends V> after)// 返回一个组合函数，首先将该函数应用于其输入，然后将 after函数应用于结果 
  R apply(T t)//将此函数应用于给定的参数 
  Function<T,R>//接口通常用于对参数进行处理，转换(处理逻辑由Lambda表达式实现)，然后返回一个新的值
  ```

## 2.25.Stream流

### 2.25.1.Stream流的生成方式

- Stream流的使用：
- 生成流：通过数据源(集合、数组等)生成流，list.stream()
- 中间操作：一个流后面可以跟随零个或多个中间操作，其目的是打开流，做出某种程度的数据过滤/映射，然后返回一个新的流，交给下一个操作使用，filter()
- 终结操作：一个流只能有一个终结操作，当这个操作执行后，流就被使用完了，无法再进行操作，forEach()

#### Stream流的常见生成方式

- Collection体系的集合可以使用默认方法Stream()生成流，default Stream<E> steam()
- Map体系的集合间接的生成流
- 数组可以通过Stream接口的静态方法of(T…values)生成流

### 2.25.2.Stream流的常见中间操作方法

- ```java
  //1.
  Stream<T> filter(Predicate predicate)//用于对流中的数据进行过滤
  Predicate接口中的方法    boolean test(T t)//对给定的参数进行判断，返回一个布尔值
  
  //2.
      Stream<T> limit(long maxSize)//返回流中的元素组成的流，截取指定参数个数的数据
  
  //3.
      Stream<T> skip(long n)//跳过指定参数个数的数据，返回由该流的剩余元素组成的流
  
  //4.
      static <T> Stream <T> concat(Stream a, Stream b)//合并a和b两个流为一个流
  
  //5.
      Stream<T> distinct()//返回由该流的不同元素(根据Object.equals(Object))组成的流
  
  //6.
      Stream<T> sorted()//返回由此流的元素组成的流，根据自然顺序排序
  
  //7.
      Stream<T>sorted(Comparator comparator)//返回由该流的元素组成的流，根据提供的Comparator进行排序
  
  //8.
      <R> Stream<R> map(Function mapper)//返回由给定函数应用于此流的元素的结果组成的流
       R apply(T t)//Function接口中的方法   
  
  //9.
      IntStream mapToInt(ToIntFunction mapper)：返回有个IntStream其中包含将给定函数应用于此流的元素的结果
      IntStream//表示原始int流，IntStream具有Stream不具有的sum()方法
      int applyAsInt(T value)//ToIntFunction接口中的方法    
  //注意：注意对流的操作，只能进行一次，操作过一次的流就不存在了
  ```

### 2.25.3.Stream流的常见终结操作方法

- ```java
  1.void forEach(Consumer action)//对此流中的每个元素执行操作
  
  //Consumer接口中的方法   
      void accept(T t)//对给定的参数执行此操作
      
  2.long count()//返回此流中的元素数
  ```

### 2.25.4.Stream流的收集操作

- ```java
  //Stream流的收集方法：
  R collect(Collector collector)        //但是这个收集方法的参数是一个Collector接口
  //工具类Collectors提供了具体的收集方法：
  1.public static <T> Collector toList()//把元素收集到List集合中
  2.public static <T> Collector toSet()//把元素收集到Set集合中
  3.public static Collector toMap(Function ketMapper, Function valueMapper)//把元素收集到Map集合中
  ```

## 2.26.反射

### 2.26.1.类加载器

####  类加载

- 当程序要使用某个类时，如果该类还未被加载到内存中，则系统会通过类的加载，类的连接，类的初始化三个步骤来对类进行初始化，也称类加载

##### 类的加载

- 指将class文件读入内存，并为之创建一个java.lang.Class对象

##### 类的连接

- ​    验证阶段：用于验证被加载的类是否有正确的内部结构，并和其他类协调一致
- ​    准备阶段：负责为类的类变量分配内存，并设置默认初始化值
- ​    解析阶段：将类的二进制数据中的符号引用替换为直接引用

##### 类的初始化

- ​    对类变量进行初始化

##### 类的初始化步骤

- ​    假如类还未被加载和连接，则程序先加载并连接该类
- ​    假如该类的直接父类还未被初始化，则先初始化其直接父类
- ​    假如类中有初始化语句，则系统依次执行这些初始化语句
- ​    注意：在执行第二个步骤时，系统对直接父类的初始化步骤也遵循步骤1-3

##### 类的初始化时机

- ​    创建类的实例
- ​    调用类的类方法
- ​    访问类或者接口的类变量，或者为该类变量赋值
- ​    使用反射方式来强制创建某个类或接口对应的java.lang.Class对象
- ​    初始化某个类的子类
- ​    直接使用java.exe命令来运行某个主类

#### 类加载器

- 作用：负责将.class文件加载到内存中，并为之生成对应的java.lang.Class对象

- JVM的类加载机制
- ​    全盘负责、父类委托、缓存机制

- ClassLoader：是负责加载类的对象

- java运行时具有以下内置加载器
- ​    Bootstrap class loader：虚拟机的内置类加载器，通常表示null，并且没有父null
- ​    Platform class loader：平台类加载器可以看到所有平台类，平台类包括由平台类加载器或其祖先定义的java SE平台API，其实现类和JDK特定的运行时类
- ​    System class loader：应用程序类加载器，与平台类加载器不同，系统类加载器通常用于定义应用程序类路径，模块路径和JDK特定工具上的类
- ​    类加载器的继承关系：System 的父类加载器为Platform，Platform 的父类加载器为Bootstrap

方法：

- ```java
  static ClassLoader getSystemClassLoader()//返回用于委派的系统类加载器
  
  ClassLoader getParent()//返回父类加载器进行委派
  ```

### 2.26.2.反射

#### 反射概述

- 是指在运行时去获取一个类的变量和方法信息，然后通过获取到的信息来创建对象，调用方法的一种机制，由于这种动态性，可以极大的增强程序的灵活性，程序不用在编译器就完成确定，在运行期仍然可以扩展
- 反射可以越过泛型检查，可以获取原始的方法所需的参数类型，然后调用原始的参数方法类型即可使用

#### 获取Class类的对象

- 首先获取到该类的字节码文件对象（即类型为Class类型的对象），然后可以通过反射去使用一个类

- 获取Class类型的对象方法：

1.  使用类的class属性来获取该类对应的Class对象，eg：Student.class将会返回Student类对应的Class对象

2. 调用对象的getClass方法，返回该对象所属类对应的

   Class对象该方法是Object类中的方法，所有的java对象都可以调用该方法

3. 使用Class类中的静态方法forName(String className)，该方法需要传入字符串参数，该字符串参数的值是某个类的全路径，也就是完整包名的路径

#### 反射获取构造方法并使用

- ```java
  //Class类中用于获取构造方法的方法：
  
  //1.   
  Constructor<?>[] getConstructors() //返回一个包含 Constructor对象的数组， Constructor对象反映了由该 Class对象表示的类的所有公共构造函数
  
  //2.    
  Constructor<?>[] getDeclaredConstructors() //返回反映由该 Class对象表示的类声明的所有构造函数的 Constructor对象的数组
  
  //3.    
  Constructor<T> getConstructor(Class<?>... parameterTypes) //返回一个 Constructor对象，该对象反映由该 Class对象表示的类的指定公共构造函数
  
  //4.    
  Constructor<T> getDeclaredConstructor(Class<?>... parameterTypes) //返回一个 Constructor对象，该对象反映由此 Class对象表示的类或接口的指定构造函数
  
  //注意：    
  //参数：想要获取的构造方法的参数个数和数据类型对应的字节码文件对象
  //Constructor<T>类中用于创建对象的方法 T newInstance(Object... initargs)：根据指定的构造方法创建对象
  ```

#### 反射取成员变量并使用

- ```java
  //Class类中获取成员变量的方法：
  
  //1.    
  Field[] getFields() //返回一个包含 Field对象的数组， Field对象反映由该 Class对象表示的类或接口的所有可访问的公共字段
  
  //2.    
  Field[] getDeclaredFields() //返回一个 Field对象的数组，反映了由该 Class对象表示的类或接口声明的所有字段
  
  //3.    
  Field getField(String name) //返回一个 Field对象，该对象反映由该 Class对象表示的类或接口的指定公共成员字段
  
  //4.    
  Field getDeclaredField(String name)// 返回一个 Field对象，该对象反映由该 Class对象表示的类或接口的指定声明字段
  
  //注意：
  //Field提供有关类或接口的单个字段的信息和动态访问
  //void set(Object obj, Object value) 将指定的对象参数中由此 Field对象表示的字段设置为指定的新值。
  ```

#### 反射获取成员方法并使用

- ```java
  //Class类中获取成员方法的方法：
  
  //1.    
  Method[] getMethods() //返回一个包含 方法对象的数组， 方法对象反映由该 Class对象表示的类或接口的所有公共方法，包括由类或接口声明的对象以及从超类和超级接口继承的类
  
  //2.    
  Method[] getDeclaredMethods() //返回一个包含 方法对象的数组， 方法对象反映由 Class对象表示的类或接口的所有声明方法，包括public，protected，default（package）访问和私有方法，但不包括继承方法
  
  //3.   
  Method getMethod(String name, Class<?>... parameterTypes) //返回一个 方法对象，该对象反映由该 Class对象表示的类或接口的指定公共成员方法
  
  //4.    
  Method getDeclaredMethod(String name, Class<?>... parameterTypes) //返回一个 方法对象，它反映此表示的类或接口的指定声明的方法 Class对象
  
  //注意：
  //Method在类或接口上提供有关单一方法的信息和访问权限
  //Object invoke(Object obj, Object... args) 在具有指定参数的指定对象上调用此 方法对象表示的基础方法
  ```

## 2.27.模块化

### 2.27.1.模块化概述

- Java语言伴随这些年的发展，越来越庞大，逐渐发发展成为一门“臃肿”的语言。无论是运行一个大型折软件系统，还是运行一个小的程序，即使程序只需要使用Java的部分核心功能，JVM也要加载整个JRE环境。为了给Java瘦身，让Java实现轻量化，Java9正式的推出了模块化系统。Java被拆分为N多个模块，并允许Java程序可以根据需要选择加载程序必须的Java模块，这样就可以让Java轻量化的方式运行。其实，Java7的时候已经提出了模块化的概念，但由于其过于复杂，Java7、Java8都一直未能真正推出，直到Java9才真正成熟起来。对于Java语言来说，模块化系统是一次真正的自我革新。

### 2.27.2.模块的基本使用

- 步骤

1. 创建模块（创建模块、创建包、创建类、定义方法）

2. 在模块src目录下新建一个名为module-info.java的描述性文件，该文件专门定义模块名，访问权限，模块依赖等信息，描述性文件中使用模块导出和模块依赖来进行配置并使用

3. 模块中所有未导出的包都是模块私有的，他们是不能在模块之外被访问的，在模块一下的描述性文件中配置模块导出。

   模块导出格式：exports 包名;

4. 一个模块要访问其他模块，必须明确指定依赖哪些模块，未明确指定依赖的模块不能访问。在模块二下的描述性文件中配置模块依赖。

   模块依赖格式：requires 模块名;

   注意：写模块名报错，需要按下Alt+Enter提示，然后选择模块依赖。

5. 在模块二的类中使用依赖模块下的内容。

### 2.27.3.模块服务的使用

- 模块服务的使用步骤

1. 在myOne模块一下创建一个包com.service，在该包下提供一个接口，接口中定义一个抽象方法

2. 在com.service包下创建一个包impl，在该包下提供两个实现类S1、S2

3. 在myOne模块下的描述性文件中添加如下配置

   模块导出：exports com.service;

   服务提供：provides MyService with S1; 指定MyService的服务实现类是S1

4. 在myTwo这个模块下的描述性文件中添加如下配置

   声明服务接口：usesMyService;

5. 在myTwo这个模块的类中使用MyService接口提供的服务

   ServiceLoader：一种加载服务实现的工具。
