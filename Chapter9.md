[![Godoc][GodocV2SVG]][GodocV2URL]
===========

#### Chapter 9 - Testing

###### 1. Writing a good suite of tests is not always easy, but the process of writing tests often reveals more about a problem than you may at first realize. For example, with our Average function, what happens if you pass in an empty list ( []float64{} )? How could the function be modified to return 0 in this case?

```go

package main
import "fmt"
import "go/Scripts/chapter9/math" //change directory

  func main() {
  input := []float64{1,2,3,4}
  avg := math.Average(input)
  fmt.Println(avg)
  }

  package math
  func Average(input []float64) float64 {
    if len(input) == 0 {
      return 0
    }
    total := float64(0)
    for _, x := range input {
    total += x
    }
  return total / float64(len(input))
  }
```


##### 2. Write a series of tests for the Min and Max functions you wrote in the previous chapter.

unkown

   [GodocV2SVG]: https://godoc.org/gopkg.in/russross/blackfriday.v2?status.svg
   [GodocV2URL]: https://godoc.org/gopkg.in/russross/blackfriday.v2
