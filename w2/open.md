# 第一個專案
2017/3/30
## 開啟專案
1. 點選起始畫面的 **Create a new Xcode project**。沒有起始畫面的同學可以點選 File > New > Project。
![](/assets/w21.png)
2. 選擇 iOS 頁籤下的 Single View Application。
![](/assets/w22.png)
3. 填寫專案的相關資訊，Language 選擇 **Swift**，Device 選擇 **Universal**。
> Universal 能讓我們同時開發 iphone 和 iPad 的介面，但同時要考慮的事情也變多囉

![](/assets/w23.png)
## 實作頁面
1. 開啟專案以後，大家應該可以看到跟下圖很像的介面，右上方（綠色部分）能讓你開啟／關閉區域。
![](/assets/w24.png)
> 為了方便教學，可以的話麻煩把左右區域打開，下方 debug area 關閉

2. 我們先來看看 `AppDelegate.swift` 這個檔案，這裡定義了程式開啟時要載入哪個頁面，程式關閉時要做什麼等等，全部都是以 func 形式表現。比如說下面這段
```swift
func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
        // Override point for customization after application launch.
        return true
 }
 ```
當程式開啟時就會呼叫這個 function ，如果你要修改進入頁面的話，可以在這裡 Override 他。
> 有看到 func 中參數部分前面有個底線嗎？ 猜猜看那代表什麼

3. 接著我們來實作頁面，這個範例中我們使用 `StoryBoard` 來製作
![](/assets/w25.png)