# Start with Kotlin
* to speed up comile, in `build.gradle` add the following:
```
kotlin.incremental=true
```

# Kotlin Basics

## val and var
## Type inference
* compile tries to figure out the type:
```kotlin
val someLong = 123456L
```

## Basic Types
### Numbers : Long, Int, Short, Byte, Double, Float
* Bitwise operation:
```kotlin
val leftShift = 1 shl 2
val rightShift = 1 shr 2
val unsignedRightShift = 1 ushr 2

val and = 1 and 0x00001111
val or = 1 or 0x00001111
val xor = 1 xor 0x00001111
val inv = 1.inv() 
```

### Boolean
### Chars
### Strings
### Arrays
```kotlin
val array = arrayOf(1,2,3)
val perfectSquares = Array(10, {k -> k*k}) //size and generator
```
* to avoid boxing use: ByteArray, CharArray, ShortArray, IntArray, LongArray, BooleanArray, FloatArray, DoubleArray

## Comments
## Packages
## Imports
### Wildcard Imports
### Import Renaming
```kotlin
import com.jenac.here as there
```
## String templates / interpolation
```kotlin
"hi, this is ${someVariableValue}"
```

## Ranges
```kotlin
val aToZ = "a".."z"
val isTure = "c" in aToZ
val oneToNine = 1..9
val isFalse = 11 in oneToNine
```
* downTo(), rangeTo()
```kotlin
val countingDown = 100.downTo(2)
val rangeTo = 10.rangeTo(20)
```

* step()
```kotlin
val oneToFifty = 1..50
val oddNumbers = oneToFifty.step(2)
```

* reversed()
```kotlin
val countingDownEvenNumbers = (2..100).step(2).reversed()
```

## Loops
* while
```kotlin
while(true) {
    ...
}
```

* for
```kotlin
val list = listOf(1, 2, 3, 4)
for (k in list) {
    ...
}

val set = setOf(1,2 )
```