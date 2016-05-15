# 陣列

## 寫法

* 使用中括號
* 元素不一定要放同一種型態
* 陣列裡可以再包陣列(N 維陣列)

```ruby
# Ruby
list = [1, 2, 3, 4, 5]
friends = ["eddie", "ken", "john", 1, 2, 3]
```

```swift
// Swift
list = [1, 2, 3, 4, 5]
friends = ["eddie", "ken", "john", 1, 2, 3]
```

## 存取

```ruby
# Ruby
friends = ["eddie", "ken", "john", "kitty"]
puts friends[0]
puts friends[-1]
puts friends.first
puts friends.last
```

```swift
// Swift
var friends = ["eddie", "ken", "john", "kitty"]
print(friends[0])
print(friends[friends.count - 1])
print(friends.first!)
print(friends.last!)
```

## 練習題
1. 給定一陣列內含數字，輸出最大值。
2. 使用者不斷輸入數字存進 Array，最後輸出總和、平均、最大值、最小值。
4. 建構一個陣列有 100 個的元素，內容是 0, 1, 4, 9, 16, 25...... 每個元素是該索引的平方
3. 請把陣列 [1, 2, 3, 4, 5] 變成 [1, 3, 5, 7, 9]。
