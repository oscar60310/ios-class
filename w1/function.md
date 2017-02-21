# 函式
2017/3/23

當程式有重複的功能被使用時，我們可以寫成函式 Function 的形式，如下面範例
```swift
func sayHI(Name: String){
    print("HI " + Name)
}
sayHI(Name: "Blob")
sayHI(Name: "Cindy")
/*
HI Blob
HI Cindy
*/
```
上面程式中，我們定義了 sayHI 這個函式名稱，說明使用函式必須傳入 `Name` 這個 String。

## 回傳 Return
函式可以回傳值給呼叫的城市，例如下方的函式會將兩數相加。
```swift
func add(a: Int,b: Int) -> Int {
    return a + b
}
print(add(a: 3,b: 4))
```
首先我們定義此函數需要兩個傳入值 `a` 和 `b` ，並說明回傳一個 Int，所以當其他程式呼叫並傳入3和4時，會得到回傳值 7

> 試試看將剛剛的成績轉換寫為函數

```swift
func grade(score: Int) -> String{
    // ....
}
```
## Tuples
Swift 把任意數值組合起來，在函式回傳中非常好用！