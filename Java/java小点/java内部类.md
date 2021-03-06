## 内部类和匿名类

内部类有个例子见[java计算器实现](../javaGUI(浅尝辄止,因为不使用)/java计算器实现.md)中的方法3

---

##### 内部类

- 内部类定义
  - 在A类的内部但是所有方法的外部定义了一个B类，则B类就是A类的内部类，A是B的外部类
- 内部类访问原则
  - 内部类的方法可以访问外部类所有的成员
  - 外部类的方法不可以直接访问内部类的成员
- 内部类的优点
  - 可以让一个类方便地访问另一个类中的所有成员
  - 增加程序的安全性，有效避免其他不相关类对该类的访问
- <strong style="color:red;">何时使用内部类</strong>
  - 如果一个A类要使用B类的所有成员，并且A类不需要被除B类以外的其他类访问，则我们应当把A类定义为B类的内部类



- **我们可以把内部类当做内部类的一个成员**
  - 也就是说地位和外部类内的方法和属性地位对等, 这样的话就可以互相访问
  - 也就是地位相等的方法是可以使用该内部类来造对象的, 注意, 仍然不能访问这个类里面的



---

#### 匿名类

- 继承父类
- 实现接口
- 实现抽象类

##### 创建匿名类之实现接口

- 假设A 是接口名

- 格式:

  ```java
  new A()
  
  {
  
  	实现接口中方法的代码
  
  };
  ```

- 功能:

  - 生成一个实现了A接口的匿名类 



##### **创建匿名类之实现抽象类**

- 假设A是抽象类

- 格式

  ```java
  new A()
  {
  	实现了A类的所有抽象类的方法代码
  	添加自己的方法或属性代码[不建议, 因为没有实际意义]
  }
  ```

- 功能

  - 生成一个匿名类, 该匿名类必须得实现了A类的所有抽象方法, 当然该匿名类也可以定义自己的属性和方法



##### 创建匿名类之继承父类

- 假设A是个类名

- 格式

  ```java
  new A()
  {
  	重写了A类的方法代码
  	添加自己的属性和方法[不建议, 因为没有实际意义]
  }
  ```

- 功能

  - 生成一个A类的子类对象, 该匿名类对象继承了A所有非private成员

---

- 匿名类是一种特殊的内部类
- 如果在一个方法内部定义了一个匿名类，则该匿名类可以访问
  - 外部类的所有成员
  - 包裹该匿名类的方法中的所有 `final` 类型的局部变量
    - 注意：非 `fianal` 类型的局部变量无法被匿名类访问



---

##### 匿名类的优缺点

- 如果一个类的语句比较少, 逻辑比较简单, 而且不经常变动, 这个时候可以使用匿名类
- 如果一个类包含了很重要的逻辑, 将来经常要修改, 则这个类就不应该当做匿名类来使用, 匿名类会导致代码的混乱





