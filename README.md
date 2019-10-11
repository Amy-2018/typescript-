## typescript入门

##### TypeScript 的安装和编译

1.   tsc 编译

     npm i -g typescript 

     tsc -v
   
     tsc index.ts
   


2. nodemon编译 

   npm install -g nodemon  
   
   nodemon index.ts 
   

3. IDE自动编译

#### 数据类型

1. 布尔类型（boolean）
2. 数字类型（number）
3. 字符串类型(string)
4. 数组类型（array）
5. 元组类型（tuple）
6. 枚举类型（enum）
7. 任意类型（any）
8. null 和 undefined
9. void类型
10. never类型
    用于函数返回值时，表示函数有抛出异常，没有正常执行到底。用于变量声明，无法为其赋予任何值！
11. 联合类型 |
12. 类型断言 手动指定一个值的类型  
    语法：<类型>值 或 值 as 类型
    注： 类型断言不是类型转换，断言成一个联合类型中不存在的类型是不允许的
    

#### 函数

##### 函数定义法

1. 函数声明法
2. 匿名函数

##### 定义方法传参

1. 固定参数
2. 可选参数
3. 默认参数
4. 剩余参数 rest
注： 可选参数、默认参数、rest都要放到最后

##### 函数重载

重载允许一个函数接受不同数量或类型的参数时，作出不同的处理。

#### 类

##### 修饰符

public 默认

private 在类里面可以访问，在子类、类外部不能访问

protected 在类里面子类里面可以访问，在类外部不能访问

public > protected > private








