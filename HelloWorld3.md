```C#

//Hello3.cs
//arguments : A B C D 

using System;

public class Hello3
  {
      public static void Main (string[ ] args)
       {
         Console.WriteLine( "Hello, World!");
         Console.WriteLine( " you entered the following { 0 } command line arguments:" , 
		args. Length );
		
for (int i=0;i<args.Length;i++) 
{
 	Console.WriteLine( " { 0 }" , args [ i ] );
		}
	}
}

OUTPUT : Hello, World!
You entered the following 4 command line arguments:
A
B
C
D

```
