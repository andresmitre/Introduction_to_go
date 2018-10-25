[![Godoc][GodocV2SVG]][GodocV2URL]
===========


#### Chapter 3 - Variables
###### 1. What are two ways to create a new variable?
:= and =


###### 2. What is the value of x after running x := 5; x += 1?
x=6


###### 3. What is scope? How do you determine the scope of a variable in Go?
Range of places where you are allowed to use a variable

###### 4. What is the difference between var and const?
value of constant does not change in code


###### 5. Using the example program as a starting point, write a program that converts from Fahrenheit into Celsius (C = (F − 32) * 5/9).

```go
package main

import "fmt"

var (
  Celsius float64
)

func main()  {
fmt.Print("Enter temperature: ")
var input float64
fmt.Scanf("%f", &input)

Celsius = ((input-32)* 5/9)
fmt.Println("Celsius: ", Celsius)
fmt.Println("Fahrenheit: ", input)
}

```

###### 6. Write another program that converts from feet into meters (1 ft = 0.3048 m)

```go
package main

import "fmt"

var (
  meters float64
)
func main(){
  fmt.Print("Enter feet: ")
  var input float64
  fmt.Scanf("%f", &input)
  meters := input*0.3048
  fmt.Println("meters: ", meters)
  fmt.Println("feet: ", input)

}

```


   [GodocV2SVG]: https://godoc.org/gopkg.in/russross/blackfriday.v2?status.svg
   [GodocV2URL]: https://godoc.org/gopkg.in/russross/blackfriday.v2
