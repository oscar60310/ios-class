# Swift 入門

2017/3/23

## 關於

在 iOS 程式可以使用 Objective-C 或 Swift 來做開發，這系列的課程會使用 swift 為主。他是一個新的程式預言，對程式新手來說是非常友善且容易學習的，下面我們會介紹他基本的邏輯，並在 playground 或其他平台上實作。

## 宣告

和其他語言一樣，在使用之前需要先宣告，我們可以利用 `var`\(變數\) 和 `let`\(常數\) 來達成目標，常數顧名思義只能設定一次。

```swift
var a = 0
a = 2
let b = 3
b = 4 // err 
```
所有的宣告都是使用var或let，那要如何決定型別呢?
編譯器會在宣告的時候自動判定型別，也可以在宣告後面加上冒號說明。
```swift
var a = 0 // int 整數
var pi = 3.1415926 // Double 浮點數 小數
var b: Double = 3 // Double
var dream = false // Bool 布林值 true 或 false
var s = "hello world" // String 字串
```
在 Swift 中，大概有這幾種型別，使用時有幾點必須注意
- 宣告變數時，要給一個初始值，下方這段程式無法成功編譯
```swift
var a
a = 1
```
- 不能改變型別
```swift
var s = "hello world" // String
s = "Hi!" // 可以執行，因為同樣是 String
s = 1234 // 無法執行
```



