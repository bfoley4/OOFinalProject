### Singleton
1. How is a singleton implemented?
2. Can it be made thread-safe?
3. Can the singleton instance be lazily instantiated?

* Singleton classes must be thread safe and made sure that initialization code only runs once at runtime.
  - Swift: 

        class Singleton {
            static let sharedInstance: Singleton = {
                let instance = Singleton()

                // setup code

                return instance
            }()
        }
        
  - C#: The following implementation has two advantages: the class is allowed additional functionality and instantiation is not performed until an object asks for an instance (lazy instanstiation).
  
        using System;

        public class Singleton
        {
           private static Singleton instance;

           private Singleton() {}

           public static Singleton Instance
           {
              get 
              {
                 if (instance == null)
                 {
                    instance = new Singleton();
                 }
                 return instance;
              }
           }
        }
