# **js 中 ... 的用法**

**展开语法(Spread syntax),** 可以在函数调用/数组构造时, 将数组表达式或者string在语法层面展开；还可以在构造字面量对象时, 将对象表达式按key-value的方式展开。(**译者注**: 字面量一般指 [1, 2, 3] 或者 {name: "mdn"} 这种简洁的构造方式)

function sum(x, y, z) {

 return x + y + z;

}

const numbers = [1, 2, 3];

console.log(sum(...numbers));

// expected output: 6

console.log(sum.apply(null, numbers));

// expected output: 6

## **语法**

函数调用：

myFunction(...iterableObj);

字面量数组构造或字符串：

[...iterableObj, '4', ...'hello', 6];

构造字面量对象时,进行克隆或者属性拷贝（ECMAScript 2018规范新增特性）：

let objClone = { ...obj };

## **示例**

在函数调用时使用展开语法

等价于apply的方式

如果想将数组元素迭代为函数参数，一般使用[Function.prototype.apply](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/apply) 的方式进行调用。

function myFunction(x, y, z) { }

var args = [0, 1, 2];

myFunction.apply(null, args);

有了展开语法，可以这样写：

function myFunction(x, y, z) { }

var args = [0, 1, 2];

myFunction(...args);

 所有参数都可以通过展开语法来传值，也不限制多次使用展开语法。

function myFunction(v, w, x, y, z) { }

var args = [0, 1];

myFunction(-1, ...args, 2, ...[3]);