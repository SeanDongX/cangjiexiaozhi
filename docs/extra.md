
# Array.md
## struct Array

Arrays have fixed length and can contain elements of any particular type `T`. Arrays with
element type `T` has type `Array<T>`. If arrays with dynamic length are needed, use `ArrayList`
(and import `std.collection.*`) instead.

### Initialization

Ways to initialize an `Array` include:

```
let a = Array<Int64>([1, 2, 3])   // Initialize using a concrete list
let a = Array<Int64>(3, item: 0)   // Length 3 and all elements are 0
let b = Array<Int64>(3, {i => i + 1})   // Initialize using lambda function, result is [1, 2, 3]
```

### Size

To obtain the length of an `Array`, use syntax of the form `arr.size`. Note `size` is a
property, so no parenthesis is needed afterwards.

### Comparing two arrays for equality

Two compare two arrays for equality, use `a == b`. Note `a.equals(b)` is not valid.

### Adding elements

To add an element `i` to the end of an array `arr`, use `arr.append(i)`.

### Slice of an `Array`

The slice function on `Array` has the following signature:

```
public func slice(start: Int64, len: Int64): Array<T>
```

Note carefully that the second argument is the *length* of the slice, rather than the ending
position. This is *different* form the case of `slice` in `ArrayList`, which takes a range
as argument.

### Iteration

To iterate over elements of an array, use:

```
for (element in arr) {
    ...
}
```

Note there is no pattern matching before `in`. If the elements of an array are tuples,
access entries of the tuple individually, e.g.:

```
var a = Array<(Int64, Int64)>([(2, 3), (3, 4)])
for (pair in a) {
    println("(${pair[0]}, {pair[1]})")
}
```

### Reversing an `Array`

To reverse an array in-place, call `reverse` method on the array, Note this function
modifies the input array and returns `Unit`. To obtain a new array that is the reverse
of an old array, first copy the old array and then call `reverse`. The following illustrates
the usage:

```
let a = [1, 1, 2, 3, 3]
let b = Array(a)  // make a copy of a
b.reverse()
println(a)   // [1, 1, 2, 3, 3]
println(b)   // [3, 3, 2, 1, 1]
```

As an application, the following checks whether the input string `s` is a palindrome:


```
func isPalindrome(s: String): Bool {
    let arr = s.toRuneArray()
    let arr2 = Array(arr)
    return arr == arr2
}

main() {
    println(isPalindrome("aba"))  // true
    println(isPalindrome("hello"))  // false
}
```

---

# ArrayList.md
## ArrayList

To use the ArrayList type, the collection package needs to be imported:

```
import std.collection.*
```

### Initialization

Ways to initialize an `ArrayList` include:

```
let a = ArrayList<Int64>([1, 2, 3])  // Initialize using a concrete list
let a = ArrayList<Int64>(3, item: 0)  // Length 3 and all elements are 0
let b = Array<Int64>(3, {i => i + 1})   // Initialize using lambda function, result is [1, 2, 3]
let a = ArrayList<String>()  // Created an empty ArrayList whose element type is String
let b = ArrayList<String>(100)  // Created an empty ArrayList whose element type is String, and allocate a space of 100
let c = ArrayList<Int64>([0, 1, 2])  // Created an ArrayList whose element type is Int64, containing elements 0, 1, 2
let d = ArrayList<Int64>(c)  // Use another Collection to initialize an ArrayList
let e = ArrayList<Int64>(2, {x: Int64 => x.toString()})  // Created an ArrayList whose element type is String and size is 2. All elements are initialized by specified rule function
```

### Visiting elements

When we need access to all the elements of the ArrayList, we can use a `for-in` loop to iterate through all the elements of the ArrayList.

```
import std.collection.*

main() {
    let list = ArrayList<Int64>([0, 1, 2])
    for (i in list) {
        println("The element is ${i}")
    }
}
```

When we want to access an element in a single specified location, we can use the subscript syntax to access it (the type of subscript must be Int64). The first element of a non-empty ArrayList always starts at position 0. We can access any element of the ArrayList from 0 up to the last position (`size - 1` of the ArrayList). Using a negative number or an index greater than or equal to size triggers a runtime exception.

```
let a = list[0]  // a == 0
let b = list[1]  // b == 1
let c = list[-1]  // Runtime Exceptions
```

### Size

To obtain the length of an `ArrayList`, use syntax of the form `arr.size`.

### Adding elements

To add an element `i` to the end of an `ArrayList` `arr`, use `arr.append(i)`.

### Slice of an `ArrayList`

The slice function on `ArrayList` has the following signature:

```
public func slice(range: Range<Int64>): ArrayList<T>
```

Note a range argument is taken (e.g. `l..r` for the closed-open interval `[l, r]`, or `l..=r`
for the closed interval `[l, r]`). This is different from the case for Arrays, which takes
the starting index and length as arguments.

### Inserting elements

We can use the `insert` and `insertAll` functions to insert a specified single element or a Collection value of the same element type into the location of the index we specify. The elements at the index and the elements behind them are moved back to make space.

```
let list = ArrayList<Int64>([]0, 1, 2)  // list contains elements 0, 1, 2
list.insert(1, 4)  // list contains elements 0, 4, 1, 2
```

