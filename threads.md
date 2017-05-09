### Multithreading

* Swift: there are very few ways to implement multi-threading in iOS not just in Swift but in Objective C too. The best way in Swift is operation queues.

      let queue = OperationQueue()

      queue.addOperation() {
          // do something in the background

          OperationQueue.main.addOperation() {
              // when done, update your UI and/or model on the main queue
          }
      }
      
 * C#: System.Threading.Thread class used for threads. Allows creating and accessing individual threads in a multithread application.
 
       using System;
       using System.Threading;

       namespace MultithreadingApplication
       {
          class MainThreadProgram
          {
             static void Main(string[] args)
             {
                Thread th = Thread.CurrentThread;
                th.Name = "MainThread";
                Console.WriteLine("This is {0}", th.Name);
                Console.ReadKey();
             }
          }
       }
