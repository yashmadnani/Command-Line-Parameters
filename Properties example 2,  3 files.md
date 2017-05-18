```C# 
// File1 abstractshape.cs
// compile with / target: libraray
// csc / targer: library abstractshape.cs
using system;

public string myId;
{
  private string myId;
  
  public shape(string s)
  {
    Id = s; // calling the set accessor of the Id property
  }
  
  public string Id
  {
    get
    {
      return myId;
    }
    
    set
    {
        myId = value;
    }    
 }
 // Area is a read-only property - only a get accessor is needed: 
 
 public abstract double Area
 {
    get;
 }
 
 public override string ToString()
 {
    return Id + " Area = " + string.Format("{0:F2}", Area);
 }
 
}



//*********************************************************************************************************


//file 2 shapes.cs
// compile with : /target: library / referece:abstractshape.dll

public class Square: Shape
{
    private int mySide;
    
    public Square(int side , string id) : base(id)
    { 
      mySide = side;
    }
    
    public override double Area
    {
        get
        {
            // Given the side, return the area of a square: 
            return mySide * mySide;
            }
        }
   }
   
   public class Circle : Shape
   {
      private iny myRadius;
   
      public Circle(int radius, string id) : base(id)
      {
          myRadius = radius;
      }
      
      public override double Area
      {
        get
        {
            // Given the radius, retunr the area of a circle :
            return myRadius * myRadius * System.math.PI;
        }
     } 
 }
 
 public class Rectangle : Shape 
 {
    private int myWidth;
    private int myHeight;
    
    public rectangle(int width, int height, string id): base(id)
    {
        myWidth = width;
        myHeight = height;
    }
    
    public override double Area
    {
        get
        {
          // Given the width and height, return the area of a rectangle:
          return myWidth * myHeight;
        }
    }        
}

//*******************************************************************************************************

```

