# Array

JavaScript 的 `Array` 对象是用于构造数组的全局对象，数组是类似于列表的高阶对象。

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
