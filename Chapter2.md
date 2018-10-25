[![Godoc][GodocV2SVG]][GodocV2URL]
===========


#### Chapter 2 - Types
###### 1. How are integers stored on a computer?
      Integers are stored on base-2. (i.e. 000, 001, 010, 011, 100, 101, 111)

###### 2. We know that (in base 10) the largest one-digit number is 9 and the largest two- digit number is 99. Given that in binary the largest two-digit number is 11 (3), the largest three-digit number is 111 (7) and the largest four-digit number is 1111 (15), what’s the largest eight-digit number? (Hint: 101−1 = 9 and 102 −1 = 99)
n^8 = 255 bits

###### 3. Although overpowered for the task, you can use Go as a calculator. Write a pro‐ gram that computes 32,132 × 42,452 and prints it to the terminal (use the * oper‐ ator for multiplication).

```go
package main

import "fmt"


func main () {
  var  a, b int
  a = 32132
  b = 42452
  fmt.Println(a*b)
}
```

###### 4. What is a string? How do you find its length?
    A sequence of character. using the "len" function.

###### 5. What’s the value of the expression (true && false) || (false && true) || ! (false && false)?
 (true && false) = False

 (false && true) = False

 !(false && false) = True

 False || False || True = True


   [GodocV2SVG]: https://godoc.org/gopkg.in/russross/blackfriday.v2?status.svg
   [GodocV2URL]: https://godoc.org/gopkg.in/russross/blackfriday.v2
