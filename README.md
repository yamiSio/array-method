##  Object.assign()  浅拷贝
#### 一般也应用于input里的值显示，当input用对话框进行修改时
#### 点取消同样会将input修改的值复制过去.这里用浅拷贝，只有当确认时才会拷贝input的值过去
```
let aaa = {
 text: 2,
 value: 11,
}

let bbb = {
  text: 3
}

let ccc = Object.assign(aaa,bbb) // aaa目标对象, bbb源对象(将bbb拷给aaa)

console.log(aaa)   //{text3,value:11}
console.log(bbb)   //{text3}
console.log(ccc)   //{text3,value:11}

```

## 验证是否为中文
```
function isChinese(str) {
  const re = /^[\u4e00-\u9fa5]+$/;
  return re.test(str);
}
```

