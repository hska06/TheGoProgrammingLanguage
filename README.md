# TheGoProgrammingLanguage

My notes from reading the book.

# Chapter 5 : Functions

## recursion

Go implementations use variable-size stacks that start small and grow as needed up to a limit on the order ofagigabyte.
This lets us use recursion safely and without worrying about overflow

## defer 
  Any number of call may be deferred; they are executed in the reverse of the order in which they were deferred.
  
  Deferred functions run after return statements have updated the function's result variables. Because an annonymous function can access its enclosing function's variables, including named results, a deferred annoymous function can observe the function's results and even change the values that the enclosing function returns to its caller.
  
 ``` go
  func cube(x int ) result int {
   defer func () { result *= x}
   return x*x
  }
  ```
  
  