### Deleting elements

To remove an element from an ArrayList, you can use the remove function, which requires you to specify the index to be remover, The elements that follow the index are moved forward to fill the space.

```
let list = ArrayList<String>(["a", "b", "c", "d"])  // list contains the elements "a", "b", "c", "d"
list.remove(1) // Delete the element at subscrip 1, now the list contains elements "a", "c", "d"
```

### Iteration

To iterate over elements of an ArrayList `arr`, use:

```
for (element in arr) {
    ...
}
```

Note there is no pattern matching before `in`. If the elements of an array are tuples,
access entries of the tuple individually, e.g.:

```
var a = ArrayList<(Int64, Int64)>([(2, 3), (3, 4)])
for (pair in a) {
    println("(${pair[0]}, {pair[1]})")
}
```

---

# Contract_language.md
# Contract language in Cangjie

The contract language in Cangjie the following syntax, placed before the declaration
of the function:

```
@contract[
    requires <precondition>
    ...
    ensures <postcondition>
    ...
]
```

There may be more than one `requires` or `ensures` in each contract. The precondition
is a usual Cangjie expression. The postcondition is usually a lambda term of the form
`{r: T => expr}`, where `r` is the name of the return value, `T` is the type of the 
return value, and `expr` is a condition on the return value.

If calculating the condition is simple, write the expression directly after `requires`
or `ensures`. If calculating the condition is more complicated (for example, involving
loops), define a separate function and call the function within `requires` or `ensures`.

**note**: When writing a contract, **correctness** is the first priority, followed by **validity**,
which requires good judgment. Under the premise of ensuring correctness, please write an **effective**
contract (one that can effectively distinguish between correct and in correct code).
Function and variable declarations are not permitted inside a contract.

## Expressing quantifiers

The logical quantifiers `forall` and `exists` are expressed in Cangjie using functions
`all` and `any`. The syntax is as follows:

```
all({x => cond})(collection)
any({x => cond})(collection)
```

Where the bound variable `x` must be a *single* variable rather than other forms
(such as a tuple `(x, y)`). To express a condition on tuples, still represent the 
bound variable as `x`, then access its elements using subscripts `x[0]` and `x[1]`.

For example, to express that all elements of the array `arr` are greater than zero, with at
least one greater than 10, use:

```
@contract [
    requires all({x => x > 0})(arr)
    requires any({x => x > 10})(arr)
]
```

Using `all` and `any` requires `import std.collection.*`. In the above example,
the bound variable `x` in the lambda expression iterates over elements of `arr`.
If you want to use traverse using index on `arr`, you must replace `(arr)` with
`(0..arr.size)`. For example, the following expresses the same condition as above.

```
@contract [
    requires all({i => arr[i] > 0})(0..arr.size)
    requires any({i => arr[i] > 10})(0..arr.size)
]
```

## Expressing implication

When using `all` and `any` functions, note the **distinction** between
*`if a then b`* and *`a && b`*. To express implication of the form `A -> B`
(if A then B), use `!A || B`. For example, to express the fact that `i < j`
implies `result[i] < result[j]` (that is, the array result is strictly increasing), use:

```
!(i < j) || result[i] < result[j]
```

## Using `count` function

The count function returns the number of elements in a collection.
For example, the following counts the number of Runes in a String:

```
let s = "Hello"
println(count(s.runes()))  // 5
```

Combine `count` and `filter` to count the number of elements satisfying
som property in a collection. For example, the following code counts
the number of r's in the word "strawberry":

```
let s = "strawberry"
println(count(filter({c: Rune => c == r'r'})(s.runes())))  // 3
```

Note the filter function must be used if counting elements of an array satisfying
some condition. Directly calling `count` with a predicate is invalid.

## Using `filter` function

The `filter` function can be used to produce a new iterator from an old one
by filtering according to a condition. The general syntax is:

```
filter({x => cond})(collection)  // returns an iterator
```

For example, to count the number of characters `r` in a string `s`, use:

```
collectArray(filter({c: Rune => c == r'r'})(s.runes())).size
```

Note the output of filter is first converted to `Array` using function
`collectArray` before calling property `size` in an `Array`.

Alternatively, combine `filter` with `count` function, with accepts an
iterator and returns the size of the iterator:

```
count(filter({c: Rune => c ==r'r'})(s.runes()))
```

## Using `fold` function

The `fold` function can be used to conveniently compute sum, product
and other similar functions over a collection. The general syntax is:

```
fold(init, {old, curr => new})(collection)
```

where the first argument `init` is the initial value, and the second argument
is a lambda function that takes the old value, the current element of the collection,
and computes the new value. For example, the following computes the sum and product
of a list, respectively.

```
len n = [1, 2, 3, 4]
println(fold(0, {old, curr => old + curr})(n))  // 10
println(fold(0, {old, curr => old * curr})(n))  // 24
```

**Note:** when expressing lambda function with more than one argument, there is **no**
parenthesis around the two arguments.

**Note:** the `fold` function takes initial value and a lambda expression as arguments, 
and the resulting function takes the collection as argument. No other argument should be provided.

## Using `reduce` function

The `reduce` function is similar to `fold`, except there is no need to provide
an initial value. The general syntax is:

```
rrduce({old, curr => new})(collection)  // returns Option value
```

