# 流程控制

## 布林 (Boolean) 資料型別

* 只有 2 種結果，真的(true)，或是假的(false)，沒有其它
* Ruby 裡只有 `nil` 跟 `false` 是假的，其它都是真的

## 想想看...

回家的時候，太太打電話來交待：

> 回家的路上，買 10 個包子，如果看到西瓜，買 2 個

結果先生回到家，只買了 2 顆包子，因為他在路上看到西瓜了...

## 如果...不然就...(if .. else ..)

* Ruby 的 if 可以丟到後面去
* Ruby 有個 `unless` 可以用 (unless = if not)

```ruby
# Ruby
age = 20

if age >= 18
  puts "你是大人了"
else
  puts "加油!"
end
```

```swift
// Swift
var age = 20

if age >= 18 {
    print("你是大人了")
} else {
    print("加油!")
}
```

## 如果太多的「如果...不然就...(if .. else ..)」

```ruby
# Ruby
weather = "下雨"

case weather
when "下雨"
  puts "待在家!"
when "出太陽"
  puts "出去玩!"
else
  puts "在家睡覺!"
end
```

```swift
// Swift
var weather = "下雨"

switch weather {
  case "下雨":
    print("待在家!")
  case "出太陽":
    print("出去玩!")
  default:
    print("在家睡覺!")
}
```

還可以使用範圍技(Range)：

```ruby
# Ruby
age = 10

if age > 0 && age <= 3
  puts "Baby"
elsif age > 3 && age <= 10
  puts "Kids"
elsif age > 10 && age <= 17
  puts "Teenager"
else
  puts "Adult"
end

# 可改寫成：

age = 10

case age
when 0..3
  puts "Baby"
when 4..10
  puts "Kids"
when 11..17
  puts "Teenager"
else
  puts "Adult"
end
```

```swift
// Swift
var age = 10

if age > 0 && age <= 3 {
    print("Baby")
} else if age > 3 && age <= 10 {
    print("Kids")
} else if age > 10 && age <= 17 {
    print("Teenager")
} else {
    print("Adult")
}

// 可改寫成：
var age = 10

switch age {
case 0...3:
    print("Baby")
case 4...10:
    print("Kids")
case 11...17:
    print("Teenager")
default:
    print("Adult")
}
```

## 練習題
1. 使用者輸入一個數字 x，請判斷是否正數、零或負數，以及是不是偶數
2. 使用者輸入 x,y,z，請輸出三個數中最大的數字
