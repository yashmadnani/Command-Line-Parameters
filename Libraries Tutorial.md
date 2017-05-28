```C#

// File 1 Factorial.cs
// compile with: /target: library
using System;

// Declare a namespace. You need to package your libraries according to 
//their namespace so the .NET runtime can correctly load the classes.

namespace Functions
{
    public class Factorial
    {
// The "Calc" static method calculates the factorial value 
// for the specified integer passes in:
    public static int Calc(int i)
     {
        return((i <= 1) ? 1 : (i * Calc(i-1)));
     }
   }
}

********************************************************************************************************

// File 2 - DigitCounter.cs
// Compile with: /target:library / out: Functions.dll/reference:Factorial.dll

using System;
// Declare the same namespace as the one in Factorial.cs
// this simple allows types to be added to the namespace 

namespace Functions 
{
    public class DigitCount
    {
        // The NumverOf Digits static method calculates the number of
        //digit characters in the passed string:
        
        public static int NumberOfDigits(string theString)
        {
            int count = 0;
            for (int i = 0; i<theString.Length; i++ )
            {
              if ( Char.IsDigit(theString[i]) )
              {
                  count++;
              }
            }
            return count;
            }
         }
     }
     
********************************************************************************************************


// File 3 - FunctionClient.cs
// compile with : /reference:Functions.dll, Factorial.dll/out:FunctionTest.exe
//arguments: 3  5  10

using System;

//The following using directive makes the types defined in the Funtions
//namespace available in this compilation unit:

using Functions;
class FuntionClient
{
    public static void Main(string[] arge)
    { 
        Console.writeLine("Function Client");
        
        if ( args.Length == 0 )
        {
            Console.WriteLine("Usage: FunctionTest ...");
            return;
        }
        
        for ( inti = 0; i< args.Length; i++ )
        {
            int num = Int32.Parse(args[i]);
            Console.WriteLine(
            "The Digit count for String[{0}] is [{1}]", args[i],
            //Invoke the NumberOfDigits static method in the 
            // DigitCount class:
            DigitCount.NumberOfDigit(args[i])));
            Console.WriteLine(
              "The Factorial for [{0}] is [{1}]",
              num,
              //Invoke the Calc static method in the Factorial class:
              Factorial.Calc(num) );
         }
     }
}

*******************************************************************************************************
OUTPUT

Function Client
The Digit Count for String [3] is [1]
The Factorial for [3] is [6]
The Digit Count for String [5] is [1]
The Factorial for [5] is [120]
The Digit Count for String [10] is [2]
The Factorial for [10] is [3628800]

```
        
            
       