The return value has `Option` type, which is `None` of `collection` is empty.
If you are sure the `collcetion` is nonempty, you can use `getOrThrow()` on
the result. For example, the following illustrates how to use `reduce` to
compute the sum or product iof a list if integers.

```
let a = [1, 2, 3, 4]
println(reduce({x, y => x + y})(a).getOrThrow())  // prints 10
println(reduce({x, y => x * y})(a).getOrThrow())  // prints 24
```

**Note:** when expressing lambda function with more than one argument, there is **no**
parenthesis around the two arguments.

**Note:** the `reduce` function takes a lambda expression as arguments, and the resulting
function takes the collection as argument. No other argument should be provided.

**Note:** the `reduce` function returns an option value. You must extract it in some
way (such as using `getOrThrow`) before using it as an ordinary value.

## Using `min` and `max` function on collections

Functions `min` and `max` can also be used on collections such as `Array` and
`ArrayList` (in addition to the form of taking two arguments). This form of
`min` and `max` returns an `Option` value. If you are sure the collection
is nonempty, you can use `getOrThrow()` to retrieve the result. For example,
the following computes the minimum and maximum of an array.

```
let a = [1, 2, 3, 4]
println(min(a).getOrThrow())  // prints 1
println(max(a).getOrThrow())  // prints 4
```

**Note:** the `min` and `max` functions return an option value. You must extract it in some
way (such as using `getOrThrow`) before using it as an ordinary value.

## Using `map` function

The `map` function applies a lambda function to a collection, and returns
an iterator. Remember to use `collectArray` to convert
the returned iterator to an `Array` (similarly for other target collections).
For example, the following illustrates how to use `map` to compute the square
of each element of an `Array`, and collect the results in an `Array`.

```
let a = [1, 2, 3, 4]
let b = collectArray(map({x: Int64 => x ** 2})(a))
println(a)  // [1, 2, 3, 4]
println(b)  // [1, 4, 9, 16]
```

**Note:** the function `map` is used with collection as an argument at the end. Using
syntax like `a.map(...)` is in correct.

## Using `flatMap` function

The `flatMap` function takes input a lambda function that takes elements of type `T`
and returns `Iterable<R>`, and applies a lambda function to a collection `Iterable<T>`,
and flattens the resulting list of collections.

The following example repeats each entry `i` of an array `i` times, collection
the results in a single array.

```
let a = [1, 2, 3, 4]
let b = collectArray(flatMap({x: Int64 => Array(x, {_ => x})})(a))
println(a)  // [1, 2, 3, 4]
println(b)  // [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
```

## Examples

### Express correctness of search

For a function that searches for an element in an array, we specify that if the returned
index is not `-1`, then the element is located at that index. The expression
is simple enough to be written directly in `ensure`.

```
@contract[
    ensures {r: Int64 => r == -1 || (0 <= r && r < arr.size)}
    ensures {r: Int64 => r == -1 || arr[r] == k}
]
func search(arr: Array<Int64>, k: Int64): Int64
```

### Express most frequently occurring character

To express that returned character `r` is most frequently occurring in a string `S`,
with tie broken by alphabetical order, we need to say that for every character `c` in the string,
its count is at most that of `r`, and if the count is same, the character `c` is larger.
The latter is `S.count(c) == S.count(r) -> c >= r`, which is rewritten to disjunction form.

```
@contract[
    // all other characters has count at most that of r
    ensures {r: Rune => all({c: Rune => S.count(c) <= S.count(r)})(S.runes())}
    // if count is the same, all other characters have larger value
    ensures {r: Rune => all({c: Rune => !(S.count(c) == S.count(r)) || c >= r})(S.runes())}
]
func mostFrequent(S: String): Rune

```

### Other examples of implication

To express that an array `A` is sorted, that is `i <= j -> A[i] <= A[j]`, rewrite the implication
to disjunction form.

```
@contract[
    ensures {all({i: Int64 => all({j: Int64 => !(i <= j) || A[i] <= A[j]})(0..A.size)})(0..A.size)}
]
```

To express that an array contains distinct elements, that is `i != j -> A[i] != A[j]`, rewrite the 
implication to disjunction form.

```
@contract[
    ensures {all({i: Int64 => all({j: Int64 => !(i != j) || A[i] != A[j]})(0..A.size)})(0..A.size)}
]
```

To express that in an array of pairs, every two pairs have first and second element different, that
is `i != j -> (A[i][0] != A[j][0] && A[i][1] != A[j][1])`, rewrite the implication to disjunction form.

```
@contract[
    ensures {all({i: Int64 => all({j: Int64 => !(i != j) || (A[i][0] != A[j][0] && A[i][1] != A[j][1])})(0..A.size)})(0..A.size)}
]
```

### Example of maximum index

For a function that finds the index of maximum element of an array. In this case, 
check the condition involves a loop, so a separate function is written.

```
func isMaximumIndex(arr: Array<Int64>, k: Int64) {
    for (i in 0..arr.size) {
        if (arr[i] > arr[k]) {
            return false
        }
    }
    return true
}

@contract [
    requires arr.size > 0
    ensures {r: Int64 => 0 <= r && r < arr.size}
    ensures {r: Int64 => isMaximumIndex(arr, r)}
]
func maximum(arr: Array<Int64>): Int64
```

