# Array.prototype.pop()

`pop()` 方法从数组中删除最后一个元素，并返回被删除的元素。该方法会改变数组的长度。

``` js
const colors = ['red', 'green', 'white'];

console.log(colors.pop());
// expected output: 'white'

console.log(colors);
// expected output: Array ['red', 'green']

colors.pop();

console.log(colors);
// expected output: Array ['red']
```

----

## 语法

``` js
arr.pop()
```

### 返回值

从数组中删除的最后一个元素（当数组为空时，返回 `undefined`）。

----

## 描述

`pop()` 方法从一个数组中删除并返回最后一个元素。

`pop()` 方法会根据 `length` 属性来确定数组尾部元素的位置。如果不包含 `length` 属性或 `length` 属性不能被转换成一个数值，会将 `length` 置为 0，并返回 `undefined`。

在一个空数组上调用 `pop()` 方法返回 `undefined`。

----

## 示例

下面代码首先创建了一个包含 4 个字符串元素的数组 `colors`，随后删掉它最后一个元素。

``` js
const colors = ['red', 'green', 'blue', 'white'];
const popped = colors.pop();

// colors: ['red', 'green', 'blue']
// popped: 'white'
```

----

## 相关链接

- [Array.prototype.push()](/Global_Objects/Array/push.html)
- [Array.prototype.shift()](/Global_Objects/Array/shift.html)
- [Array.prototype.unshift()](/Global_Objects/Array/unshift.html)
- [Array.prototype.concat()](/Global_Objects/Array/concat.html)
- [Array.prototype.splice()](/Global_Objects/Array/splice.html)
