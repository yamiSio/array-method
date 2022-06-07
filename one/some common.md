- <a href ="#id1"> push()组尾添加</a>
- <a href ="#id2"> pop()组尾删除</a>
- <a href ="#id3"> shift()删除第一些</a>
- <a href ="#id4"> unshift()添加第一项</a>
- <a href ="#id5"> slice()查找内容</a>
- <a href ="#id5.5"> split() 把一个字符串分割成字符串数组</a>
- <a href ="#id6"> splice()对数组进行增删改</a>
- <a href ="#id7"> join()用指定的分隔符将数组每一项拼接为字符串</a>
- <a href ="#id8"> concat()用于连接两个或多个数组</a>
- <a href ="#id9"> indexOf()检测当前值在数组中第一次出现的位置索引</a>
- <a href ="#id10"> lastIndexOf()检测当前值在数组中最后一次出现的位置索引</a>
- <a href ="#id11"> includes()判断一个数组是否包含一个指定的值</a>
- <a href ="#id12"> sort()对数组的元素进行排序</a>
- <a href ="#id13"> reverse()对数组倒叙输出</a>
## <div id="id1"> 1.push()</div>
#### 向数组向数组的末尾添加新内容
### 可以添加如何数据类型
```
let ary1 = [12,34,26];

ary1.push(100); //返回一个新的长度 

console.log(ary1)//结果为 [12,34,26,100]
```

## <div id="id2">2.pop()</div>
### 删除数组的最后一项
```
let arry2=[12,34,26];

arry2.pop();

console.log(arr2)  //结果[12,34]
```

## <div id="id3">3.shift()</div>
### 删除数组的第一项
```
let arry3=[12,34,26];

arry2.shift();

console.log(arry3)  //结果[34,26]
```

## <div id="id4">4.unshift()</div>
### 新增到数组的首位
```
let arry4=['a','b'];

arry4.unshift('c','d');

console.log(arry4)  //结果['c','d','a','b']
```

## <div id="id5">5.slice()</div>
###  查找内容
### array.slice(n, m)，从索引n开始查找到m处（不包含m）
### array.slice(n) 第二个参数省略，则一直查找到末尾
### array.slice(0)原样输出内容，可以实现数组克隆
### array.slice(-n,-m) slice支持负参数，从最后一项开始算起，-1为最后一项，-2为倒数第二项
### 返回值：返回一个新数组
### 是否改变原数组：不改变
```
let ary5 = [1,2,3,4,5,6,7,8,9]; 

//console.log(ary5.slice(2,8));//从索引2开始查找到索引为8的内容，结果为[3, 4, 5, 6, 7, 8] 

//console.log(ary5.slice(0));  //复制原数组

console.log(ary5.slice(-2,-1));//[8]
```

## <div id="id5.5">5.5.split()
## 把一个字符串分割成字符串数组
 ```
var str="How are you doing today?";
var n=str.split(" ");  //How,are,you,doing,today?
 可以使用limit限制
var str="How are you doing today?";
var n=str.split(" ",3);  //How,are,you
  
 ```

## <div id="id6">6.splice()</div>
### 对数组进行增删改
### 增加：ary.splice(n,0,m)从索引n开始删除0项，把m或者更多的内容插入到索引n的前面
### 返回空数组
### 修改：ary.splice(n,x,m)从索引n开始删除x个，m替换删除的部分
### 把原有内容删除掉，然后用新内容替换掉
### 删除：ary.splice(n,m) 从索引n开始删除m个内容
### （如果第二个参数省略，则从n删除到末尾）
### 返回删除的新数组，原有数组改变
```
//增加

  let ary6_z = [33,44,55,66,77,88];

  ary6_z.splice(2,0,'a','b')

  console.log(ary6_z);// [33, 44, "a", "b", 55, 66, 77, 88]

 
  //修改

  let ary6_x = [33,44,55,66,77,88];

  ary6_x.splice(1,2,'x','y')

  console.log(ary6_x);// [33, "x", "y", 66, 77, 88]

 
  //删除

   let ary6_s = [33,44,55,66,77,88];

   //console.log(ary6.splice(3,2))//[66, 77]

   console.log(ary6_s.splice(3));//[66, 77, 88]
```

## <div id="id7">7.join()</div>
### 用指定的分隔符将数组每一项拼接为字符串
### 参数：指定的分隔符（如果省略该参数，则使用逗号作为分隔符）
### 返回值：拼接好的字符串
### 是否改变原数组：不改变
```
let ary7 = [1,2,3];

console.log(ary7.join('、'));//1、2、3
```

## <div id="id8">8.concat()</div>
### 用于连接两个或多个数组
### 返回新的数组
```
let ary8 = ['你'];

let ary80 = ary8.concat('好');

console.log(ary80);//["你", "好"]
```

## <div id="id9">9.indexOf()</div>
### 检测当前值在数组中第一次出现的位置索引
### 返回值：第一次查到的索引，未找到返回-1
```
let ary9 = ['a','b','c','d','e','a','f'];   

console.log(ary9.indexOf('c'));//2

console.log(ary9.indexOf('a',3))//5
```

## <div id="id10">10.lastIndexOf()</div>
### 检测当前值在数组中最后一次出现的位置索引
### 返回值：最后一次查到的索引，未找到返回-1

## <div id="id11">11.includes()</div>
### 判断一个数组是否包含一个指定的值
```
let ary11 = ['a','b','c','d']; 

console.log(ary11.includes('c'));//true

console.log(ary11.includes(2));//false
```

## <div id="id12">12.sort()</div>
### 对数组的元素进行排序（默认是从小到大来排序 并且是根据字符串来排序的）
```
let ary12 = [32,44,23,54,90,12,9]; 

  ary12.sort(function(a,b){        // return a-b;  // 结果[9, 12, 23, 32, 44, 54, 90]

       // return b-a;  // 结果[90, 54, 44, 32, 23, 12, 9]   })  

   console.log(ary12);
```

## <div id="id13">13.reverse()</div>
### 把数组倒过来排列
```
let ary13 = [6,8,10,12]; 

console.log(ary13.reverse());//[12, 10, 8, 6]
```
