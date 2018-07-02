# 关于Java集合（Java Collection）

* 存储对象

> Java集合只能存放对象，基本类型（int,float,double,long）无法放入集合中，必须使用各自的对象类型（Integer,Float,Double,Long）


* 泛型没那么玄乎
> Java容器支持各种类型对象的存储，这叫泛型。类型的确定其实是编译阶段进行，编译期间通过集合的参数类型来进行类型强转。
> 集合可以存储任何类型，当然包括所有对象类型的父类Object。

* 容器和对象的内存
> Java对象都在堆中，容器并不包含对象的实际数据，而是保存指向各个对象的引用。