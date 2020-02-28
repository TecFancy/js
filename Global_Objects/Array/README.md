# Array

## 表现形式

``` js
[element0, element1, ..., elementN]
```

----

## 特征

JavaScript 的数组具有以下特征：

1. 数组元素可以是任意数据类型

  比如，可以用数组的第一个位置保存字符串，第二个位置保存数组，第三个位置来保存对象，以此类推。

2. 数组大小可动态调整

  数组长度随着数据的添加可自动增长，以容纳新数据。

----

## 创建数组的方式

有两种方式创建数组，第一种是用 `Array` 构造函数创建数组，第二种是使用数组字面量表示法。

``` none
new Array(element0, element1[, ...[, elementN]])
new Array(arrayLength)
Array(element0, element1[, ...[, elementN]])
Array(arrayLength)
[element0, element1, ..., elementN]
```

### `Array` 构造函数

`new` 操作符后跟 `Array` 构造函数，即可创建一个数组。下面代码创建了一个长度为 0 的数组 `colors`。

``` js
const colors = new Array(); // 构造函数中不传参会创建长度为 0 的数组
```

若 `Array` 构造函数的参数是一个数字，会创建指定长度的数组。比如，下面创建一个长度为 3 的数组 `arr`。在创建数组 `arr` 时，只指定了数组的长度，没有指定数组要保存的内容，所以数组 `arr` 中 3 个元素的值都为 `undefined`。

``` js
const arr = new Array(3);
console.log(arr);
// expected output: Array [ <3 empty items> ]
// arr[0]: undefined; arr[1]: undefined; arr[2]: undefined;
```

如果 `Array` 构造函数的参数类型为除数字类型以外的其他任何类型，则会创建包含这些参数值的数组。下面代码创建了包含 3 个字符串值的数组：

``` js
const names = new Array('Olive', 'Jack', 'Amy');
console.log(names);
// expected output: Array ['Olive', 'Jack', 'Amy']
```

在使用 `Array` 构造函数创建数组时，也可以省略前面的 `new` 操作符：

``` js
const classmates = Array('Amy', 'Tony');
```

### 数组字面量表示法

在实际开发中，数组字面量表示法更常用。数组字面量是由一对包含数组元素的方括号表示，数组元素之间以英文逗号(,)分割。下面代码创建了一个包含 3 个字符串值的数组：

``` js
const colors = ['red', 'green', 'blue'];
```

----

## 数组属性

**`Array.length`**

`Array` 构造函数的属性，其值为 1。该属性为静态属性，不是数组实例的 `length` 属性。

**`Array.prototype`**

通过数组的原型对象可以为所有数组对象添加属性。

----

## 数组方法

**`Array.from()`**

从类数组对象或可迭代对象中创建一个新的数组实例。

**`Array.isArray()`**

用来判断某个变量是否是一个数组对象。

**`Array.of()`**

根据一组参数来创建新的数组实例，支持任意的参数数量和类型。

----

## 数组实例的属性和方法

所有数组实例都会从 `Array.prototype` 继承属性和方法。修改 `Array` 的原型会影响所有数组实例。

### 属性

**`Array.prototype.constructor`**

所有数组实例都继承了这个属性，它的值就是 `Array`，表明所有数组都是由 `Array` 构造出来的。

**`Array.prototype.length`**

因为 `Array.prototype` 也是个数组，而且它是一个空数组，所以 `Array.prototype.length` 值为 0。

### 方法

按照功能，`Array` 数组实例的方法可分为：修改器方法、访问方法和迭代方法。

#### 修改器方法

下面这些方法会改变调用它们的对象自身的值：

**`Array.prototype.copyWithin()`**

**`Array.prototype.fill()`**

[**`Array.prototype.pop()`**](/Global_Objects/Array/pop.html)

[**`Array.prototype.push()`**](/Global_Objects/Array/push.html)

**`Array.prototype.reverse()`**

**`Array.prototype.shift()`**

**`Array.prototype.sort()`**

**`Array.prototype.splice()`**

**`Array.prototyp.unshift()`**

#### 访问方法

下面这些方法绝对不会改变调用它们的对象自身的值，只会返回一个新的数组或返回一个其他的期望值。

**`Array.prototype.concat()`**

**`Array.prototype.includes()`**

**`Array.prototype.join()`**

**`Array.prototype.slice()`**

**`Array.prototype.toString()`**

**`Array.prototype.toLocaleString()`**

**`Array.prototype.indexOf()`**

**`Array.prototype.lastIndexOf()`**

#### 迭代方法

**`Array.prototype.forEach()`**

**`Array.prototype.entries()`**

**`Array.prototype.every()`**

**`Array.prototype.some()`**

**`Array.prototype.filter()`**

**`Array.prototype.find()`**

**`Array.prototype.findIndex()`**

**`Array.prototype.keys()`**

**`Array.prototype.map()`**

**`Array.prototype.reduce()`**

**`Array.prototype.reduceRight()`**

**`Array.prototype.values()`**