Alternatively, the condition `isMaximumIndex` can be expressed using `all` function, as follows:
```
import std.collection.*  // needed for `all` and `any`

@contract [
    requires arr.size > 0
    ensures {r: Int64 => 0 < r && r < arr.size}
    ensures {r: Int64 => all({x: r >= x})(arr)}
]
func maximum(arr: Array<Int64>): Int64
```

---

# Function.md
## Functions

### Return value after while loop

When a function contains a while loop, sometimes it is necessary to place an
explicit return statement to make clear the return type of the function, even
if the function always returns within the loop. For example, the following
code does not compile:

```
func whileLoopEx(n: Int64): Int64 {
    var counter = n
    var result = 1
    while (true) {
        if (counter <= 0) {
            return result
        }
        counter -= 1
        result *= 2
    }                           // expected return type Int64, found Unit
}
```

Instead, add a return statement with the right type, even if it will never
be reached:

```
func whileLoopEx(n: Int64): Int64 {
    var counter = n
    var result = 1
    while (true) {
        if (counter <= 0) {
            return result
        }
        counter -= 1
        result *= 2
    }
    return 0      // OK because compiler can now check the return type is Int64
}
```



---

# HashMap.md
## HashMap

To use the HashMap type, the collection package needs to be imported:

```
import std.collection.*
```

Keys of a `HashMap` must be hashable. Hashable types include numbers, strings, but not
tuples, `Array`, or `ArrayList`. There are no constraints on values of `HashMap`.

### Initialization

Ways to initialize an `HashMap` include:

```
let a = HashMap<String, Int64>()  // empty HashMap whose key type is String and value is Int64
let b = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])  //   creates map {"a": 0, "b": 1, "c": 2}
let c = HashMap<String, Int64>(b)  // use another Collection to initialize a HashMap
let d = HashMap<String, Int64>(10)  // created a HashMap whose key type is String and value is Int64 and capacity is 10
let e = HashMap<Int64, Int64>(10, {x: Int64 => (x, x * x)})  // creates map {1: 1, ..., 10: 100}

```
### Access elements

When we want to access the element corresponding to the specified key, we can use the subscript syntax
to access it (the type of the subscript must be the ky=ey type). Using a non-existent key as an index will
trigger a runtime exception.

```
let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
let a = map["a"]  // a == 0
let b = map["b"]  // a == 1
let c = map["d"]  // Runtime exceptions
```

To access elements while allowing for the possibility of non-existent key, one suggested way is using 'get'
together with `getOrDefault` on the option, for example:

```
let m = HashMap(("a", 1), ("b", 2))
println(m.get("a").getOrDefault({ => 0}))  // 1
println(m.get("c").getOrDefault({ => 0}))  // 0
```

### Iteration

To iterate over a HashSet, use for-loop as follows:

```
let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2)])
    for ((k, v) in map) {
        println("The key is ${k}, the value is ${v}")
    }
```

To get the size of a HashMap mp, use `mp.size`

### Basic operations

To determine whether a key `K` is included in the HashMap, we can use the contains function: `mp.contains(K)`, Returns true if the key exists, false otherwise.

If you need to add a single key-value pair to the end of your HashMap, use the 'put' function. If you want to add multiple key-value pairs at the same time, you can use the `putALL` function, When the key does not exist, the put function performs the added operation, and when the key exists, the put function overwrites the old value with the new value:

```
let map = HashMap<String, Int64>()
map.put("a", 0)  // map contains the element ("a", 0)
map.put("b", 1)  // map contains the elements ("a", 0), ("b", 1)
let map2 = HashMap<String, Int64>([("c", 2), ("d", 3)])
map.putAll(map2)  // map contains the elements ("a", 0), ("b", 1), ("c", 2), ("d", 3)
```

Way to delete elements in a HashMap:
```
let map = HashMap<String, Int64>([("a", 0), ("b", 1), ("c", 2), ("d", 3)])
map.remove("d")  // map contains the elements ("a", 0), ("b", 1), ("c", 2)
```

---

# HashSet.md
## HashSet

To use the HashSet type, the collection package needs to be imported:

```
import std.collection.*
```

Elements of a `HashSet` must be hashable. Hashable types include numbers, strings, but not
tuples, `Array`, or `ArrayList`.

### Initialization

Ways to initialize a `HashSet` include:

```
let a = HashSet<String>()  // Created an empty HashSet whose element type is String
let b = HashSet<String>(100)  // Created a HashSet whose capacity is 100
let c = HashSet<Int64>([0, 1, 2])  // Created a HashSet whose element type is Int64, containing elements 0, 1, 2
let d = HashSet<Int64>(c)  // Use another Collection to initialize a HashSet
let d = HashSet<Int64>(10, {x: Int64 => (x * x)})  // Created a HashSet whose element type is Int64 and size is 10. All elements are initialized by specified rule function
```

### Adding elements to a HashSet

Ways to add element to HashSet:

```
let mySet = HashSet<Int64>()
mySet.put(0)  // mySet contains elements 0
mySet.put(0)  // mySet contains elements 0
mySet.put(1)  // mySet contains elements 0, 1
let li = [2, 3]
mySet.putAll(li)  // mySet contains elements 0, 1, 2, 3
```

