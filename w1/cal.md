# Swift 運算、邏輯


2017/3/23

## 運算子
常見的數值運算有底下這幾種：
加( + )、減( - )、乘( * )、除( / )、餘數( % )
```swift
var a = 1 // 1
var b = 2 // 2
var c = a + b // c = 3
c = c + 1 // 4
c += 1 // c = c + 1 簡寫
10 % 3 // 1
```

## Array
在 Swift 中，一樣有 Array ，寫法如下
```swift
var numbers = [1,2,3,4,5]
numbers[0] // 1
numbers[4] // 5
```
> 在 Array 中，型別必須相同

## For 迴圈
用 For 迴圈可以拜訪集合中的所有元素，比如上面程式的 numbers = [1,2,3,4,5]
```swift
var numbers = [1,2,3,4,5]
for i in numbers{
    print(i)
}
/*
1
2
3
4
5
*/
```
改為下面這樣也有同樣效果
```swift
for i in 1...5{
    print(i)
}
```
迴圈內的變數(上例的i)只有在迴圈內有效，試試看下面這段程式會輸出什麼？
```swift
var i =  10
for i in 1...5{
    print(i)
}
print(i)
```

## IF 條件
if 後面接著一個判斷條件，是 True 的話才會執行
```swift
var score = 59
if score >= 60{
    print("pass")
}
else{
    print("fail")
}
```
因為 score = 59 ， >= (大於或等於) 60 不成立，會執行 else 後方大括號的程式。
> 上面的程式要顯示 `pass` 需要怎麼修改呢？

使用 else if 可以判斷更多的條件，試著分辨出下面的分數：
A 80~100  B 70~80 C 60~70 D 50~60 E 0~50

## SWITCH 條件
條件判斷比較多時，我們會使用 swift
```swift
var score = 30

switch score {
case 80...100:
    print("A")
case 70...79:
    print("B")
case 60...69:
    print("C")
case 50...59:
    print("D")
default:
    print("E")
}

```




