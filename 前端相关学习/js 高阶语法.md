## js 高阶语法

**数组便利**

```js
1. for in
2. for of
...
```

**高阶函数**

```js
// hadoop mapReduce
1. map
2. reduce
3. filter //过滤器
```

**filter**

```js
ReadonlyArray.filter<S extends T>(predicate: (value: T, index: number, array: readonly T[]) => value is S, thisArg?: any): S[]

A function that accepts up to three arguments. The filter method calls the predicate function one time for each element in the array.
```

**map 内容使用**

```js
ReadonlyArray.map<U>(callbackfn: (value: T, index: number, array: readonly T[]) => U, thisArg?: any): U[]

A function that accepts up to three arguments. The map method calls the callbackfn function one time for each element in the array.
```

**reduce 使用**

```js
arr.reduce(callback(accumulator, currentValue[, index[, array]])[, initialValue])
// init..初始值
```

💡 通过高阶函数多重操作

```js
例如 多个需求
1. 筛选
2. 翻倍...
3. 求和
let Result = arr.filter((value) => {
    return value > 50
      // [111, 222, 333]
    }).map((value) => {
      return value * 2
      // [222, 444, 666]
    }).reduce((preVal, curVal) => {
      return preVal + curVal
      // 1332
    })

```
