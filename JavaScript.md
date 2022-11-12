# 第一部分 基本的JavaScript

# 第二部分 ES6

## 1.比较var的范围和let关键字

## 2.改变一个用const声明的数组

## 3.防止对象突变

```javascript
//通过之前的挑战可以看出，const 声明并不会真的保护数据不被改变。 为了确保数据不被改变，JavaScript 提供了一个函数 Object.freeze。

任何更改对象的尝试都将被拒绝，如果脚本在严格模式下运行，将抛出错误。
let obj = {
  name:"FreeCodeCamp",
  review:"Awesome"
};
Object.freeze(obj);
obj.review = "bad";
obj.newProp = "Test";
console.log(obj); 
```

## 4. 使用箭头函数编写简洁的匿名函数

```javascript
const myFunc = function() {
  const myVar = "value";
  return myVar;
}

const myFunc = () => {
  const myVar = "value";
  return myVar;
}

const myFunc = () => "value";
```

