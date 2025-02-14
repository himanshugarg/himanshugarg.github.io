## Declaring Named Functions

### Scala uses def

```scala
def sum(a: Int, b: Int): Int = a+b 
```

### Kotlin uses fun

```kotlin
fun sum(a: Int, b: Int): Int = a+b
```

## Named Function Reference

### Scala

```scala
sum
```

### Kotlin uses ::
```kotlin
::sum
```

## Lambda Functions
### Scala uses =>
```scala
def sumf(f: Int => Int, a: Int, b: Int): Int =
    if (a > b) 0
    else f(a) + sumf(f, a + 1, b)
```
```scala
sumf(x => x*x, 1, 5)
```
### Kotlin uses -> and {} 
```kotlin
fun sumf(f: (Int) -> Int, a: Int, b: Int): Int =
    if (a > b) 0
    else f(a) + sumf(f, a + 1, b)
```
```kotlin
sumf({ x -> x * x }, 2, 3)
```
OR
```kotlin
sumf({ it * it }, 2, 3) 
```
