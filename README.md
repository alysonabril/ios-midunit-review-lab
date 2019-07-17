## Mid Unit-1 Review


## Strings

1. **Given a String, return a String with each letter uppercased**

Input: `Hello, there`

Output: `HELLO, THERE`

2. **Given a String, return a String alternating between uppercase and lowercase letters**


Input: `Hello, there`

Output: `HeLlO, tHeRe`
```swift

let inputString = "Hello, there!"

var alternatingOutput = ""

var stringArray = Array(inputString)

for char in 0..<stringArray.count {
if  char % 2 == 0 {
alternatingOutput.append(stringArray[char].uppercased())
} else {
alternatingOutput.append(stringArray[char].lowercased())
}
}
print(alternatingOutput)

```

3. **Given a String, return a String with all occurrences of a given letter removed**

Input: `Hello, there`

Output: `Hllo, thr`

```swift
let inputString3 = "Hello, there?"
var removeLetter = ""

for character in inputString3 {
if character != "e" {
removeLetter.append(character)
}
}
print(removeLetter)


```

## Arrays


4. **Given an array of type [Int], return the largest element**

Input: `[1,5,2,4,1,4]`

Output: `5`

```swift
let numArray = [1,5,2,4,1,4]

var largestElement = numArray.max()
print(largestElement ?? 0) 
```

5. **Given an array of type [Int], return the smallest element**

Input: `[1,5,2,4,1,4]`

Output: `1`
```swift
let numArray2 = [1,5,2,4,1,4]
var smallestElement = numArray2.min()
print(smallestElement ?? 0)
```

6. **Given an array of type [Int], return its sum**

Input: `[1,5,2,4,1,4]`

Output: `17`
```swift
let numArray3 = [1,5,2,4,1,4]
var sum = 0

for i in numArray {
sum += i
}
print(sum)

```

7. **Given an array of type [Double], return its average**

Input: `[3,4.5,7.5,2,1]`

Output: `3.6`
```swift
let numArray4 = [3,4.5,7.5,2,1]
var total = Double()

for double in numArray4 {
total += Double(double)
}

let average = total/Double(numArray4.count)
print(average)

```

8. **Given an array of type [Double] and a Double, return the sum of all numbers in the array greater than a given number**

Input: `[3,4.5,7.5,2,1], 3`

Output: `12`

```swift
let numArray5 = [3,4.5,7.5,2,1]
let givenNum: Double = 3
var arraySum:Double = 0

for num in numArray5 where num > givenNum {
arraySum += num
}

print(arraySum)
```

9. **Given an array of type [Double], return the product of all the elements**

Input: `[3,4.5,7.5,2,1]`

Output: `202.5`
```swift
let numArray6 = [3,4.5,7.5,2,1]
let arrayProduct = numArray6.reduce(1, *)
print(arrayProduct)

//we worked together to show how reduce works
//let numArray6 = [3,4.5,7.5,2,1]
//var arrayProduct = Double(1)
//
//for num in numArray6 {
//    arrayProduct *= num
//}
//print(arrayProduct)
```

10. **Given an array of type [Int], return the second smallest value in the array**

Input: `[3,6,1,9,4,8]`

Output: `3`
```swift

```

## Optionals

11. **Given an array of type [String?] return an array of [String] removing all nil values**

Input: `[nil, "We", "come", nil, "in", "peace"]`

Output: `["We", "come", "in", "peace"]`

```swift
let inputOptional = [nil, "We", "come", nil, "in", "peace"]
var removedNil = [String]()
for string in inputOptional {
if let string = string {
removedNil.append(String(string))
}
}
print(removedNil)


```

12. **Given an array of type [String?]? return an array of [String] removing all nil values**

Input: `nil`

Output: `[]`
```swift
let optionalArray2: [String?]? = nil
print(optionalArray2 ?? [])
```

13. **Given an array of type [Int?] return the sum of all non-nil values.  Use guard statements in your solution.**

