# Array

JavaScript 的 `Array` 对象是用于构造数组的全局对象。JavaScript 的 `Array` 具有以下特征：

1. 数组元素可以是任何类型。比如，可以用数组的第一个位置保存字符串，第二个位置保存数组，第三个位置来保存对象，以此类推。
2. 数组大小可动态调整。数组长度随着数据的添加可自动增长，以容纳新数据。

**创建数组**

``` js
const colors = ['red', 'green'];
// colors.length: 2
```

**通过索引访问数组元素**

``` js
const colors = ['red', 'green'];

const firstColor = colors[0];
// firstColor: red

const lastColor = colors[colors.length - 1];
// lastColor: green
```

**遍历数组**

``` js
const colors = ['red', 'green'];

colors.forEach((colorItem, colorIndex, array) => {
  console.log(colorItem, colorIndex);
});
// red 0
// green 1
```

**添加元素到数组末尾**

``` js
const colors = ['red', 'green'];

const newLength = colors.push('gray');
// newLength: 3
// colors: ['red', 'green', 'gray']
```

**删除数组末尾的元素**

``` js
const colors = ['red', 'green'];

const last = colors.pop();
// last: 'green'
// colors: ['red']
```

**添加元素到数组的头部**

``` js
const colors = ['red', 'green'];

const newLength = colors.unshift('blue');
// newLength: 3
// colors: ['blue', 'red', 'green']
```

**删除数组最前面（头部）的元素**

``` js
const colors = ['red', 'green'];

const first = colors.shift();
// first: 'red'
// colors: ['green']
```

**找出某个元素在数组中的索引**

``` js
const colors = ['red', 'green'];

colors.push('white');
// colors: ['red', 'green', 'white']

const pos = colors.indexOf('green');
// pos: 1
```

**通过索引删除某个数组元素**

``` js
const colors = ['red', 'green', 'white'];
const pos = colors.indexOf('green');

var removedItem = colors.splice(pos, 1);
// removedItem: ['green']
// colors: ['red', 'white']
```

**从一个索引位置删除多个数组元素**

``` js
const colors = ['red', 'green', 'white', 'gray'];
const pos = 1, n = 2;

// 从指定位置删除指定数量的数组元素
// pos 定义了从数组的哪个位置开始删除，n 定义了要删除的数组数量
const removedItems = colors.splice(pos, n);
// removedItems: ['green', 'white']
// colors: ['red', 'gray']
```

**复制一个数组**

``` js
const colors = ['red', 'green'];
const shallowCopy = colors.slice(); // 潜复制
// shallowCopy: ['red', 'green']
```

----

## 语法

创建数组的方式有两种，第一种是使用 `Array` 构造函数。如下代码所示：

``` js
const colors = new Array();
// colors: []
// colors.length: 0
```

上面代码会创建一个长度为 0 的空数组 `colors`。如果预先知道要保存的项目数量，也可以给构造函数传递该参数，该数量会自动变成 `length` 属性的值。代码如下：

``` js
const colors = new Array(3);
// colors: [ <5 empty items> ]
// colors.length: 5
```

也可以向 `Array` 构造函数传递数组应该包含的项。以下代码创建了一个包含 3 个字符串值的数组：

``` js
const colors = new Array('red', 'green', 'blue');
// colors: ['red', 'green', 'blue']
// colors.length: 3
```

如果给构造函数传递一个值的话，虽然也可以创建数组，但是却要复杂一些。因为如果传递的是数值，则会按照数值创建包含给定项的数组；而如果传递的是其他类型的参数，则会创建包含那个值的只有一项的数组。下面代码说明了这两种情况：

``` js
const colors = new Array(3); // 创建一个包含 3 个元素的数组
// colors: [ <3 empty items> ]
// colors.length: 3

const names = new Array('Olive'); // 创建一个包含 1 个元素的数组
// names: ['Olive']
// names.length: 1
```

在使用 `Array` 构造函数创建数组时，可以省略 `new` 操作符。比如下面的例子，省略 `new` 操作符的结果与上面代码的结果相同：

``` js
const colors = Array(3);
// colors: [ <3 empty items> ]
// colors.length: 3

const names = Array('Olive');
// names: ['Olive']
// names.length: 1
```

创建数组的第二种方式是使用数组字面量表示法。数组字面量是由一对包含数组元素的方括号表示，数组元素之间用逗号（,）隔开：

``` js
const colors = ['red', 'green', 'white']; // 创建一个包含 3 个字符串的数组
const names = []; // 创建一个空数组
```

总结起来，创建数组的语法如下：

``` none
new Array(element0, element1[, ...[, elementN]])
new Array(arrayLength)
Array(element0, element1[, ...[, elementN]])
Array(arrayLength)
[element0, element1, ..., elementN]
```

----

## 属性

**`Array.length`**

`Array` 构造函数的属性，其值为 1。该属性为静态属性，不是数组实例的 `length` 属性。

**`Array.prototype`**

通过数组的原型对象可以为所有数组对象添加属性。

----

## 方法

**`Array.from()`**

从类数组对象或可迭代对象中创建一个新的数组实例。

**`Array.isArray()`**

用来判断某个变量是否是一个数组对象。

**`Array.of()`**

根据一组参数来创建新的数组实例，支持任意的参数数量和类型。

----

## 数组实例

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

**`Array.prototype.push()`**

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
