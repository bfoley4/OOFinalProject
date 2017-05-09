### Lambda expressions, closures, or functions as types

* Swift: Swift uses closures which is similiar to Java's lamda expressions.
  - Example of a closure in swift

        func makeIncrementer(forIncrement amount: Int) -> () -> Int {
            var runningTotal = 0
            return () -> Int {
                runningTotal += amount
                return runningTotal
            }
        }
        
* C#: C# uses lamda expressions that you can use to create delegates or expression tree types.

      delegate int del(int i);  
      static void Main(string[] args)  
      {  
          del myDelegate = x => x * x;  
          int j = myDelegate(5); //j = 25  
      } 
