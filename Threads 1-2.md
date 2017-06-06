```C#

using Sytem;
using System.Threading;
namespace Chapter1
{
    public static class Program
    {
        public static void ThreadMethod()
        {
          for (int i=0; i<10; i++)
          {
            Console.WriteLine("ThreadProc: {0}" , i);
            Thread.Sleep(1000);
          }
      }
      
        public static void Main()
        {
          Thread t= new Thread(new ThreadStart(ThreadMethod));
          t.IsBackground = true;
          t.Start();
        }
     }
 }
 
 //If you run this application with the IsBackground property set to true, the application exits immediately. If you set it to false (creating a foreground thread), the application prints the ThreadProc message ten times.
