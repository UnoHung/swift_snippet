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
