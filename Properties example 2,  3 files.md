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

```
    
