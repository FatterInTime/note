## 0.目录



## 1.八股文

### 1.1 关键字

####  **1.1.1 const** 

被他修饰的值不能改变，是只读变量。必须在定义时就要给他赋初值。

(1) 常量指针

const int *a 修饰int,int const *a 

修饰*a 只读变量 

```c
int tmp = 9;

  const int *a = &tmp;

  int const *b = &tmp;

  printf(" a:%d b :%d tmp:%d\n", *a, *b, tmp);

  tmp = 10;

  printf(" a:%d b :%d tmp:%d\n", *a, *b, tmp);
```

*a *b 不可以修改， a，b可以修改 a = &tmp1, b=&tmp2

修改tmp也可以改变值

(2)指针常量

  int * const c =  &tmp;

*c 可以改变 c不可以改变

#### 1.1.2 define typedef  inline 

**define:**

(1)简单的字符串替换，编译器没有类型检查

(2)编译的预处理阶段起作用

(3)可以用来防止头文件重复

(4)不分配内存，是立即数，有多少次使用就有多少次替换

 

**typedef：**

(1) 有对应的数据类型，编译器会类型检查

(2) 编译,运行的时候起作用

(3) 静态存储区分配空间，程序运行时 内存只有一个拷贝

 

**inline：**

  先把内联函数编译完成，生成的函数体 直接插入被调用的地方，减少了压栈 跳转 返回的操作。

  内联函数是特殊函数 也会进行类型检查，但是属于对编译器的请求，编译器有可能拒绝这种请求 。

  在C++种还有额外的限制：

   a.不能存在任何循环 b.不能存在过多的条件判断

  c. 函数体不能过于庞大 d.声明必须在调用前

