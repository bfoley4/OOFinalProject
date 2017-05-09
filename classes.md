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