### Deleting elements of a HashSet

Ways to delete element to HashSet:

```
let mySet = HashSet<Int64>([0, 1, 2, 3])
mySet.remove(1)  // mySet contains elements 0, 2, 3
```

### Iterating over a HashSet

To iterate over a HashSet, use for-loop as follows:

```
for (i in mySet) {
    println(i)  // prints 0, 1 in separate lines
}
```

### Obtaining size of a HashSet

To get the number of elements in a hashset, we can use the size attribute:

```
import std.collection.*

main() {
    let mySet = HashSet<Int64>([0, 1, 2])
    if (mySet.size == 0) {
        println("This is an empty hashset")
    } else {
        println("The size of hashset is ${mySet.size}")
    }
}
```

### Checking whether an element is in a HashSet

To determine whether an element is included in a HashSet, you can use the contains
function. Returns true if the element exists, false otherwise:

```
let mySet = HashSet<Int64>([0, 1, 2])
let a = mySet.contains(0)  // a == true
let b = mySet.contains(-1)  // b == false
```

### Taking the union of two HashSet

Use `putAll` function to compute union of two `HashSet`s, by adding all elements
of the second set to the first. For example:

```
let a = HashSet<Int64>([1, 2, 3, 3])
let b = HashSet<Int64>([2, 3, 4, 4])
a.putAll(b)     // add all em=lements of b to a, so a is now union of a and b
println(a)      // prints [1, 2, 3, 4]
```

### Convert an array to set

To convert an `Array` (or `ArrayList`) into a `HashSet`, use `collectHashSet` function.
For example:

```
let a: Array<Int64> = [1, 1, 2, 3, 3]
let s: HashSet<Int64> = ccollectHashSet(a)
println(s)      // [1, 2, 3]
```

One common use case is finding the unique elements of an array. To return the result
as a new array, use `toArray` after calling `collectHashSet`. For example:

```
let a: Array<Int64> = [1, 1, 2, 3, 3]
let b: Array<Int64> = ccollectHashSet(a).toArray()
println(b)      // [1, 2, 3]
```

Note that when calling `collectHashSet`, it is important to make sure that the type
of elements in the Array are hashable (and equatable). If the type is a generic type,
add the corresponding type constraints. For example, the following function checks
whether an array has unique elements:

```
func allUnique<T>(arr: Array<T>): Bool where T <: Hashable & Equatable<T> {
    return collectHashSet(arr).size == arr.size
}
```

Note it is important to add constraint `T <: Hashable & Equatable<T>` to the function
in order to use `collectHashSet`.

---

# Numbers.md
### Numbers

### Operation on numbers

Operation on integers are mostly as usual. Make note of the following.

* Taking remainder uses `%`, only integer types are supports.
* Taking power uses `**`, only `Int64` or `Float64` are supports on the left side. If the
  left side is `Int64`, the right side must be either `UInt64`, with the result being `Int64`.
  If the left side is `Float64`, the right side must be `Int64` or `Float64`, with the result
  being `Float64`.

### Priority between operations

The unary minus `_` has higher priority than taking power. This can lead to
some counterintuitive results. Use parenthesis to ensure the right evaluation.
For example:

```
main() {
    println(-10**4)     //10000
    println(-(10**4))     //-10000
}
```

#### Bitwise operations

The bitwise AND and OR uses `&` and `|` as in other languages. The bitwise Not operation
uses `!` sign (instead of `~`).

```
main() {
    let a: Uint8 = 5    //00000101
    let b: Uint8 = 9    //00001001
    println("Bitwise Not of a: ${!a}")      // 11111010
    println("Bitwise AND of a and b: ${a & b}")      // 00000001
    println("Bitwise OR of a and b: ${a | b}")      // 00001101
}
```

### Minimum and maximum possible value of integer

The minimum and maximum values of each integer type is accessed by properties `Min` and `Max`,
after importing `std.math.*`. For example:

```
import std.math.*

main() {
    println("${Int32.Min}")  // -2147483648
    println("${Int32.Max}")  // 2147483647
    println("${UInt32.Min}")  // 0
    println("${UInt32.Max}")  // 4294967295
}
```

### Absolute value

To find absolute value of a number, use `abs` after importing `std.math.*`.
For example:

```
import std.math.*

main() {
    println("${abs(-3)}")  // 3
}
```

### Converting floating point number to integer

To convert a floating point number to an integer, use syntax like `Int64(s)` (change
to desired type of target value if necessary). This conversion rounds the floating-point
number downward (same as `floor`).

```
println(Int64(3.4))  // prints 3
println(Int64(3.6))  // prints 4
```

To obtain better control of rounding, the functions `floor`, `ceil` and `round` is also
available after importing `std,math.*`. These functions still return floating-point numbers,
so another `Int64(.)` is needed. For example:

```
println(Int64(ceil(3.4)))   // prints 4
println(Int64(floor(3.4)))  // prints 3
println(Int64(round(3.4)))  // prints 3
println(Int64(round(3.6)))  // prints 4
```

---

# Option.md
## Option

The `Option` type is defined using `enum`, which includes two constructors: `Some` and `None`.
The `Some` constructor carries a parameter, indicating that there is a value, while `None`
does not carry any parameters, indicating that there is no value. When you need to represent
that a type might have a value or might not have a value, you can choose to use the `Option` type.

