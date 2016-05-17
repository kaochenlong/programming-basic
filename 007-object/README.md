# 物件

## 什麼是物件 (Object)

* 物件 (Object) = 狀態 (State) + 行為 (Behavior)
* 在 Ruby 裡，(幾乎)所有的東西都是物件

## 什麼是類別 (Class)

* 物件的藍圖
* 類別 = 分類

## 定義

* 規定：Ruby 的類別必須是「常數」(大寫字母開頭)

```ruby
# Ruby
class Animal
  def sleep                # 假設所有的動物都會睡覺
    puts "ZZZZZ"
  end
end

class Cat < Animal
end
```

```swift
// Swift
class Animal {
    func sleep() {        // 假設所有的動物都會睡覺
        print("ZZZZZ")
    }
}

class Cat: Animal {
}
```

## 使用方法

* 如果某個物件是由某個類別所「製造」出來的，那我們稱該物件是這個類別的一個實體(instance)

```ruby
# Ruby
kitty = Cat.new
kitty.sleep             # Cat 類別本身並沒有定義 sleep，但可正常運作
```

```swift
// Swift
var kitty = Cat()
kitty.sleep()          // Cat 類別本身並沒有定義 sleep，但可正常運作
```

## 初始化

```ruby
# Ruby
class Cat
  def initialize
    puts "我一出生就會講話喔"
  end
end

kitty = Cat.new
```

```swift
// Swift
class Cat {
    init() {
        print("我一出生就會講話喔")
    }
}

var kitty = Cat()
```

## 擴充功能

* 幫類別新增功能，甚至是內建的類別也行!
* Ruby 稱之「Open Class」，Swift 稱之「Extension」(Objective-C 稱之「Category」)

```ruby
# Ruby
class String
  def say_hello
    puts "hello, #{self}"
  end
end

"kk".say_hello            # => hello, kk
"見龍".say_hello          # => hello, 見龍
```

```swift
// Swift
extension String {
    func say_hello() {
        print("hello, \(self)")
    }
}

"kk".say_hello()          // => hello, kk
"見龍".say_hello()        // => hello, 見龍
```

## 特別補充 A

* 繼承有時沒辦法解決所有的需求...
* Ruby 有種東西叫 Module 模組

```ruby
module Fly
  def fly
    # .... 實作
  end
end

class Cat
  include Fly
end

kitty = Cat.new
kitty.fly
```

## 特別補充 B

* Swift 有種東西叫 Protocol

```swift
// Swift
protocol FlyingProtocol {
    func fly()
}

class Animal {
    func sleep() {
        print("ZZZZZ")
    }
}

class Cat: Animal, FlyingProtocol {
    func fly() {

    }
}
```

參考資料：

* http://kaochenlong.com/2010/12/11/protocol-in-objective-c/
* http://kaochenlong.com/2010/12/16/category-in-objective-c/

