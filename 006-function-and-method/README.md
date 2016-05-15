# Function 及 Method

## Function 跟 Method

* 有什麼不同?

## 定義及使用

* 命名慣例與變數類似
* 儘量以程式碼可讀性為前提
* Ruby 常常會省略小括號

```ruby
# Ruby
def say_hello_to(name, age)
  puts "helli, #{name}, I am #{age} years old"
end

say_hello_to("見龍", 18)
say_hello_to "見龍", 18     # 小括號常常省略
```

```swift
// Swift
func sayHelloTo(name: String, age: Int) {
    print("hello, \(name), I am \(age) years old")
}

sayHelloTo("見龍", age: 18)        // 注意這裡 age 要連名帶姓的叫
```

## 回傳值

* Ruby 常常會省略 return，最後一行的執行結果預設就是其回傳值

```ruby
# Ruby
def bmi_calculator(height, weight)
  # BMI = 體重(公斤) / 身高2(公尺2)
  return weight / (height * height)        # 這裡的 return 可以省略
end

puts bmi_calculator(1.72, 70)              # 身高 1.72 公尺，體重 70 公斤
```

```swift
// Swift
func bmiCalculator(height: Double, weight: Double) -> Double {
    return weight / (height * height)
}

print(bmiCalculator(1.72, weight: 70))    # 身高 1.72 公尺，體重 70 公斤
```

## 特別補充

* Ruby 有種東西叫 Block

## 練習題
1. 實作一個 function 可以輸入陣列，回傳總和
2. 實作一個 function 回傳階乘數 (請用遞迴)

