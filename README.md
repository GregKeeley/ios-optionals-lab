# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift
var userNameOne: String? = "Test User"
```
Answer
```swift
var userNameOne: String? = "Test User"

if let userNameOne = userNameOne {
    print("The username is \(userNameOne)")
}

```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).

```swift
var userNameTwo: String? = nil
```
Answer
```swift
var userNameTwo: String? = nil

let userTwo = userNameTwo ?? "The user is unidentified"
print(userTwo)
```

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
```
Answer
```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
var rectOneArea: Double? = (50)
if let squareRectOne = rectOneArea {
    print("The area of rectOne is \(squareRectOne)")
} else {
    print("The area of rectOne is not able to be calculated")
}
```
b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The are of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil
```
Answer
```swift
var rectTwoWidth: Double? = nil
var recTwoHeight: Double? = nil
var rectTwoArea: Double? = nil
if let squareRectTwo = rectTwoArea {
    print("The area of rectTwo is \(squareRectTwo)")
} else {
    print("The area of rectTwo is not able to be calculated")
}
```
## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70
```
Answer
```swift
if let oneName = userOneName, let oneAge = userOneAge, let oneHeight = userOneHeight {
    let formattedHeight = String(format: "%.2f", oneHeight / 12)
    print("Hello \(oneName), you are \(oneAge) years old, and you are \(formattedHeight)) feet tall.")
} else {
print("ERROR")
}
```

b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil
```


## Question 4

Give the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
```
Answer
```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil

if let favNum = favoriteNumber {
    print("Your favorite number is \(favNum)")
} else if favoriteNumber == nil {
    print("I don't know what your favorite number is")
}
```


## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
```
Answer
```swift
if let numSum5A = numOne5,let numSum5B = numTwo5,let numSumC = numThree5 {
print("The sum of the numbers is \(numSum5A + numSum5B + numSumC)")
} else {
    print("The values of the numbers is nil")
}
```
## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}
```

b. Using the same variable, find the average of all non-nil values.

## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
