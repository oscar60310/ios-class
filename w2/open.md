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

3. 接著我們來實作頁面，這個範例中我們使用 `StoryBoard` 來製作，他可以讓你像說故事一樣完成介面設計，不需要打任何的程式，當然也還有其他發法來產生畫面。請按照下圖點選 **Main.storyboard** > **View Controller Scene** > 右方的第三個圖示 identity inspector
![](/assets/w25.png)

4. 一個 ViewController 控制一個畫面，在右方 Custom Class > Class，寫著 ViewController，代表著他受 ViewController.swift 所控制，我們可以按下右方的箭頭前往看看她長什麼樣。
```swift
import UIKit
class ViewController: UIViewController {

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }
}
```
最上面 import UIKit 代表我們會使用 UIKit 這個函式庫，很像 c 的 include 、 C# using 、 Java import 等等

5. 接著有兩個 function ，分別是 viewDidLoad 和 didReceiveMemoryWarnin，看名字應該不難猜到什麼時候會被執行。分別是程式載入後和記憶體警告，值得注意的是前面的 `override` ，我們在剛剛也提過這個詞，在父類別 `UIViewController` 中已經有定義這兩個 function 了，但我們可以取代他，如果沒有到，把兩個 function 都刪掉也沒問題。
> 該怎麼看父類別呢？

6. 我們回到 storyboard 中，找到 Object library，介面的元件都會放在這裡，沒有這個區塊的同學請點選 View > Utilities > show object library。
![](/assets/w26.png)

7. 拉一個 Label 到畫面的中央（顯示藍線），切換到屬性頁面，在 `Text` 的地方打上一些文字。
![](/assets/w27.png)

8. 修改其他屬性，讓文字看起來長得好看些。
![](/assets/w28.png)

9. 接著拉出一個 button 放在字的底下
![](/assets/w29.png)

所有的屬性都可以在右方找到喔，大家可以看看還有哪些東西可以修改，改壞了頂多刪掉重拉而已。