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
        
* C#: Get accesors return private values and set accessors perform data validation.

      using System;

      class TimePeriod
      {
         private double seconds;

         public double Hours
         {
             get { return seconds / 3600; }
             set { 
                if (value < 0 || value > 24)
                   throw new ArgumentOutOfRangeException(
                         $"{nameof(value)} must be between 0 and 24.");

                seconds = value * 3600; 
             }
         }
      }