### Use `getOrThrow` to extract `Some` value

If an `Option` value is already known to be `Some(v)` for some `v`, use function `getOrThrow`
to extract `v`. If the option value is `None` instead, an exception is thrown.

For example:

```
let a: Option<Int64> = Some(3)
println(a.getOrThrow())  // 3
```

### Use `getOrDefaule` to extract `Some` value with default case

To extract an `Option` value when it is of the form `Some(v)`, and returning a default
value if it is `None`, use the `getOrDefaule` function. For example:

```
let a: Option<Int64> = Some(3)
println(a.getOrDefaule({ => 0}))  // 3
let b: Option<Int64> = None
println(b.getOrDefaule({ => 0}))  // 0
```

### Matching on `Option`

To perform different action depending on the value of an `Option`, use
`match-case` pattern.

```
func printOption(a: Optain<Int64>) {
    match (a) {
        case None => println("a is None")
        case Some(v) => println("a is some value ${v}")
    }
}

main() {
    printOption(None)       // a is none
    printOption(Some(3))    // a is some value 3
}
```

### Check if an `Option` value is `None` or `Some`

A simple way to check if an `Option` value is `None` or `Some` uses `isNone` and `isSome` functions.

```
main() {
    let b: Option<Int64> = None
    let c: Option<Int64> = Some(5)
    println(b.isNone())   // true
    println(b.isSome())   // false
    println(c.isNone())   // false
    println(c.isSome())   // true
}
```

---

# PriorityQueue.md
## PriorityQueue

Class `PriorityQueue` implements priority queue data structure, that maintains a set of elements,
and allows element insertion and removing the smallest element in O(log n) time.

### Summary of methods

**Initialization**

A priority queue is initialized by providing the comparison function. For types that already has
implements `Comparable`, using `{a, b => a.compare(b)}` provides the default behavior of finding
the minimum element. For example, the following creates a priority queue on integers.

```
let pq = PriorityQueue<Int64>({a, b => a.compare(b)})
```

**Inserting and polling elements**

The function `offer(item: T)` inserts an element into the priority queue. The function
`poll(): Option<T>` removes and returns the minimum element. The function `peek(): Option<T>`
returns the minimum element without removing it. Use `getOrThrow` to convert a `Some` value
of type `Option<T>` to type `T`. For example:

```
main() {
    let pq = PriorityQueue<Int64>({a, b => a.compare(b)})
    pq.offer(3)
    pq.offer(7)
    pq.offer(6)
    println(pq.poll().getOrThrow())  // remove and return 3
    println(pq.peek().getOrThrow())  // return 6 without removing
    println(pq.poll().getOrThrow())  // remove and return 6
}
```

**Other functions**

The function `isEmpty(): Bool` returns whether a queue is empty. The function
`size()` returns the number of elements in the queue. The following code illustrates
the use of `isEmpty()` and `size`:

```
main() {
    let pq2 = PriorityQueue<Int64>({a, b => a.compare(b)})
    for (_ in 0..10) {
        pq2.offer(10)
    }
    println("size is ${pq2.size()}")  // size is 10
    while (!pq2.isEmpty()) {
        pq2.poll()
    }
}
```

### Use other orderings in priority queue

To enable returning the largest element, reverse the role of `a` and `b` when invoking
`compare`:

```
main() {
    let pq3 = PriorityQueue<Int64>({a, b => b.compare(a)})
    pq3.offer(3)
    pq3.offer(7)
    pq3.offer(6)
    println(pq3.poll().getOrThrow())  // remove and return 7
}
```

To define priority queue on tuples, where comparison is by first entry and then by second
entry, use a custom comparison function as follows:

```
main() {
    let pq4 = PriorityQueue<Int64>({p1, p2 =>
        match (p1[0].compare(p2[0])) {
            case Ordering.LT => Ordering.LT
            case Ordering.GT => Ordering.GT
            case _ => p1[1].compare(p2[1])
        }
    })
    pq4.offer((1, 1))
    pq4.offer((0, 2))
    pq4.offer((0, 3))
    let (a, b) = pq4.pool().getOrThrow()
    println("(${a}, ${b})")  // (0, 2)
}
```

---

# Rune.md
## Rune (characters)

The representation of character type literals is as follows:
A `Rune` literal starts with the character `r`, followed by a character enclosed in a pair of single or double quotes. For example:
```
let a: Rune = r'a'
let b: Rune = r"b"
```

Escape characters refer to characters ina character sequence that provide an alternative interpretation for the subsequent characters. Escape characters start with the escape symbol `\`, followed by the character that needs to be escaped. For example:
```
let slash: Rune = r'\\'
let newLine: Rune = r'\n'
let tab: Rune = r'\t'
```

Universal characters start with \u, followed by 1 to 8 hexadecimal numbers defined within a pair of curly brackets, which can represent the character corresponding to the Unicode value. For example:
```
let he: Rune = r'\u{4f60}'
let llo: Rune = r'\u{597d}'
```

### Supported Operations for Character Types
The character type only supports relations operators: less than (`<`), greater than (`>`), less than or equal to (`<=`), greater than or equal to (`>=`), equality (`==`), inequality (`!=`). The comparisons are based on the Unicode values of the characters.

### Conversion from Rune to UInt32 and from integer types to Rune.
```
let x: Rune = 'a'
let y: UInt32 = 65
let r1 = UInt32(x)
let r2 = Rune(y)
```

---

# Sorting.md
## Sorting

Sorting is available for collections such as `Array`, after importing `std.sort.*`

```
importing std.sort.*