Input: `[4, nil, 9, 5, nil]`

Output: `18`
```swift

```

14. **Given an array of type [Int?]? return the sum of all non-nil values.  Use guard statements in your solution.**

Input: `nil`

Output: `0`
```swift

```

15. **Given an array of type [Int?] and an optional Int, return the sum of all values not equal to the given number.  If the given number is nil, return the sum of all non-nil values.**

Input: `[1, 1, nil, 3, 5, nil, 1, nil, 3, 5, nil, 5, nil, 3], 1`

Output: `24`

```swift

```
## Dictionaries

16. **Given an array of type [String], return a copy of the array with all duplicate values removed**

Input: `["apple", "apple", "banana", "banana", "banana", "cake", "cake"]`

Output: `["apple", "banana", "cake"]`
```swift

```

17. **Given a String, find the most frequently occurring letter**

Input: `Never trust a computer you can't throw out a window ~ Steve Wozniak`

Output: `t`
```swift

```

18. **Given an array of type [Int], return a copy of the array that contains only elements that appear at least twice**

Input: `[1,1,2,3,3,3,4,5,6,6,7]`

Output: `[1,3,6]`
```swift

```

19. **Given a String, find the second most frequently occurring letter in a string**

Input: `Never trust a computer you can't throw out a window ~ Steve Wozniak`

Output `o`
```swift

```

## Closures

20. **Given an array of type [String], return an array that contains the Strings sorted alphabetically with capital letters first (Swift will do that part automatically)**

Input: `["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]`
```swift

```
Output: `["Never", "a", "a", "can\'t", "computer", "out", "throw", "trust", "window", "you"]`
```swift

```
21. **Given an array of type [String], return an array that contains the Strings sorted by length**

Input: `["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]`

Output: `["a", "a", "you", "out", "Never", "trust", "can\'t", "throw", "window", "computer"]`
```swift

```
22. **Given an array of type [String], return an array containing all Strings at least 4 characters long**

Input: `["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]`

Output: `["Never", "trust", "computer", "can\'t", "throw", "window"]`
```swift

```

23. **Given an array of type [String], return a String containing all of the Strings from the array combined and separated by spaces.  Do this first without using the `joined(separator:) method`**

Input: `["Never", "trust", "a", "computer", "you", "can't", "throw", "out", "a", "window"]`

Output: `Never trust a computer you can't throw out a window`
```swift

```

## Enums


1. **Given an array of type [Int] and an instance of NumberType (defined below), return an array containing only all the even or odd numbers.**

```swift
enum NumberType {
case even
case odd

}
```

```swift

```

Input: `[1,2,3,4,5,6], NumberType.odd`
```swift
Output: `[1,3,5]`
func oddOrEven() {
if num % 2 == 0 {
even.append(num)
} else {
odd.append
}
}
```

```swift

```

2. **Given a String and an instance of StringType (defined below), return the String either lowercased or uppercased**

```swift
enum StringType {
case lowercase
case uppercase
}
```

Input: `"Design is not just what it looks like and feels like. Design is how it works", .uppercase`

Output: ``"DESIGN IS NOT JUST WHAT IT LOOKS LIKE AND FEELS LIKE. DESIGN IS HOW IT WORKS"``
```swift

```

3. **Given an array of type [FileStatus] (defined below) and an Int, return an array containing only files that were saved more than that many times**

```swift
enum FileStatus: CustomStringConvertible {
case unsaved
case saved(numberOfVersions: Int)
var description: String {
switch self {
case .unsaved: return "Unsaved File"
case let .saved(numberOfVersions): return "File that has been saved \(numberOfVersions) times"
}
}
}
```

Input: `[FileStatus.saved(numberOfVersions: 5), FileStatus.saved(numberOfVersions: 3), FileStatus.saved(numberOfVersions: 8)], 4`

Output: `[File that has been saved 5 times, File that has been saved 8 times]`
```swift

```
