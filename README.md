# swift_snippet

## Animate
```swift
UIView.animate(withDuration: 0.5, animations: {
            
}, completion: { result -> Void in

})
```

## Data <-> String
```swift
var testString = "This is a test string"
var somedata = testString.data(using: String.Encoding.utf8) // String to Data
var backToString = String(data: somedata!, encoding: String.Encoding.utf8) as String! // Data to String
```

## Int <-> String
```swift
String(myInt) // Int to String
Int(myString) // String to Int
```

## for each subviews
```swift
for subview in view.subviews {
    ...
}
```

## String to Date
```swift
let formatter = DateFormatter()
formatter.dateFormat = "yyyy MM dd"
formatter.timeZone = Calendar.current.timeZone
formatter.locale = Calendar.current.locale

let date = formatter.date(from: "2018 06 01")!
```

## Date to String
```swift
let formatter = DateFormatter()
let startDate = Date()
let dateString = formatter.string(from: startDate)
```

## Label 加底線
```swift
label.attributedText = NSAttributedString(string: "Text", attributes:
    [.underlineStyle: NSUnderlineStyle.styleSingle.rawValue])
```    

## 取得螢幕寬度
```
UIScreen.main.bounds.width
```

## NavigationController 回前一頁
```
self.navigationController?.popViewController(animated: true)
```

## NavigationController 隱藏/顯示
```
self.navigationController?.navigationBar.isHidden = true
```

## TabbarController 隱藏/顯示
```
self.tabBarController?.tabBar.isHidden = true
```

## 離開此頁將 tabbar or Navigation 設定隱藏/顯示
```
override func viewWillDisappear(_ animated: Bool) {
        super.viewWillDisappear(animated)
        
        if self.isMovingFromParentViewController {
            self.tabBarController?.tabBar.isHidden = false
            self.navigationController?.navigationBar.isHidden = false
        }
    }
```    

## 快速設定 constraints
```
let webCons = webView.constraints.first { $0.identifier == "webViewHeight" }
webCons?.constant = newHeight
```

## 設定 statusBar 顏色
```
// MARK: - 設定 statusBar 顏色
override var preferredStatusBarStyle: UIStatusBarStyle {
    return UIStatusBarStyle.lightContent
}
```

## Navigation Controller 設定下一頁 back 的文字(在前一個 ViewController 內設定)
```
override func prepare(for segue: UIStoryboardSegue, sender: Any?) {
    let backItem = UIBarButtonItem()
    backItem.title = ""
    navigationItem.backBarButtonItem = backItem // This will show in the next view controller being pushed
}
```    
