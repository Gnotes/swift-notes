# Swift学习

- [HANKING WHIT SWIFT](https://www.hackingwithswift.com/read)


## 常量 & 变量 & 控制条输出 & 数据类型 & 字符拼接 & 数组 & 字典 & 循环 & 函数

- var 声明变量
```swift
var a = "i am a string"
```

- let 声明常量
```swift
let = 10 # 我不可以修改的哟😀
```

- print 控制台输出
```swift
print("something")
```

- 数据类型

`声明 名称:类型`

一般不写类型，swift会自动转换
```swift
var a:String = "Hello,my first step of swift"
let b:Int = 10
```

- 字符拼接

`+`：加号拼接字符串

```swift
var a = "hello" + ", myself" # hello, myself
```

双引号`""`包裹的字符串中可以使用`\(variable)`的方式拼接字符串
```swift
var str = "learning swift"
var ch1 = 1
var ch2 = 2
var a = "\(str) step by step ,step \(ch1 + ch2)"
```

- 数组

```swift
// 声明并初始化
var arr1 = ["name","age"]
var arr2 = [1,2]

// 存放任意类型数据
var arr3 = [1,"string"] as [Any]
var arr4:[Any] = [1,"string"]

// 声明并指定类型
var songs: [String] = []
var books = [Int]()

// 合并数组 NB的 '+' 号
var songs = ["Shake it Off", "You Belong with Me", "Love Story"]
var songs2 = ["Today was a Fairytale", "Welcome to New York", "Fifteen"]
var both = songs + songs2
// and
both += ["someone like u"]

```

- 字典

var dict = ["age":"10","name":"xing.he"]

- 循环

```swift
for item in 0..100{
    print("output : \(item)") // 输出0到100
}

for value in array{
    print(value) // 输出数组的值
}

for (key ,value) in dict {
    print(key + " : " + value) // 输出字典
}
```

- 函数

```
func name(parameters) -> return type {
    function body
}
```

无返回值
```swift
func sayHi(str:String){
    print("hello \(str) ," + str)
}

sayHi(str: "@me") // hello @me ,@me
```

有返回值，使用`->(类型,类型...)`表示，取值时变量声明也为对应格式`()`
```swift
func getAgeAndHeight(age:Int,height:Float)->(Int,Float){
    return (age,height)
}

var (age,height) = getAgeAndHeight(age: 10, height: 170.2)

print(age) // 10
```

- 类

```
class name: super class {
    code
}
```
类继承需要`:` ，方法覆写需要`override`关键字 ，构造函数为 `init` ， `self`指向当前对象
```
class Hi {
    func sayHi(name:String) {
        print("hello, \(name)")
    }

    func sayGreeting(name:String) {
        print("hello, \(name)")
    }
}

class Hello: Hi {
    var _greet:String

    init(greet:String) {
        self._greet = greet
    }

    override func sayGreeting(name: String) {
        print("\(self._greet)，\(name)")
    }
}


var hi = Hi()
hi.sayHi(name: "xing.he")

var hello = Hello(greet: "你好") // hello, xing.he
hello.sayHi(name: "@me")        // hello, @me
hello.sayGreeting(name: "@me")  // 你好，@me
```
