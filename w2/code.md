# 程式部分
2017/3/30

到目前為止你應該完成一個 Label 和 Button，接著我們開始程式部分
## 元件連結
我們在 storyboard 上畫了兩個元件，要怎麼讓程式知道他們在哪呢？

1. 點選右上角的 `show assitant`，他會顯示 storyboard 和 swift 檔案，沒有的話請自己把 viewcontroller.swift 拉過去。如果覺得畫面有點擠的話，可以點圖中２的部分，暫時把列表收起來。
![](/assets/w210.png)

2. 接著點選你的文字，按住 Ctrl(option)，往右拉，拉到 Class 裡面。
![](/assets/w11.png)
> 雖然說拉到 class 任一個地方都可以，但元件多時很容應找不到他，建議各位把定義的部分放到最上面

3. 幫這個元件取個名字，這個名字是是程式中要使用的，不可以是系統保留字，按下 connect 後就可以了。
![](/assets/w12.png)

4. 接著換拉 button ，要注意的是我們不是要定義 button ，而是想要定義 button 按下去後的動作，所以要把上面的 Connection 改為 `Action`
![](/assets/w13.png)

5. 完成後的程式應該長這樣，左方黑點點會說明連結的資料。
![](/assets/w14.png)  

6. 我們想要按下按鈕後（會呼叫 btnClick 函式），文字（我們訂為 textShow）改變，程式如下
```swift
@IBOutlet weak var textShow: UILabel!
@IBAction func btuClick(_ sender: Any) {
    textShow.text = "Hi iOS"
}
```
7. 這樣我們的程式就大功告成了!按下左上方播放鍵就可以開始建置和執行囉，你可以在後面選擇模擬器裝置，或是插上你的 iPad ，開啟開發人員模式，直接在上面執行。
![](/assets/w15.png)
![](/assets/w16.png)

## 練習
現在的範例是按一次按鈕後轉換文字，請設計看看再按一次按鈕回到原本的文字