# 第一部分 基本的JavaScript

## 1. 介绍

### 1.1 检查数据类型

要检查某个变量的数据类型，我们使用**typeof**运算符。请参见以下示例。

```javascript
console.log(typeof 'Asabeneh') // string
console.log(typeof 5) // number
console.log(typeof true) // boolean
console.log(typeof null) // object type
console.log(typeof undefined) // undefined
```

## 2. 数据类型

### 2.1 数据类型

#### 2.1.1 原始数据类型

1. 数字 - 整数、浮点数
2. 字符串 - 单引号、双引号或反引号下的任何数据
3. 布尔值 - 真值或假值
4. Null - 空值或无值
5. 未定义 - 声明的变量没有值
6. Symbol - 可以由 Symbol 构造函数生成的唯一值

#### 2.1.2 非原始数据类型

1. 对象
2. 数组

### 2.2 数字

#### 2.2.1 声明数字类型

#### 2.2.2 数学对象

```javascript
const PI = Math.PI

console.log(PI)                            // 3.141592653589793

// Rounding to the closest number
// if above .5 up if less 0.5 down rounding

console.log(Math.round(PI))                // 3 to round values to the nearest number

console.log(Math.round(9.81))              // 10

console.log(Math.floor(PI))                // 3 rounding down

console.log(Math.ceil(PI))                 // 4 rounding up

console.log(Math.min(-5, 3, 20, 4, 5, 10)) // -5, returns the minimum value

console.log(Math.max(-5, 3, 20, 4, 5, 10)) // 20, returns the maximum value

const randNum = Math.random() // creates random number between 0 to 0.999999
console.log(randNum)

// Let us  create random number between 0 to 10

const num = Math.floor(Math.random () * 11) // creates random number between 0 and 10
console.log(num)

//Absolute value
console.log(Math.abs(-10))      // 10

//Square root
console.log(Math.sqrt(100))     // 10

console.log(Math.sqrt(2))       // 1.4142135623730951

// Power
console.log(Math.pow(3, 2))     // 9

console.log(Math.E)             // 2.718

// Logarithm
// Returns the natural logarithm with base E of x, Math.log(x)
console.log(Math.log(2))        // 0.6931471805599453
console.log(Math.log(10))       // 2.302585092994046

// Returns the natural logarithm of 2 and 10 respectively
console.log(Math.LN2)           // 0.6931471805599453
console.log(Math.LN10)          // 2.302585092994046

// Trigonometry
Math.sin(0)
Math.sin(60)

Math.cos(0)
Math.cos(60)
```

###### 2.2.2.1 随机数发生器

```javascript
//JavaScript 数学对象有一个 random() 方法数字生成器，它生成从 0 到 0.999999999 的数字......

let randomNum = Math.random() // generates 0 to 0.999...

//现在，让我们看看如何使用 random() 方法生成 0 到 10 之间的随机数：

let randomNum = Math.random()         // generates 0 to 0.999
let numBtnZeroAndTen = randomNum * 11

console.log(numBtnZeroAndTen)         // this gives: min 0 and max 10.99

let randomNumRoundToFloor = Math.floor(numBtnZeroAndTen)
console.log(randomNumRoundToFloor)    // this gives between 0 and 10
```

### 2.3 字符串

#### 2.3.1 字符串连接

```javascript

```



###### 1. 使用加法运算符连接

###### 2. 长文字串

###### 3. 字符串中的转义序列

```javascript
\n: 换行
\t：制表符，表示8个空格
\\: 反斜杠
\'：单引号 (')
\": 双引号 (")

```



###### 4. 模板文字（模板字符串）

```javascript
//要创建模板字符串，我们使用两个反引号。我们可以将数据作为表达式注入模板字符串中。为了注入数据，我们用大括号 ({}) 将表达式括起来，前面是 $ 符号。请参阅下面的语法。

console.log(`The sum of 2 and 3 is 5`)              // statically writing the data
let a = 2
let b = 3
console.log(`The sum of ${a} and ${b} is ${a + b}`) // injecting the data dynamically
```



#### 2.3.2  字符串方法