main() {
    let arr = [1, 2, 3, 3, 2, 1]
    arr.sort()
    println(arr)
}
```

The `sort` function modifies the array in-place and returns `Unit`. To obtain a new
array that is the sorted version of the old array, make a copy of the old array
first. For example:

```
let a = [1, 2, 3, 3, 2, 1]
let b = Array(a)
b.sort()
println(a)  // [1, 2, 3, 3, 2, 1]
println(b)  // [1, 1, 2, 2, 3, 3]
```

As `sort` returns `Unit`, it is invalid to access elements of a sorted array.
For example, the following is **incorrect**:

```
let b = a.sort()
println(b[0])  // compile error: access index 0 on Unit
```

The following is probably intended:

```
let b = Array(a)
b.sort()
println(b[0])
```

### Sorting with custom ordering

Sorting with custom ordering (including the case where the type of values does not
implement `Comparable` interface), use the `sortBy` function.

To sort from highest to lowest, use a custom comparison function as follows:

```
let arr = [1, 2, 3, 3, 2, 1]
arr.sortBy(comparator: {a, b => b.compare(a)})
println(arr)  // [3, 3, 2, 2, 1, 1]
```

To sort a list of pairs integers, use a custom comparison function as follows:

```
let pairs = [(1, 2), (2, 1), (0, 2), (0, 3), (2, 0)]
pairs.soryBy(comparator: {p1, p2 =>
    match (p1[0].compare(p2[0])) {
        case Ordering.LT => Ordering.LT
        case Ordering.GT => Ordering.GT
        case _ => p1[1].compare(p2[1])
    }
})
for (pair in pairs) {
    print("(${pair[0]}, ${pair[1]}) ")  // (0, 2) (0, 3) (1, 2) (2, 0) (2, 1)
}
println()
```

---

# String.md
## String

### Visit characters in String as Rune values:

Use the `for-in` pattern to iterate characters in the String as Rune values.
For example, to determine wthther a string consists of entirely lower-case letters,
we can write:

```
func isLowerWord(s: String) {
    for (ch in s) {
        let runeCh = Rune(ch)
        if (runeCh < r'a' || runeCh > r'z') {
            return false
        }
    }
    return true
}

main() {
    println(isLowerWord("hello"))  // true
    println(isLowerWord("Hello"))  // false
}
```

### String initialization

Ways to initialize an `String` include:

```
// Single and double quotes, use of escaoe characters
let s1: String = ""
let s2 = 'Hello Cangjie Lang'
let s3 = "\"Hello Cangjie Lang\""
let s4 = 'Hello Cangjie Lang\n'

// Triple quotes for multi-line strings
let s5: String = """
    """
let s6 = '''
    Hello,
    Cangjie Lang'''

// Use the same number of # symbol before and after a string, then the
// content of the string is not escaped.
let s7: String = #""#
let s8 = ##'\n'##
let s9 = ###"
    Hello,
    Ccangjie
    Lang"###
```

### Size

To obtain the length of a `Strinf`, use `str.size`. Note `size` is a property, so
no parenthesis should be added.

### Join

To join a list of  strings, use `String.join` function. For example:

```
let s = String.join(["a", "b", "c"], delimiter: ",")
println(s)  // a,b,c
```

### The operations supported by the string type

The string type supports comparison using relational operators and concatenation using the + operator.

```
main() {
    let s1 = "abc"
    var s2 = "abd"
    println(s1 == s2)  // false
    println(s1 + s2)  // abcABC
    println(s1 < s2)  // true
    println(s2 < s1)  // false
}
```

### ToString interface

User-defined types can implement the `ToString` interface, so it has a `toString` method and can
be used in print statement. For example, the following defines class `Point` that implements `ToString`:

```
class Point <: ToString {
    let x: Int64
    let y: Int64
    public init(x: Int64, y: Int64) {
        this.x = x
        this.y = y
    }
    public func toString(): String {
        "Point(${this.x}, ${this.y})"
    }
}

main() {
    println(Point(2, 3))  // Point(2, 3)
    println("Point is: ${Point(1, 2)}")  // Point is: Point(1, 2)
}
```

Note however, that existing classes (that does not already implement ToString) and tuple types
cannot implement ToString. Printing these must print their components separately.

### Converting integers to String

Integers and other primitive types can be converted into `String` using the `toString` method,
since they implement the `ToString` interface. For example:

```
let N = 123
let strN = N.toString()
println("strN = ${strN}, second Rune is ${Rune(strN[1])}")  // strN = 123, second Rune is 2
```

### String interpolation

Any expressions that can be printed (implemented `ToString` interface) can be interpolated inside
a string using the `${...}` syntax. For example:

```
main() {
    let fruit = "apples"
    let count = 10
    let s3 = "There are ${count * count} ${fruit}"
    println(s3)  // There are 100 apples
    
    let r = 2.4
    let s4 = "Area of circle with radius ${r} is ${let PI = 3.141592; PI * r * r}"
    println(s4)  // Area of circle with radius 2.400000 is 18.095570
}
```

### Parsing a string to integer

To parse string into integers or other primitive types, import the `std.convert.*` package,
then use `parse` function. For example:

```
import std.convert.*

