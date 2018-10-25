[![Godoc][GodocV2SVG]][GodocV2URL]
===========

#### Chapter 7 - Structs and Interfaces
###### 1. What’s the difference between a method and a function?
Method add a reciever before the function. Function does not have a reciever.

###### 2. Why would you use an embedded anonymous field instead of a normal named field?

To acces a variable into a method with unkown type.


###### 3. Add a new perimeter method to the Shape interface to calculate the perimeter of a shape. Implement the method for Circle and Rectangle.

```go
type Shape interface {
  area() float64
  perimeter() float64   
}

func (r *Rectangle) area() float64 {
  l := distance(r.x1, r.y1, r.x1, r.y2)
  w := distance(r.x1, r.y1, r.x2, r.y1)
  return l * w
}
func (r *Rectangle) perimeter() float64 {
  l := distance(r.x1, r.y1, r.x1, r.y2)
  w := distance(r.x1, r.y1, r.x2, r.y1)
```





   [GodocV2SVG]: https://godoc.org/gopkg.in/russross/blackfriday.v2?status.svg
   [GodocV2URL]: https://godoc.org/gopkg.in/russross/blackfriday.v2
