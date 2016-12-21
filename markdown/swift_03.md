# Swift学习

- [HANKING WHIT SWIFT](https://www.hackingwithswift.com/read)

## 区间运算符

- 闭区间运算符

`[a,b]` 取值在a到b之间，包括a,b ; `a...b`  

- 开区间运算符

`[a,b)` 取值在a到b之间，包括a,不包括b ; `a..<b`  

## 循环

- for in

`{}` 是必须的，即使只有一条循环体语句  
循环变量`index`是一个`常量`，不能修改:可以理解为每次循环都声明了一个常量叫`index` 并把循环值赋给了它  

```swift
for index in 1...100{ // 循环1...100
  print(index)
}

for index in 1..<100{ // 循环1...99
  print(index)
}
```

- for 

**continue & break**

```swift
for var i = 0; i < 100; i++{
  if i == 4 {
    continue
  }

  print(i)

  if i == 9 {
    break
  }
}
```

- while

```swift
var i = 0;
while i < 10{
  if i == 4 {
    continue
  }

  print(i)

  if i == 9 {
    break
  }
  i++
}
```

- repeat

**类似do while, do 关键字被占用，使用repeat替代**

```swift
var i = 0
repeat{
  print(i)
}while i < 0
```

- continue 或 break 指定循环

**传统方式**

```swift
var flag = false
for i in 1...100{
  for index in 1...100{
    if index == 10{
      flag = true
      break
    }
  }
  if flag{
    break
  }
}
```

**新技能**

```swift
breakHere : for i in 1...100{ // 给循环声明一个名称
  for index in 1...100{
    if index == 10{
      break breakHere         // 跳出指定名称的循环
    }
  }
}
```

## switch

**不需要显示书写break**
**不能枚举所有case时，default是必须的**
**执行空语句时可以书写`break`或`()`**
**fallthrough关键字：执行完当前case后并执行下一个case**

```swift
var i = 60
switch i{
  case 0,1:       // 0和1都匹配的值都会进入这个case
    code here
  case 2..10:     // 2到10的匹配进入

  case 11..<60:   // 11到小于60的匹配进入

  default:        // 其他case
    break
}
```

```swift
var i = 1
switch i{
  case 1:         // fallthrough
    print(1)
    fallthrough
  case 2:         
    print(2)
  case 2:

  default:
    break
}

// 执行结果为：
1 
2
```

**where关键字指定case条件**

```swift
var point = (1,1)
switch i{
  case let (x,y) where x == y:
    code here
  case let (x,y) where x == -y:
    code here
  case let (x,y):
    ()
}
```




