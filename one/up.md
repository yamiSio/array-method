- <a href ="#id1"> forEach()遍历数组</a>
- <a href ="#id2"> map()创造新数组</a>
- <a href ="#id3"> new Set()去重</a>
- <a href ="#id4"> reduce()数组累加</a>
- <a href ="#id5"> filter()过滤某些元素</a>
- <a href ="#id6"> some()元素判断是否符合</a>
- <a href ="#id7"> every()所有元素判断是否全都为ture</a>
- <a href ="#id8"> find()是否存在某元素</a>


## <div id="id1">1.forEach</div>
### 遍历数组
### 第一个参数是遍历到的元素，第二个参数才是索引，第三个是数组本身
```
例1:let array = [1, 2, 3, 4, 5, 6, 7];

array.forEach(function (item, index) {

console.log(item); //输出数组的每一个元素

});

例如2:var array=[1, 2, 3, 4, 5];

array.forEach(function(item, index, array){

array[index]=4 * item;

});

console.log(array); //输出结果：修改了原数组元素，为每个元素都乘以4
```

## <div id="id2">2.map()</div>
### 创建一个新的数组,
```
var arry=[1,3,5,7,9]

var after=arry.map(item=>{
  return item*2
})

console.log(after)  //[2,6,10,14,18]
})
```


## <div id="id3">3.new Set()</div>
### 去除数组重复数据。使用拓展运算符
```
例1:
let arr =['vivo','oppo','realme','xiaomi','oppo','vivo'];
let item = new Set(arr);
console.log(item);//结果输出对象{'vivo', 'oppo', 'realme', 'xiaomi'}

//使用Array.from转成数组
let newarr = Array.from(new Set(item ));
console.log(newarr );// ['vivo', 'oppo', 'realme', 'xiaomi']

例2:
let arr =['vivo','oppo','realme','xiaomi','oppo','vivo'];
let newarr= [...new Set(arr)];
console.log(newarr );// ['vivo', 'oppo', 'realme', 'xiaomi']

```

## <div id="id4">4.reduce()</div>
### reduce() 方法接收一个函数作为累加器，数组中的每个值（从左到右）开始缩减，最终计算为一个值。
```
<script>
      var nums = [11, 22, 33, 44, 55]
      // 计算nums数组的元素总和
      let total = 0
      // 缩写规则: 方法体只有一行代码, 可以省略 {return }
      // nums.forEach(value => {
      //   total += value
      // })
 
      // => () 的 () 非必须, 是格式化软件自动加的.
      nums.forEach(value => (total += value))
 
      console.log(total)
 
      // 高阶函数 reduce:  合并数组数据
      // 固定格式:  参数1 (总和变量, 每个元素);
      // 参数2: 总和的初始值
      var r = nums.reduce((total, value) => {
        // 遍历nums数组的每个元素, 触发这里的方法
        // 返回值: 就是新的总和
        return total + value
      }, 0)
    </script>
```
## <div id="id5">5.filter()</div>
### 过滤某些元素
```
在一个Array中，删掉偶数，只保留奇数
var arr = [1, 2, 4, 5, 6, 9, 10, 15];
var r = arr.filter(function (x) {
    return x % 2 !== 0;
});
r; // [1, 5, 9, 15]
```

## <div id="id6">6.some()</div>
### 数组判断
```
是否有负数
const arr = [10,20.50,60,70,80]
const res = arr.some(item => item < 0)
console.log(res)
```

## <div id="id7">7.every()</div>
```
every()是对数组中每一项运行给定函数，如果该函数对每一项返回true,则返回true
every从迭代开始，一旦有一个不符合条件，则不会继续迭代下去。 every() 不会对空数组进行检测
返回布尔值，遇到不满足条件跳出循环
every 一假即假
let arr = [
    {name:'jerry',sex:'man',age:14},
    {name:'jack',sex:'woman',age:19},
    {name:'bill',sex:'man',age:18}
];
let res = arr.every(t => t.age > 17);
console.log(res);

`输出结果：false`

```

## <div id="id8">8.find()</div>
### 寻找函数是否有这个元素 布尔判断
```
let names = ["憨憨卷","花卷","糟老婆子"];
let res = names.find(t => t==='憨憨卷');
console.log(res);

`输出结果： 憨憨卷`

```
