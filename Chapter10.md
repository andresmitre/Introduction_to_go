[![Godoc][GodocV2SVG]][GodocV2URL]
===========

#### Chapter 10 - Concurrency

######1. How do you specify the direction of a channel type?

We can specify a direction on a channel type, thus restricting it to either sending or
receiving. For example, pinger ’s function signature can be changed to this:
func mascota(c perro<- string)


##### 2. Write your own Sleep function using time.After .


```go

func main() {
c1 := make(chan string)
go func() {
for {
c1 <- "from 1"
time.Sleep(time.Second * 2)
}
}()

go func() {
for {
  select {
    case msg1 := <- c1:
    fmt.Println(msg1)
      }
    }
  }()

var input string

fmt.Scanln(&input)

}

select {
case msg1 := <- c1:
fmt.Println("Message 1", msg1)
case <- time.After(time.Second):
fmt.Println("timeout")
}

```



###### 3. What is a buffered channel? How would you create one with a capacity of 20?


A buffered channel is asynchronous; sending or receiving a message will not wait unless the channel
is already full. If the channel is full, then sending will wait until there is room for at
least one more int .
```go
c:= make(chan int, 1)
```


   [GodocV2SVG]: https://godoc.org/gopkg.in/russross/blackfriday.v2?status.svg
   [GodocV2URL]: https://godoc.org/gopkg.in/russross/blackfriday.v2
