### Language purpose/genesis
1. Why was the language created?
* Swift: Programming language developed by Apple to use for ios devices.
* C#: Microsoft wanted to develop a OO language since it was becoming much more of an influence in computer programming. 


2. What problems was the language trying to address?
* Swift: Complexity of developing apps for ios. People wanted a easier way to code for ios than other preiously available languages.
* C#: Create a simpler version of complex languages. (C and C++)

3. Is the language a reaction to a previous language or a replacement for another language?
* Swift: Create a more simple and elgant way to develop apps for ios instead of using other languages (objective c). Encorparates multiple functions from other languages.
* C#: Derived from C and C++

### Unique features of the language
1. Does the language have any particularly unique features?
* Swift: Completely compatible with objective (Use same APIs). You can use both languages in the same project.
* C#: Partial Classes - you can define a class in multiple files.

### Name spaces
1. How are name spaces implemented?
* Swift:
 
      import FrameworkA
      import FrameworkB

      FrameworkA.foo()
      
* C#:

      Using System;
      Console.WriteLine("Hello");
      Console.WriteLine("World!");

2. How are name spaces used?
* Swift and C#: Shorten code lines into more compact statements. Console.WriteLine()... instead of System.Console.WriteLine()...
  Provide context to the compiler to allow you to create classes unrestricted. (A class named Console)
  
### Types
1. What types does the language support?
  * Swift: In Swift, there are two kinds of types: named types and compound types. 
    - A named type is a type that can be given a particular name when it is defined. Named types include classes, structures, enumerations, and protocols. For example, instances of a user-defined class named MyClass have the type MyClass. In addition to user-defined named types, the Swift standard library defines many commonly used named types, including those that represent arrays, dictionaries, and optional values.
    - A compound type is a type without a name, defined in the Swift language itself. There are two compound types: function types and tuple types. A compound type may contain named types and other compound types. For instance, the tuple type (Int, (Int, Int)) contains two elements: The first is the named type Int, and the second is another compound type (Int, Int).
  
  * C#: 
    - Built-in Types: C# provides a standard set of built-in numeric types to represent integers, floating point values, Boolean expressions, text characters, decimal values, and other types of data. There are also built-in string and object types. These are available for you to use in any C# program.
    - Custom Type: You use the struct, class, interface, and enum constructs to create your own custom types. The .NET Framework class library itself is a collection of custom types provided by Microsoft that you can use in your own applications. By default, the most frequently used types in the class library are available in any C# program. Others become available only when you explicitly add a project reference to the assembly in which they are defined. After the compiler has a reference to the assembly, you can declare variables (and constants) of the types declared in that assembly in source code.
    - Reference Types: A type that is defined as a class, delegate, array, or interface is a reference type. At run time, when you declare a variable of a reference type, the variable contains the value null until you explicitly create an instance of the object by using the new operator, or assign it an object that has been created elsewhere by using 

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
* C#: Uses a destructor

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
1. this? self?
* Swift: In Swift self is a special property of an instance that holds the instance itself. Most of the times self appears in an initializer or method of a class, structure or enumeration.
* C#: The this keyword refers to the current instance of the class and is also used as a modifier of the first parameter of an extension method.

### Properties
1. Getters and setters...write your own or built in?
* Swift: Build in custom getters and setters.
* C#
  - The get Accessor: The body of the get accessor resembles that of a method. It must return a value of the property type. The execution of the get accessor is equivalent to reading the value of the field. For example, when you are returning the private variable from the get accessor and optimizations are enabled, the call to the get accessor method is inlined by the compiler so there is no method-call overhead. However, a virtual get accessor method cannot be inlined because the compiler does not know at compile-time which method may actually be called at run time. The following is a get accessor that returns the value of a private field name:
  
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
        
  - The set Accessor: The set accessor resembles a method whose return type is void. It uses an implicit parameter called value, whose type is the type of the property. In the following example, a set accessor is added to the Name property:
  
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

2. Backing variables?


3. Computed properties?


### Interfaces / protocols
1. What does the language support?
2. What abilities does it have?
3. How is it used?

### Inheritance / extension

### Reflection
1. What reflection abilities are supported?
2. How is reflection used?

### Memory management
1. How is it handled?
2. How does it work?
3. Garbage collection?
4. Automatic reference counting?

### Comparisons of references and values
1. How are values compared? (i.e. comparing two strings)

### Null/nil references
1. Which does the language use? (null/nil/etc)
2. Does the language have features for handling null/nil references?

### Errors and exception handling

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
