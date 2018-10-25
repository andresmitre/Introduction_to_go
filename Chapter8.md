[![Godoc][GodocV2SVG]][GodocV2URL]
===========

#### Chapter 8 - Packages
###### 1. Why do we use packages?
For a good structure and understand of the code.

######  2. What is the difference between an identifier that starts with a capital letter and one that doesn’t (e.g., Average versus average)?

if an identifier starts with a capital letter, that means other packages (and programs) are able to see it.



###### 3. What is a package alias? How do you make one?

Is other way to declare a package. import f "fmt" .


###### 4. We copied the average function from Chapter 6 to our new package. Create Min and Max functions that find the minimum and maximum values in a slice of float64s.

```go
func minimum(input []int) int {
  var min int
  for i, x := range input {
  if i == 0 || x < min {
  min = x
      }
    }
  return min
  }


  func maximum(input []int) int {
    var max int
    for i, x := range input {
    if i == 0 || x > max {
    max = x
        }
      }
    return max
    }
```

##### 5. How would you document the functions you created in #4?

commenting the function



   [GodocV2SVG]: https://godoc.org/gopkg.in/russross/blackfriday.v2?status.svg
   [GodocV2URL]: https://godoc.org/gopkg.in/russross/blackfriday.v2
