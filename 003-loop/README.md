# 迴圈

## For 迴圈

### 樣式 1 - for

```swift
// Swift
for (var i = 0; i < 10; i++) {
    print("hi \(i)")
}
```

* Ruby 沒有這樣的寫法!

### 樣式 2 - for .. in

```ruby
# Ruby
for i in [*1..5]
  puts "hello, #{i}"
end

friends = ["Eddie", "John", "Kitty", "Jack"]

for friend in friends
  puts "Hello, #{friend}"
end

# 更常用這種寫法
friends.each do |friend|
  puts "Hello, #{friend}"
end
```

```swift
// Swift
for i in 1...5 {
    print("hello, \(i)")
}

let friends = ["Eddie", "John", "Kitty", "Jack"]

for friend in friends {
    print("Hello, \(friend)")
}
```

## While 迴圈

```ruby
# Ruby
i = 0

while i < 10
  puts "hi, #{i}"
  i += 1                # 記得要增加條件
end
```

```swift
// Swift
var i = 0

while i < 10 {
    print("hi \(i)")
    i += 1             // 記得要增加條件
}
```

## 練習題
1. 求 1 到 100 所有偶數的和
2. 請印出 1 ~ 100 數字中所有的單數。
3. 輸入一個數字 N，輸出 N * N 乘法表，例如輸入 12，輸出
```
0 x 0 = 0
0 x 1 = 0
......
12 x 11 = 132
12 x 12 = 144
```
4. 輸入一個數字 N，請檢查是不是質數(提示：從 2 開始到 N/2 不斷去除這個數字，如果可以整除就表示不是質數)
