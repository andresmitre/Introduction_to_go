[![Godoc][GodocV2SVG]][GodocV2URL]
===========

#### Chapter 6 - functions
###### 1. sum is a function that takes a slice of numbers and adds them together. What would its function signature look like in Go?
```go
func sum(x []float64) float64{
}
```

###### 2. Write a function that takes an integer and halves it and returns true if it was even or false if it was odd. For example, half(1) should return (0, false) and half(2) should return (1, true).

```go
package main

import "fmt"

func main() {
fmt.Print("Enter number:")
var input int
fmt.Scanf("%d", &input)
f(input)
}


func f(x int)  {
if x % 2==0{
  fmt.Println(x, "is an odd number")
}else{
fmt.Println(x, "is an even number")
}
}
```


###### 3. Write a function with one variadic parameter that finds the greatest number in a list of numbers.
```go
package main

import "fmt"

func main() {
fmt.Println(max(1,2,3))
}

func max(args ...int) int{
var max int
for i, v := range args{
  if i == 0 || v > max {
    max = v
  }
}
return max
}

```
###### 4. Using makeEvenGenerator as an example, write a makeOddGenerator function that generates odd numbers.
```go
package main

import "fmt"

func makeEvenGenerator() func() uint {
   i := uint(1)
   return func() (ret uint) {
     ret = i
     i += 2
     return
}
}
func main() {
  nextEven := makeEvenGenerator()
   fmt.Println(nextEven()) // 0
   fmt.Println(nextEven()) // 2
   fmt.Println(nextEven()) // 4
}
```



###### 5. The Fibonacci sequence is defined as: fib(0) = 0, fib(1) = 1, fib(n) = fib(n-1) + fib(n-2). Write a recursive function that can find fib(n).
```go
func fib(n int) int {
switch n {
  case 0:
    return 0
  case 1:
    return 1
  default:
    return fib(n-1) + fib(n-2)
  }
}
```
###### 6. What are defer, panic, and recover? How do you recover from a runtime panic?

Defer:  is used when resources need to be freed in some way.

Panic: cause the function to cause runtime error.

Recover: recover stops the panic and returns the value that was passed to the call to panic.

defering a call in a function

###### 7. How do you get the memory address of a variable

Using a pointer. Pointers reference a location in memory where a value is stored rather than the value itself.

###### 8. How do you assign a value to a pointer?

Pointer is represented using an asterisk and the type of the stored value.


###### 9. How do you create a new pointer

using the built-in new function

###### 10. What is the value of x after running this program:

x = 2.25





   [GodocV2SVG]: https://godoc.org/gopkg.in/russross/blackfriday.v2?status.svg
   [GodocV2URL]: https://godoc.org/gopkg.in/russross/blackfriday.v2
