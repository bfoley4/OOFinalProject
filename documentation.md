### Language purpose/genesis
1. Why was the language created?
* Swift: Programming language developed by Apple to use for ios devices.
* C#: Microsoft wanted to develop a OO language since it was becoming much more of an influence in computer programming. 

2. What problems was the language trying to address?
* Swift: Complexity of developing apps for ios. People wanted a easier way to code for ios than other preiously available languages.
* C#: Create a simpler version of complex languages. (C and C++)

3. Is the language a reaction to a previous language or a replacement for another language?
* Swift: Create a more simple and elegant way to develop apps for ios instead of using other languages (objective c). Encorparates multiple functions from other languages.
* C#: Derived from C and C++

### Unique features of the language
* Swift: Completely compatible with objective (Use same APIs). You can use both languages in the same project.
* C#: Partial Classes - you can define a class in multiple files.

### Name spaces
* Swift:
 
      import FrameworkA
      import FrameworkB

      FrameworkA.foo()
      
* C#:

      Using System;
      Console.WriteLine("Hello");
      Console.WriteLine("World!");

* Swift and C#: Shorten code lines into more compact statements. Console.WriteLine()... instead of System.Console.WriteLine()...
  Provide context to the compiler to allow you to create classes unrestricted. (A class named Console)
  
### Types
 * Swift: In Swift, there are two kinds of types: named types and compound types. 
   - Named type: Type that can be given a particular name when defined. Includes classes, structures enumerations, and protocols. In C#, instances of a user-defined class named Dog have the type Dog. The Swift standard library also defines many commonly used name types; arrays, dictionaries, and optional values.
   - Compound type: Type without a name, defined in the language itself.
  
  * C#: 

### Classes
1. Defining
* Swift: 

      class student {
        var studname: String
        var mark: Int 
        var mark2: Int 
      }
      
* C#
    
      public class Person
      {
        // Field
        public string name;

        // Constructor that takes no arguments.
        public Person()
        {
            name = "unknown";
        }

        // Constructor that takes one argument.
        public Person(string nm)
        {
            name = nm;
        }

        // Method
        public void SetName(string newName)
        {
            name = newName;
        }
      }

2. Creating new instances
* Swift:

      let studrecord = student()
      
* C#:

      Person person1 = new Person();

3. Constructing/initializing
* C#: Uses constructor

      public class Taxi
      {
          public bool isInitialized;
          public Taxi()
          {
              isInitialized = true;
          }
      }
  
* Swift: Uses initializer

      init() {
          // perform some initialization here
      }

4. Destructing/de-initializing
* C#: Uses a destructor. Code example:

      class Car
      {
          ~Car()  // destructor
          {
              // cleanup statements...
          }
      }

* Swift: De-initalizer

      deinit {
          // perform the deinitialization
      }
      
### Instance reference name in data type (class)
* Swift: Swift uses the keyword "self" as a special property of an instance that holds the instance itself. Self usually appears in a initializer or a method.
* C#: C# uses the "this" keyword and refers to the current instance of the class. It is also used as a modifier of the first paramater of an extension method.

### Properties
* Swift: Build in custom getters and setters.
  - Similar to the behavior of a method, get accessors in Swift must return a value of the property type. However when returning a private variable from a get accessor, the call is inlined by the compiler so there is no method call over head. Get accesor example:
  
        class Person
        {
            private string name;  // the name field
            public string Name    // the Name property
            {
                get
                {
                    return name;
                }
            }
        }
        
  - Swift's set accesor resembles a method with a return type of void. It uses a parameter called value whose type is the type of the property. Set accesor example (setting the Name property):
  
        class Person
        {
            private string name;  // the name field
            public string Name    // the Name property
            {
                get
                {
                    return name;
                }
                set
                {
                    name = value;
                }
            }
        }

### Interfaces / protocols
1. What does the language support?
2. What abilities does it have?
3. How is it used?

### Inheritance / extension

### Reflection
1. What reflection abilities are supported?
2. How is reflection used?

### Memory management
 * Swift: Swift uses Automatic Reference Counting (ARC) for memory managment. When a new instance of a class is created, ARC allocates a chunk of memory to store information about the instance. When an instance is no longer needed ARC frees the allocated memory so that the memory can be used for other purposes. To allocate and deallocate safely ARC tracks how many properties, constants, and variables for currently referring to the class instance. ARC will never deallocate memory as long as there at least one active reference to the instance exists.
 * C#: C# uses the Common Language Runtime (CLR) to allocate memory. CLR allocates memory to the 'heap' everytime an object is created. The garbage collector in C# works in this heap. The heap is categorized by different 'Generations' that rank the objects based on the lifespan of the object. The garbage collector is then triggered depending on three conditions, when the memory is running out, when the garbage collector found the lifespan of the objects are high thus increasing the threshold allocation, and lastly when the garbage collector is called directly with GC.Collect().

### Comparisons of references and values
1. How are values compared? (i.e. comparing two strings)

### Null/nil references
* Swift: Swift does not support Null. Swift uses nil which means "no value." It is only assignable to optional variables.
* C#: C# supports null which means "no object." Null is the default value of reference-type variables. Ordinary value types cannot be null.

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

### Lambda expressions, closures, or functions as types

### Implementation of listeners and event handlers

### Singleton
1. How is a singleton implemented?
2. Can it be made thread-safe?
3. Can the singleton instance be lazily instantiated?

### Procedural programming
1. Does the language support procedural programming?

### Functional programming
1. Does the language support functional programming?

### Multithreading
1. Threads or thread-like abilities
2. How is multitasking accomplished?
