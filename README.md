
# 设计模式

## 单例模式
单例模式是一种创建型设计模式， 让你能够保证一个类只有一个实例， 并提供一个访问该实例的全局节点。
### 有了全局变量为什么还要单例模式？

全局变量和单例模式都可以用于在程序中创建全局唯一的对象，但它们的实现方式和应用场景有所不同。\
全局变量是一种简单的方式来表示在整个程序中只需要存在一个实例的对象。但是，全局变量可能会导致命名空间污染和代码的可维护性问题。\
单例模式是一种设计模式，它提供了一种更加灵活和可控的方式来创建全局唯一的对象。它通过将对象的创建和访问进行封装，从而避免了全局变量的问题。此外，单例模式还可以提供一些额外的特性，比如懒加载和线程安全等。
因此，尽管全局变量可以实现类似的功能，但在需要更加优雅和可维护的代码时，单例模式是更好的选择。
### 单例模式适合应用场景
程序中的某个类对于所有客户只有一个可用的实例， 可以使用单例模式。
比如：windows 任务管理器只能打开一个
### 饿汉模式
饿汉模式就是在类加载的时候立刻进行实例化，这样就得到了一个唯一的可用对象，是线程安全的。
### 懒汉模式
懒汉模式是在类加载的时候不去创建这个唯一的实例，而是在需要使用的时候再进行实例化，是线程不安全的。
### 实现方式
* 将默认构造函数设为私有， 防止对象使用new运算符。
* 将拷贝构造和运算符禁用， 防止对象拷贝。
* 创建一个静态方法来获取相同的对象。
懒汉模式实现，见demo1[]