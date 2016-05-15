# Hash 及 Dictionary

## 使用 Key-Value 結構的容器

* 在 Ruby 稱之 Hash
* 在 Swift 稱之 Dictionary

## 寫法

* Ruby 使用大括號，Swift 使用中括號

```ruby
# Ruby
profile = { :name => 'eddie', :age => 18 }     # Ruby 1.9 之前的寫法
profile = { name: 'eddie', age: 18 }           # Ruby 1.9 之後類似 JSON 格式的寫法
```

```swift
// Swift
var profile = ["name": "eddie", "age": 18]
```

## 存取

```ruby
# Ruby
profile = { name: 'eddie', age: 18 }

puts profile[:name]
puts profile["name"]          # 注意!! 這樣會拿到 nil
```

```swift
// Swift
var profile = ["name": "eddie", "age": 18]

print(profile["name"]!)
print(profile["age"]!)
```

## 走訪

```ruby
# Ruby
profile = { name: 'eddie', age: 18 }

# 方法 1
for k in profile.keys
  puts "#{k}: #{profile[k]}"
end

# 方法 2
profile.each do |k, v|
  puts "#{k}: #{v}"
end
```

```swift
// Swift
var profile = ["name": "eddie", "age": 18 ]

// 方法 1
for k in profile.keys {
    print("\(k): \(profile[k]!)")
}

// 方法 2
for (k, v) in profile {
    print("\(k): \(v)")
}
```

## 特別補充

* Ruby 有個東西叫 Symbol

## 練習題
1. 給定一 Hash，輸出有最大 value 的 key
2. 給定一 Hash，輸出 value 是偶數的 key
3. 陣列 a = [1, 2, 3, 1, 2, 1, 3, 1, 2, 3, 4, 5, 6]，請計算在陣列 a 中，每個數字出現的次數。
