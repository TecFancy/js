# Array.prototype.push()

`push()` 方法将一个或多个元素添加到数组末尾，并返回该数组的新长度。

``` js
const colors = ['red', 'green', 'white'];

const count = colors.push('black');
console.log(count);
// expected output: 4
console.log(colors);
// expected output: Array ['red', 'green', 'white', 'black']

colors.push('gray', 'blue', 'yellow');
console.log(colors);
// expected output: ['red', 'green', 'white', 'black', 'gray', 'blue', 'yellow']
```

----

## 语法

``` js
arr.push(element1, element2, ..., elementN)
```

### 参数

**`elementN`**

被添加到数组末尾的元素。

### 返回值

返回新的 `length` 属性值。

----

## 示例

### 添加元素到数组

下面代码创建了一个包含 2 个字符串元素的数组，随后在它尾部追加了 2 个字符串元素。`total` 变量是数组的新长度值。

``` js
const sports = ['soccer', 'baseball'];
const total = sports.push('football', 'swimming');

console.log(sports);
// expected output: Array ['soccer', 'baseball', 'football', 'swimming']

console.log(total);
// expected output: 4
```

----

## 相关链接

- [Array.prototype.pop()](/Global_Objects/Array/pop.html)
- [Array.prototype.shift()](/Global_Objects/Array/shift.html)
- [Array.prototype.unshift()](/Global_Objects/Array/unshift.html)
- [Array.prototype.concat()](/Global_Objects/Array/concat.html)
