# Array.isArray()

`Array.isArray()` 用于确定传递的值是否是一个 [`Array`](/Global_Objects/Array/)。

``` js
Array.isArray([1, 2, 3]); // true
Array.isArray({name: 'Olive'}); // false
Array.isArray('baseball'); // false
Array.isArray(undefined); // false
```

----

## 语法

``` js
Array.isArray(value)
```

### 参数

**`value`** - 需要检测的值。

### 返回值

如果被检测的值是 `Array` 则返回 `true`，否则返回 `false`。

----

## 相关链接

- [`Array`](./)
