### Errors and exception handling
 * Swift: 
   - Errors are represented by values of types that conform to the Error protocal that indicats a type can be used for error handling. Error conditions are ideal for Swift enumerations with associate values allowing additional information about status of an error. Enumeration example for error conditions:
 
         enum VendingMachineError: Error {
             case invalidSelection
             case insufficientFunds(coinsNeeded: Int)
             case outOfStock
         }
     
    - Throwing errors indicates that something unexpected happened and the execution stops. A "throw" statement can be used to throw and error.
    
          throw VendingMachineError.insufficientFunds(coinsNeeded: 5)
    
    - Four ways to handle errors in Swift. Using throwing functions, a do-catch statement, as an optional value, or state that the error will not occur.
    
      * Throwing functions: You can use the "throws" keyward to indicate that a method can throw an error. It is place after its parameters.
      
            func canThrowErrors() throws -> String
            func cannotThrowErrors() -> String
           
      * Do-catch statement: Used to hadle errors by running a block of code. An error that is thrown by the do clause is matched against the catch clause to determine which catch statement can handle the error. Catch clauses don't have to handle every possible error that the do clause can throw. If none of the catch clauses handle the error, it moves on t the surrounding scope. But the error still must be handled.
      
            do {
                try expression
                statements
            } catch pattern 1 {
                statements
            } catch pattern 2 where condition {
                statements
            }
          
      * Converting Errors to Optional Values: Use "try?" to handle by converting to optional value. If an error is thrown by try? statement, the value of the expression is nil.
      
            func someThrowingFunction() throws -> Int {
                // ...
            }

            let x = try? someThrowingFunction()

            let y: Int?
            do {
                y = try someThrowingFunction()
            } catch {
                y = nil
            }
            
       * Disabling Error Propagation: When you know a throwing method won't throw an error at runtime, you can use "try!" before the expression to disable error propagation. If an error is thrown, a runtime error will occur.ggg
       
             let photo = try! loadImage(atPath: "./Resources/John Appleseed.jpg")
             
  * C#
    - Try block is used to partition code that might be affected by an exception. Catch blocks handle resulting exceptions. Finally block contains code that is run ragardless if an error is thrown or not.
    
          try
          {
              // Code to try goes here.
          }
          catch (SomeSpecificException ex)
          {
              // Code to handle the exception goes here.
          }
          finally
          {
              // Code to execute after the try (and possibly catch) blocks 
              // goes here.
          }
