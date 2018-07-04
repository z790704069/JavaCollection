Java Collections Framework(JCF)

# 关于Java集合（Java Collection）
> 本质是数据结构，用于存储数据。不同类型集合对应不同的数据结构，用于数据的不同组织形式。
> 由JAVA语言提供，开发人员直接使用，提升开发人员效率，同时Java集合有着非常好的性能。
> 对集合知识掌握地越好，越能更好地使用它们

* 存储对象

> Java集合只能存放对象，基本类型（int,float,double,long）无法放入集合中，必须使用各自的对象类型（Integer,Float,Double,Long）


* 泛型没那么神秘

> Java容器支持各种类型对象的存储，这叫泛型。类型的确定其实是编译阶段进行(语法)，编译期间通过集合的参数类型来进行类型强转。
> 集合可以存储任何类型，当然包括所有对象类型的父类Object。

* 容器和对象的内存

> Java对象都在堆中，容器并不包含对象的实际数据，而是保存指向各个对象的引用。

* 迭代器

# 几个重要类/接口

```
java.util.Collection [I]
+--java.util.List [I]
   +--java.util.ArrayList [C]
   +--java.util.LinkedList [C]
   +--java.util.Vector [C]
      +--java.util.Stack [C]
+--java.util.Set [I]
   +--java.util.HashSet [C]
   +--java.util.SortedSet [I]
      +--java.util.TreeSet [C]

java.util.Map [I]
+--java.util.SortedMap [I]
   +--java.util.TreeMap [C]
+--java.util.Hashtable [C]
+--java.util.HashMap [C]
+--java.util.LinkedHashMap [C]
+--java.util.WeakHashMap [C]
```

以上为Java集合框架的一个大致情况（该层次情况很重要），主要分为List,Set以及Map三个接口。其中List和Set属于Collection,也就是说Collection与Map级别相同。其中List以及Set可以理解为集合，Map是一种关联容器，跟List、Set从大的概念上来看不相同。

* ArrayList

> 顺序容器，内部元素使用数组（Object数据，实现泛型）进行存储。理解size和capacity，capacity是容器容量，size为数组的当前长度。当size大于capacity，需要扩充数据大小然后将元素拷贝。capacity有一个初始值。

* ArrayList & Vector

> ArrayList非线程安全，Vector线程安全。非线程安全主要从性能角度考虑

* LinkedList
> 内部实现为双向队列，所以可以作为栈或队列来使用。

* Set(接口)
> 不允许有重复元素存在

* Map接口
> Map没有继承Collection接口。也就是说Map和Collection是2种不同的集合。Collection可以看作是（value）的集合，而Map可以看作是（key，value）的集合。
Map接口由Map的内容提供3种类型的集合视图，一组key集合，一组value集合，或者一组key-value映射关系的集合。

* HashMap & HashTable
> HashTable线程安全，HashMap非线程安全。
> HashMap可以接受空（null）的key和value，而Hashtable则不行

