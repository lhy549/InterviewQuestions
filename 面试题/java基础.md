# java基础面试题

标签： java

---

**Contents**

- [java基础常见面试题](#java基础笔记常见面试题)
  - [多态的实现机制是什么](#多态的实现机制是什么)
  - [多态有两种表现方式](#多态有两种表现方式)
  - [抽象类和接口有什么异同？](#抽象类和接口有什么异同)
  - [面向对象有哪些特征？](#面向对象有哪些特征)
  - [java语言有什么优点？](#java语言有什么优点)
  - [final在java中有什么作用？](#final在java中有什么作用)
  - [java中的访问修饰符](#java中的访问修饰符)
  - [抽象类必须要有抽象方法吗？](#抽象类必须要有抽象方法吗)
  - [普通类和抽象类有哪些区别？](#普通类和抽象类有哪些区别)
  - [java中IO流分为几种?](#java中IO流分为几种)
  - [抽象类能使用final修饰吗？](#抽象类能使用final修饰吗)
  - [Files的常用方法都有哪些？](#Files的常用方法都有哪些)
  - [String类的常用方法都有那些](#String类的常用方法都有那些)
  - [如何将字符串反转？](#如何将字符串反转)
  - [java中的Math.round(-1.5)等于多少](#java中的Math.round(-1.5)等于多少)
  - [String属于基础的数据类型吗？](#String属于基础的数据类型吗)
  - [Java中的基本数据类型](#Java中的基本数据类型)
  - [==和equals的区别是什么？](#==和equals的区别是什么)
  - [Stringstr="i"与String str=new String("i")一样吗?](#Stringstr="i"与Stringstr=newString("i")一样吗)
 
---

## 多态的实现机制是什么

表示当同一个操作作用在不同对象时，会有不同的语义，从而产生了不同的结果。

## 多态有两种表现方式

- 方法重载。重载是指同一个类中有多个同名的方法，但是他们的参数不同，在编译时就可以确定到底调用了哪个方法，它是一种编译时多态。重载可以被看作一个类中的方法多态性。
- 方法覆盖。子类可以覆盖父类的方法，因此同样的方法会在父类与子类中有着不同的表现形式。

## 抽象类和接口有什么异同？

相同点：

- 都不能被实例化
- 接口的实现类或者抽象类的子类都只有实现了接口或者抽象类中的方法后才能被实例化。

不同点：

- 接口只有定义，其方法不能在接口中实现，只有实现接口的类才能实现接口中定义的方法，而抽象类可以有定义与实现，即其方法可以在抽象类中被实现
- 接口需要实现（implements），但是抽象类需要继承（extends）。一个类可以实现多个接口，但一个类只能继承一个抽象类，因此使用接口可以间接的达到多重继承的目的
- 接口强调特定功能的实现，其设计理念是“”has a“”关系，抽象类强调所属关系，is a 关系

## 面向对象有哪些特征？

- 封装：每个类对自身的数据和方法实行保护。
- 继承：对象的一个新类可以从现有的类中派生，此过程称为类继承。
- 多态：多态是允许不同类的对象对同一消息做出相应。

## java语言有什么优点？

- 纯面向对象编程语言
- 平台无关性
- 具有较好的安全性和健壮性

## final在java中有什么作用？

final关键字可以用来修饰类、方法和变量（包括成员变量和局部变量）

-  修饰类 

  当用final修饰一个类时，表明这个类不能被继承
 
-  修饰方法

“使用final方法的原因有两个。第一个原因是把方法锁定，以防任何继承类修改它的含义；第二个原因是效率。在早期的Java实现版本中，会将final方法转为内嵌调用。但是如果方法过于庞大，可能看不到内嵌调用带来的任何性能提升。在最近的Java版本中，不需要使用final方法进行这些优化了

类的private方法会隐式地被指定为final方法

-  修饰变量

修饰变量是final用得最多的地方，也是本文接下来要重点阐述的内容。首先了解一下final变量的基本语法：

对于一个final变量，如果是基本数据类型的变量，则其数值一旦在初始化之后便不能更改；如果是引用类型的变量，则在对其初始化之后便不能再让其指向另一个对象。

## java中的访问修饰符

- public： 用public修饰的类、类属变量及方法，包内及包外的任何类（包括子类和普通类）均可以访问；

- protected： 用protected修饰的类、类属变量及方法，包内的任何类及包外那些继承了该类的子类才能访问（此处稍后解释），protected重点突出继承；
　
- default： 如果一个类、类属变量及方法没有用任何修饰符（即没有用public、protected及private中任何一种修饰），则其访问权限为default（默认访问权限）。默认访问权限的类、类属变量及方法，包内的任何类（包括继承了此类的子类）都可以访问它，而对于包外的任何类都不能访问它（包括包外继承了此类的子类）。default重点突出包；

- private： 用private修饰的类、类属变量及方法，只有本类可以访问，而包内包外的任何类均不能访问它

## 抽象类必须要有抽象方法吗？

抽象类可以没有抽象方法，但是如果你的一个类已经声明成了抽象类，即使这个类中没有抽象方法，它也不能再实例化，即不能直接构造一个该类的对象。但是有抽象方法，该类一定是抽象类。

如果一个类中有了一个抽象方法，那么这个类必须声明为抽象类，否则编译通不过。


## java中IO流分为几种？
![](https://i.imgur.com/gRLU9lC.png)
![](https://i.imgur.com/UENezuJ.jpg)

## 抽象类能使用final修饰吗？

## Files的常用方法都有哪些？

java.io.File类主要是完成了文件夹管理的命名、查询文件属性和处理目录等到操作它不进行文件夹内容的读取操作。以下描述了File类的主要常用方法。 

File()：构造函数，一般是依据文件所在的指定位置来创建文件对象。
  
CanWrite()：返回文件是否可写。  

CanRead()：返回文件是否可读。 

CompareTo(File pathname)：检查指定文件路径间的顺序。
 
Delet()：从文件系统内删除该文件。 

DeleteOnExit()：程序顺利结束时从系统中删除文件。 

Equals(Object obj)：检查特定对象的路径名是否相等。
 
Exists()：判断文件夹是否存在。 

GetAbsoluteFile()：返回文件的完整路径。 

GetAbsolutePath()：返回文件的完整路径。 

GetName()：返回文件名称。 

GetParent()：返回文件父目录路径。 

GetPath()：返回文件的潜在相对路径。 

GetParentFile()：返回文件所在文件夹的路径。 

HashCode()：返回文件哈希码。 

IsDirectory()：判断该路径指示的是否是文件。 

IsFile()：判断该路径指示的是否是文件。 

LastModified() ：返回文件的最后修改时间标志。 

Length()：返回文件长度。 

List()：返回文件和目录清单。 

Mkdir()：生成指定的目录。 

RenameTo(File dest)：更名文件。 

SetReadOnly()：将文件设置为可读。 

ToString()：返回文件状态的字符串。 

ToURL()：将文件的路径字符串转换成URL 

File.GetCreationTime 读取创建时间 

file.SetCreationTime 设置创建时间 

File.GetLastAccessTime   读取最后访问时间 

File.SetLastAccessTime   设置最后访问时间 

File.GetLastWriteTime 读取最后修改时间 

File.SetLastWriteTime 设置最后修改时间 

File.GetAttributes 读取文件属性 

File.SetAttributes 设置文件属性

## String类的常用方法都有那些?

**String构造方法**

String(String original):把字符串数据封装成字符串对象

String(char[] value):把字符数组的数据封装成字符串对象

String(char[] value, int index, int count):把字符数组中的一部分数据封装成字符串对象

**String判断功能**

boolean equals(Object obj):比较字符串的内容是否相同

boolean equalsIgnoreCase(String str):比较字符串的内容是否相同,忽略大小写

boolean startsWith(String str):判断字符串对象是否以指定的str开头

boolean endsWith(String str):判断字符串对象是否以指定的str结尾

**String类的获取功能：**

 int length():获取字符串的长度，其实也就是字符个数

 char charAt(int index):获取指定索引处的字符

 int indexOf(String str):获取str在字符串对象中第一次出现的索引

 String substring(int start):从start开始截取字符串

 String substring(int start,int end):从start开始，到end结束截取字符串。包括start，不包括end

**转化方法：**

char[] toCharArray():把字符串转换为字符数组

String toLowerCase():把字符串转换为小写字符串

String toUpperCase():把字符串转换为大写字符串

**按照指定符号分割字符串**

String[] split(String str)

StringBuilder:是一个可变的字符串。字符串缓冲区类。  

split()方法将一个字符串对象的每个字符拆出来，并且将每个字符串当成数组的每个元素

reverse()方法用来改变数组，将数组中的元素倒个序排列，第一个数组元素成为最后一个，最后一个变成第一个

join()方法将数组中的所有元素边接成一个字符串

## 如何将字符串反转？

    function reverseString(str) {
          // 第一步，使用split()方法，返回一个新数组
          // var splitString = "hello".split("");
     
          var splitString = str.split(""); //将字符串拆分
      
          // 返回一个新数组["h", "e", "l", "l", "o"]
      
         // 第二步，使用reverse()方法创建一个新数组
         // var reverseArray = ["h", "e", "l", "l", "o"].reverse();
     
         var reverseArray = splitString.reverse(); 
         // 原数组元素顺序反转["o", "l", "l", "e", "h"]
     
         // 第三步，使用join()方法将数组的每个元素连接在一起，组合成一个新字符串
         // var joinArray = ["o", "l", "l", "e", "h"].join("");
     
         var joinArray = reverseArray.join(""); 
         // "olleh"
     
         // 第四步，返回一个反转的新字符串
         return joinArray; // "olleh"
    }
 
    reverseString("hello"); // => olleh

## java中的Math.round(-1.5) 等于多少？

round是四舍五入，注意负数5是舍的，例如：Math.round(1.5)值是2，Math.round(-1.5)值是-1；
floor就是直接去掉小数保留整数，即如果参数是正数则小数部分全舍，参数是负数则小数部分全入。 例如：Math.floor(2.6)的值是2，Math.floor(-2.1)的值是-3


## String属于基础的数据类型吗？

不是

## Java中的基本数据类型？

-  byte
-  short
-  int
-  long
-  float
-  double
-  char
-  boolean

## ==和equals的区别是什么？

- ==号比较的是内存地址
- equals()比较的是字符串的内容

## Stringstr="i"与Stringstr=newString("i")一样吗？

1. 当使用String str="abc",这种方式时，先去内存的Heap中找是否存在"abc"这个字符串，若存在，则将地址引用。若不存在则创建。
2. 当使用String str=new String("abc");时，不管事先是否存在"abc"，每次都会创建其新的对象。


















