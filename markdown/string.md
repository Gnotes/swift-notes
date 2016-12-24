# String

字符串类型

## 字符串声明

```swift
var str         = "this is a string"
var str1:String = "some string"
var str2        = String("something else")

// 声明一个空串

var str3 = ""
var str4 = String()  // 括号里不传参数
```

## 字符串拼接

- `+`号拼接

```swift
var a = "hello" + ", myself" # hello, myself
```

```swift
var str2 = ""
str2 += "i'm xing.he"

let constant = "Constant string"
str2 += constant                // ❌，常量和变量字符不可拼接
```

- 变量拼接

双引号`""`包裹的字符串中可以使用`\(variable)`的方式拼接字符串
```swift
var str = "learning swift"
var ch1 = 1
var ch2 = 2
var a = "\(str) step by step ,step \(ch1 + ch2)"
```

## 成员变量&方法
- isEmpty 
`String.isEmpty` ：该成员变量判断字符串是否为空，返回true or false    

- characters
`String.characters` ：获取每一个字符    
  
```swift
var str = "abcdef"
for c in str.characters{
  print(c)
}
```

- characters.count
`String.characters.count` ：获取字符长度   

- append
`String.append("+")` ：追加`字符`到string中  

- appendContentsOf
`String.appendContentsOf("哇哈哈😀")` ：追加`字符串`到string中  

- startIndex & endIndex
返回一个`Index`类型的索引对象  
`String.startIndex` ：字符开始位置索引   
`String.endIndex` ：字符结束位置索引   
一个字符索引位置为`前闭后开`的区间`[startIndex,endIndex)`   
`Index.advancedBy(index_number)` 指定索引位置，如:    

```swift
var str         = "hello man"
var startIndex  = str.startIndex                  // 结果为0的索引位置
var str[startIndex]                               // 结果为:h
var index       = startIndex.advancedBy(4)        // 索引位置为4的索引对象，从0开始
str[index]                                        // 结果为:o

index.predecessor()                               // 返回前一个索引位置
index.successor()                                 // 返回后一个索引位置

str[str.endIndex.predecessor()]                   // 结果为:n
```

- insert
`String.insert(String,atIndex:Index)` ：添加字符串到指定位置   

- removeAtIndex
`String.removeAtIndex(Index)` ：删除指定位置字符，返回值为该删除字符   

- uppercaseString & lowercaseString & capitalizedString 
大小写转换

- containsString
`String.containsString(String)` : 是否包含某个字符串,返回true or false

- hasPrefix & hasSuffix
是否包含前后缀

## 字符类型
Character ,不同于其他语言，swift声明字符使用的是双引号`""`，并显示的声明类型为`Charater`

```swift
var ch:Charater = "i"
```
