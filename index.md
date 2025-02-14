
## Function Declarations
### Scala
```scala
def sum(a: Int, b: Int): Int = a+b 
```
### Kotlin
```
fun sum(a: Int, b: Int): Int = a+b
```

## Passing Functions
### Scala
```scala
def sumf(f: Int => Int, a: Int, b: Int): Int =
    if (a > b) 0
    else f(a) + sumf(f, a + 1, b)
  
sumf(x => x*x, 1, 5)
```
### Kotlin
```kotlin
fun sumf(f: (Int) -> Int, a: Int, b: Int): Int =
    if (a > b) 0
    else f(a) + sumf(f, a + 1, b)
        
sumf({ x -> x * x }, 2, 3)
```