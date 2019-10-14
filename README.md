## typescript入门

### 关于 TypeScript

 JavaScript 的一个超集，主要提供了类型系统和对 ES6 的支持

##### TypeScript 的安装和编译

1.   tsc 编译

     npm i -g typescript 

     tsc -v
   
     tsc index.ts
   


2. nodemon编译 

   npm install -g nodemon  
   
   nodemon index.ts 
   

3. IDE自动编译



### 数据类型

1. 布尔类型（boolean）

   取值只能是true、false
2. 数字类型（number）

   数字类型, 整数/小数都包括, 同时支持2/8/10/16进制字面量.
3. 字符串类型(string)
4. 数组类型（array）

    1).指定类型后面增加[] eg：number:[]
    
    2).泛型 Array[number]
5. 元组类型（tuple）

    元组类型表示一个已知元素数量和类型的数组, 各元素的类型不必相同:
    
    let list4:[number, string] = [1, '2'];
6. 枚举类型（enum）

   用于取值被限定在一定范围内的场景，比如一周只能有七天
   
   编译后会被转化成对象, 默认元素的值从0开始，也可以手动设置值
   
7. 任意类型（any）

   1.接入第三方库
   
   2.初学前期
   
8. null 和 undefined 

   当你指定了--strictNullChecks标记，null和undefined只能赋值给void和它们各自
9. void类型 

   一般用来标记函数没有返回值
   
   这时候就不能写return了
10. never类型 

    . throw new Error(message)
    
    . return error("Something failed")
    
    . while (true) {} // 存在无法达到的终点
    
11. 联合类型 |  

     联合类型也是将多个类型合并为一个类型, 表示"或"的关系,用|连接多个类型
     
12. 交叉类型 &  

    交叉类型是将多个类型合并为一个类型, 表示"并且"的关系,用&连接多个类型, 常用于对象合并
    
13. 类型断言 手动指定一个值的类型  

    语法：<类型>值 或 值 as 类型
    
    注： 类型断言不是类型转换，断言成一个联合类型中不存在的类型是不允许的
    
 14. 类型推论 
 
     如果没有明确的指定类型，那么 TypeScript 会依照类型推论（Type Inference）的规则推断出一个类型。
 
 15. 类型别名 type 
 
     使用 type 创建类型别名,类型别名常用于联合类型
  
 16. 对象类型 object 
 
     一般不用，他标注不具体，一般用接口
 
 17. unknown 
     
      任何东西都可以赋值给 unknown，但 unknown 不能赋值给除了它本身和 any 以外的任何东西, 在没有先断言或指定到更具体类型的情况下，
      不允许对 unknown 进行任何操作
     
 17. 接口 interface
 
     - 它是对行为的抽象，而具体如何行动需要由类（classes）去实现（implements）。
     
     - 字段个数、类型必须一致
     
     - 非必填(?) 
     
     - 只读属性 readonly 只读的约束存在于第一次给对象赋值的时候
     
     - 顺序： 只读参数放第一位，必选参数第二位，可选参数次之，不确定参数放最后 
     
     - 任意属性 一旦定义了任意属性，那么确定属性和可选属性都必须是它的子属性
     
     - 对于从服务器端获取或者业务场景中模拟的数据（数据通常不经常变化和调整的），或者ui文本
     
      
       ```
       interface iProps {
 
         readonly x: number;
 
         readonly y: number;
         
         name: string;
         
         age: number;
         
         height?: number;
         
         [propName: string]: any;
       }
       ```

### 函数

#### 函数定义法

1. 函数声明法
2. 匿名函数

#### 定义方法传参

1. 固定参数
2. 可选参数
3. 默认参数
4. 剩余参数 rest
注： 可选参数、默认参数、rest都要放到最后

#### 函数重载

重载允许一个函数接受不同数量或类型的参数时，作出不同的处理。

### 类

#### 修饰符

public 默认

private 在类里面可以访问，在子类、类外部不能访问

protected 在类里面子类里面可以访问，在类外部不能访问

public > protected > private

#### 特性

1. 静态属性

2. 静态方法

3. 多态 
   父类定义一个方法不去实现，让继承它的子类去实现，每一个子类有不同表现

4. 抽象类 
   它是提供其他类继承的基类，不能直接被实例化
   abstract抽象方法只能在抽象类中
   子类必须实现抽象方法


### 泛型
    解决类、接口、方法的复用、以及对不特定数据类型的支持
    
    







