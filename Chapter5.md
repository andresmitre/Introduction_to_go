[![Godoc][GodocV2SVG]][GodocV2URL]
===========

#### Chapter 5 - Array, slices, and maps
###### 1. How do you access the fourth element of an array or slice?
```go
x = :=[4]
arr[3]
```

###### 2. What is the length of a slice created using make([]int, 3, 9)?
3


###### 3. Given the following array, what would x[2:5] give you? x := [6]string{"a","b","c","d","e","f"}
x[2:5]
[c d e]


###### 4. Write a program that finds the smallest number in this list:

```go

package main

import "fmt"

func main()  {
  var min int
  x := []int{ 48,96,86,68, 57,82,63,70, 37,34,83,27, 19,97, 9,17,}
  for i, v := range x{
    if i == 0 || v < min {
      min = v
    }
  }
  fmt.Println(min)
}
```



   [GodocV2SVG]: https://godoc.org/gopkg.in/russross/blackfriday.v2?status.svg
   [GodocV2URL]: https://godoc.org/gopkg.in/russross/blackfriday.v2