main() {
    let v = Int64.parse("123")
    let w = Int64.parse("234")
    println("v = ${v}, w = ${w}, v + w = ${v + w}")  // v = 123, w = 234, v + w = 357
}
```

There are no library function in Cangjie for parsing an integer as binary numbers.
these need to be implemented manually.

### Slice of a String

To obtain a slice (substring) of a string, use range indexing. For example:

```
main() {
    let words = "Hello, World"
    println(words[2..])  // llo, World
    println(words[..5])  // Hello
    println(words[2..5])  // llo
    println(words[2..=])  // llo,
}
```

### Convert `String` to array of Runes

To obtain the list of characters (of type Rune) from a string for further processing,
use either `runes` or `toRuneArray`.

The function `toRuneArray` converts string to `Array<Rune>`, so it is possible to
directly access the `Rune` value at particular index. For examepl:

```
let s = "hello"
let arr = s.toRuneArray()
println(arr)  // [h, e, l, l, o]
println(arr[1])  // e
```

The function `runes` converts string to `Iterable<Rune>`, and is more well-suited
for further stream-based processing, for example in for loops and as inputs to
functions like `all` and `filter`. For example:

```
import std.collection.*

main() {
    let s = "hello"
    for (c in s.runes()) {
        print("${c} ")
    }  // h e l l o
    println()
    println(count(filter({c => c == r'l'})(s.runes())))  // 2
}
```

---

# Tuple.md
## Tuple

### Access the elements of a tuple

Elements of a tuple are accessed using the same notation `[]` as for arrays. For example:

```
var pi = (3.14, "PI")
println(pi[0])  // prints 3.140000
println(pi[1])  // prints PI
```

The index must be concrete numbers. Accessing using a variable is not allowed. For example:

```
var a = (1.0, 2.0)
for (i in 0..2) {
    println(a[i])  // compiler error
}
```

Instead, write out the print statements explicitly, since the size of the tuple is
known beforehand.

### Assignment of tuples:

```
let x: (Int64, Float64) = (3, 3.141592)
let x: (Int64, Float64, String) = (3, 3.141592, "PI")
var a: Int64
var b: String
var c: Unit
var f: { => ((1, "abc"), ())}
((a, b), c) = f()  // value of a is 1, value of b is "abc", value of c is '()'
((a, b), _) = ((2, "def"), 3.0)  // value of a is 2, value of b is "def", 3.0 is ignored
let c: (name: String, Int64) = ("banana", 5)  // Error
```

### To iterate over an array of tuples:

```
var a = Array<(Int64, Int64)>([(2, 3), (3, 4)])
for (pair in a) {
    println("(${pair[0]}, {pair[1]})")
}
```

### Immutability of tuples

Tuple types are immutable, i.e. once an instance of a tuple type is defined, its contents can
no longer be updated:

```
var tuple = (true, false)
tuple[0] = false  // Error, 'tuple element' can not be assigned
```

Instead, create a new tuple and copy over some of the elements:

```
var tuple = (true, false)
var tuple2 = (false, tuple[1])
```

### Type parameter of the typle type:

```
func getFruitPrice (): (name: String, price: Int64) {
    return ("banana", 10)
}
```

### Printing tuples and arrays of tuples

Unfortunately, the tuple type does not implement `ToString`, so it does not have `toString`
functions, not can it be used in `println` and string interpolation. To print a tuple
or array of tuples, iterate over the elements explicitly. For example:

```
let a = ("a", 3)
println("${a[0]}, ${a[1]}")  // rather than println(a)
let arr = [("a", 3), ("b", 4)]
for (pair in arr) {
    println("${pair[0]}, ${pair[1]}")
}  // rather than println(arr)
```

### Using tuple in `HashSet` and `HashMap`

Tuples are not Hashable in Cangjie, so it cannot be put into `HashSet` or be used as
keys in a `HashMap`. The following code is incorrect:

```
let set = HashSet<(Int64, Int64)>()  // compiler error: (Int64, Int64) is not Hashable
set.put((0, 0))
for (pair in set) {
    println(pair)
}
```

Instead, create a new structure for the pair. The structure need to implement both
`Hashable` and `Equatable`:

```
struct IntPair <: Hashable & Equatable<IntPair> {
    let x: Int64
    let y: Int64
    public init(x: Int64, y: Int 64) {
        this.x = x
        this.y = y
    }
    public func hashCode(): Int64 {
        "${x}_${y}".hashCode()
    }
    public operator func ==(other: IntPair) {
        this.x == other.x && this.y == other.y
    }
    public operator func !=(other: IntPair) {
        !(this == other)
    }
}

main() {
    let set = HashSet<IntPair>()
    set.put(IntPair(0, 0))
    for (pair in set) {
        let (x, y) = (pair.x, pair.y)
        println("(${x}, ${y})")  // prints (0, 0)
    }
}
```

---
