# scala基础
## scala基本数据类型

scala中的数据类型都是**object**类型的，它是真正的一切皆对象

数据类型分为两大类

1.值类型 （java中的基本类型） —值类型是类类型

2.引用类型

![scala数据结构图](https://docs.scala-lang.org/resources/images/tour/unified-types-diagram.svg)

它支持八大基础数据类型：

- Byte
- Int
- Short
- Float
- Long
- Double
- Char
- Boolean
- Unit相当于Java中的void类型
- Nothing是异常情况

scala工具库里有个去除多行字符串**行首**的空格 的工具类`stripMarigin`

## scala中的循环

### 1.for循环

语法：

```
for(i <- 表达式，数组，集合)
```

ps: `for(i <- 1 to 10) println(i)`打印出1到10，10次

​     `for(i <- 1 until 10) println(i)` 打印出1到9，9次不包括右边边界值

1 to 10返回的是个range是个集合 1 until 10也是

e.g：打印一个字符串中的每个字母

```
1.
val s:String="scala"
s: String = scala
for(i<-0 until s.length) println(s(i))
s
c
a
l
a
2.字符串也是可以变成集合的(隐式转换 可以把字符串转换成一个字符序列)
scala> for(i <- s)println(i)
s
c
a
l
a
3.
scala> for(i <-0 until s.length)println(s.charAt(i))
s
c
a
l
a

```

双重for循环:高级for循环

```
找到10位数和个位数不一样的地方
scala> for(i<-1 to 3;j<-1 to 3;if(i!=j))print(i*10+j+" ")
12 13 21 23 31 32 
```

用原有的集合产生一个新的集合：

```
scala> val res=for(a <-1 to 10) yield a*10
res: scala.collection.immutable.IndexedSeq[Int] = Vector(10, 20, 30, 40, 50, 60, 70, 80, 90, 100)
```



### 2.while循环

```
while(条件语句){表达式}
```



### 3.do-while循环

```
do{
表达式
}while(条件语句)
```





