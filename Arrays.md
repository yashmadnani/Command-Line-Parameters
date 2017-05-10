```C#

using System;
class DeclareArraySample
{ 
  public static void Main()
  {
      // Single-dimension array 
      int[] numbers = new int[5];
      
      //Multidimensional array
      string[,] names = new string[5,4];
      
      //Array-of-arrays (Jagged array)
      byte[] [] scores = new byte[5][];
      
      //create the jagged array
      for (int i=0; i < scores.length; i++)
      {
        Console.WrtiteLine(" Length of row {0} is {1}" , i, scores[i].Length);
        }
    }
}


OUTPUT : 
Length of row 0 is 3
Length of row 1 is 4
Length of row 2 is 5
Length of row 3 is 6
Length of row 4 is 7

```
