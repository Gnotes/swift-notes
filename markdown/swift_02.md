# Swift学习

- [HANKING WHIT SWIFT](https://www.hackingwithswift.com/read)

**不同类型值进行运算需要强转**

```swift
var left = 3.14
var right = 3

var middle = left + right // 报错❌

var middle = left + Double(right)
```

- 布尔类型
**只有true 和 false**
```swift
let omg      = true
let lgd:Bool = false
```

**一般0代表false，非0代表true，但在swift中这样是不行的🚫**

- if else 条件语句

```swift
if omg {
  print("I'm true")
}else if 4 > 3 {
  print("I'm true too")
}else{
  print("I'm false")
}
```
判断条件可以不使用`()`包裹  
表达式语句必须使用`{}`包裹，即使只有一条语句

- 元组数据类型

类似C++中的结构体吧！  

**特点**  容纳 `多个` `不同类型` 的值  
```swift
var point = (10,20)                             // 多个值使用逗号(,)分隔
var http:(Int , String) = (200,"success")       // 显示指定元组数据类型

// 命名元组
var location(x:Int,y:Int) = (10,20)             // 指定类型&指定值得名称
var me:(Int, String) = (age:25,name:"xing.he")  // 指定类型&指定值得名称

// 获取元祖的值

// 解构方式
var (statusCode, message) = http                // 使用类似JS-es6语句解构方式获取值，es6中使用{}，swift使用()

// 下标方式获取值
var x = point.0   // x = 10
var y = point.1   // y = 20

// 命名元组获取
var x = location.x
var y = location.y

var age  = me.age
var name = me.name

```