```javascript
//length：字符串长度方法返回字符串中包含空格的字符数。

//访问字符串中的字符

//toUpperCase()：此方法将字符串更改为大写字母

//toLowerCase()：此方法将字符串更改为小写字母。

//substr()：它有两个参数，起始索引和要切片的字符数

//substring()：它有两个参数，起始索引和停止索引，但它不包括停止索引处的字符

//split()：split 方法在指定位置拆分字符串。

//trim()：删除字符串开头或结尾的尾随空格。

//includes()：它接受一个子字符串参数，并检查字符串中是否存在子字符串参数。includes()返回一个布尔值。如果字符串中存在子串，则返回真，否则返回假。

//replace()：将旧子字符串和新子字符串作为参数。

//charAt()：采用索引并返回该索引处的值

//charCodeAt()：采用索引并返回该索引处值的字符代码（ASCII 数字）

//indexOf()：获取一个子字符串，如果该子字符串存在于字符串中，则返回该子字符串的第一个位置，如果不存在，则返回 -1

//lastIndexOf()：获取一个子字符串，如果子字符串存在于字符串中，则返回子字符串的最后位置，如果不存在，则返回 -1

//concat()：它需要很多子字符串并将它们连接起来。

//startsWith：它接受一个子字符串作为参数，并检查字符串是否以指定的子字符串开头。它返回一个布尔值（真或假）。

//endsWith：它接受一个子字符串作为参数，并检查字符串是否以指定的子字符串结尾。它返回一个布尔值（真或假）。

//搜索：它接受一个子字符串作为参数，并返回第一个匹配项的索引。搜索值可以是字符串或正则表达式模式。

let string = 'I love JavaScript. If you do not love JavaScript what else can you love.'
console.log(string.search('love'))          // 2
console.log(string.search(/javascript/gi))  // 7

//match：它以子字符串或正则表达式模式作为参数，如果匹配则返回一个数组，否则返回 null。让我们看看正则表达式模式是什么样的。它以 / 符号开始并以 / 符号结束。
let string = 'I love JavaScript. If you do not love JavaScript what else can you love.'
console.log(string.match('love'))
//["love", index: 2, input: "I love JavaScript. If you do not love JavaScript what else can you love.", groups: undefined]

repeat()：它接受一个数字作为参数，并返回字符串的重复版本。
let string = 'love'
console.log(string.repeat(10)) // lovelovelovelovelovelovelovelovelovelove
```

### 2.4 检查数据类型和转换

#### 2.4.1 检查数据类型

#### 2.4.2 更改数据类型（转换）

转换：将一种数据类型转换为另一种数据类型。我们使用

```javascript
*parseInt()*、*parseFloat()*、*Number()*、*+ sign*、*str()*
```

 当我们进行算术运算时，字符串数字应该首先转换为整数或浮点数，否则返回错误

###### 1. 字符串转整数

```javascript
//我们可以将字符串数字转换为数字。引号内的任何数字都是字符串数字。字符串数字的示例：'10'、'5'等。我们可以使用以下方法将字符串转换为数字:

解析整数()
数字（）
加号 (+)
let num = '10'
let numInt = parseInt(num)
console.log(numInt) // 10
let num = '10'
let numInt = Number(num)

console.log(numInt) // 10
let num = '10'
let numInt = +num

console.log(numInt) // 10
    
```



###### 2. 要浮动的字符串

```javascript
//我们可以将字符串浮点数转换为浮点数。引号内的任何浮点数都是字符串浮点数。字符串浮点数的示例：'9.81'、'3.14'、'1.44'等。我们可以使用以下方法将字符串浮点数转换为数字：
//解析浮点数()
//数字（）
//加号 (+)

let num = '9.81'
let numFloat = parseFloat(num)

console.log(numFloat) // 9.81
let num = '9.81'
let numFloat = Number(num)

console.log(numFloat) // 9.81
let num = '9.81'
let numFloat = +num

console.log(numFloat) // 9.81

```



###### 3. 浮点数到整数

```javascript
//我们可以将浮点数转换为整数。我们使用以下方法将 float 转换为 int：

let num = 9.81
let numInt = parseInt(num)

console.log(numInt)
```

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

