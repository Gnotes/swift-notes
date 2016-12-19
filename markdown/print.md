# print

**控制台打印输出函数**

- 直接打印String

```swift
print("i am a string")
```
- 多个值打印

```swift
var a = 1, b = 2, c = "hello";
print(a, b, c)                 // 1 2 hello 输出之间使用空格隔开
```

- 指定分隔符输出
```swift
var a = 1, b = 2, c = "hello";
print(a, b, c, separator:"|")  // 1|2|hello 输出之间使用|分隔 ，需要使用 separator:"something" 指定
```

- 指定结束符输出
```swift
var a = 1, b = 2, c = "hello";
print(a, b, c, separator:"|", terminator:"&")  // 1|2|hello& 输出结束使用&表示 ，需要使用 terminator:"something" 指定,默认结束符是 “回车”
```

- 字符串值变量插入
```swift
var name = "xing.he"
print("hello \(name)")    // 双引号包裹的字符串可以使用 `\()`插入变量
```
