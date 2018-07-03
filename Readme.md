Java Collections Framework(JCF)

# 关于Java集合（Java Collection）
> 本质是数据结构，用于存储数据。不同类型集合对应不同的数据结构，用于数据的不同组织形式。
> 由JAVA语言提供，开发人员直接使用，提升开发人员效率，同时Java集合有着非常好的性能。
> 对集合知识掌握地越好，越能更好地使用它们

* 存储对象

> Java集合只能存放对象，基本类型（int,float,double,long）无法放入集合中，必须使用各自的对象类型（Integer,Float,Double,Long）


* 泛型没那么玄乎

> Java容器支持各种类型对象的存储，这叫泛型。类型的确定其实是编译阶段进行(语法)，编译期间通过集合的参数类型来进行类型强转。
> 集合可以存储任何类型，当然包括所有对象类型的父类Object。

* 容器和对象的内存

> Java对象都在堆中，容器并不包含对象的实际数据，而是保存指向各个对象的引用。

* 迭代器

# 集中结合类
* ArrayList

> 顺序容器，内部元素使用数组（Object数据，实现泛型）进行存储。理解size和capacity，capacity是容器容量，size为数组的当前长度。当size大于capacity，需要扩充数据大小然后将元素拷贝。capacity有一个初始值。

* ArrayList & Vector

> ArrayList非线程安全，Vector线程安全。非线程安全主要从性能角度考虑。